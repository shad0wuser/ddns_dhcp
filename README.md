# Dynamic DNS and DHCP (bind9 & isc-dhcp-server)
Copy/Modify the configuration files

## Generating the key to secure DNS / DHCP exchanges
```bash
dnssec-keygen -a HMAC-MD5 -b 128 -r /dev/urandom -n USER DDNS_UPDATE
```
It will generate two key files. Just copy the **key** in `Kddns_update.+157+57083.private` and paste to **secret** case on `ddns.key` file.

The both files `/etc/bind/ddns.key` and `/etc/dhcp/ddns.key` must be identical.

**Supported by Sofiane**
