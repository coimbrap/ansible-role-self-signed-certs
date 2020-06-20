# Ansible role - Selfsigned certificates

Utilise pyOpenSSL sur l'hôte

host_vars/certs/cert.yml
```yaml
generate_ca_cert: true # Just once
generate_client_cert: true
generate_server_cert: true
generate_pfx_cert: true # For web browser

# -----------
# SERVER CERT
# -----------
tls_server_key_cn: '*.loc.elukerio.org'
server_name: haproxy

# -----------
# CLIENT CERT
# -----------
tls_client_authname: [coimbrap,mablr]

# --------
# PFX CERT
# --------
tls_pfx_password: strongpass
fetch_pfx: true # Copy pfx to your computer
fetch_dest: ..
```

### License

GPLv3 - Elukerio

### Author Information

Pierre Coimbra
