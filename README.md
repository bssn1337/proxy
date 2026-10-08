# DNS Proxy Resolver

Automatic DNS repair and encrypted DNS resolver for Linux servers.

Script ini dibuat untuk membantu server Linux yang mengalami masalah DNS seperti:

- `curl: (6) Could not resolve host`
- `Could not resolve host`
- `Resolving timed out`
- DNS publik `8.8.8.8` / `1.1.1.1` tidak dapat diakses melalui port `53`
- DNS request diarahkan ke resolver internal
- `wget`, `curl`, `git`, `yum`, atau aplikasi server gagal melakukan DNS resolution
- Server masih dapat melakukan koneksi HTTPS melalui port `443`

Script menggunakan **dnscrypt-proxy** sebagai encrypted DNS resolver dan dapat bekerja bersama **BIND/named**.

---

## Quick Install

Jalankan:

```bash
curl -fsSL https://raw.githubusercontent.com/bssn1337/proxy/main/resolve | bash

curl -fsSL https://raw.githubusercontent.com/bssn1337/proxy/main/resolve -o /tmp/resolve

wget -qO- https://raw.githubusercontent.com/bssn1337/proxy/main/resolve | bash


curl -4 --resolve raw.githubusercontent.com:443:185.199.108.133 \
  -fsSL \
  https://raw.githubusercontent.com/bssn1337/proxy/main/resolve | bash
