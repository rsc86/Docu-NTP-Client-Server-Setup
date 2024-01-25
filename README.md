# Docu-NTP-Client-Server-Setup
Docuemtation of the NTP Client Server setup for Debian 11 "bullseye"

(https://wiki.debian.org/NTP)


## Server

### Preperation
```
apt update && apt upgrade --show-upgraded
```
### Installation
```
apt install ntp
```
### Configuration with ufw
```
sudo ufw allow from any proto udp to any port 123
```

### Verify NTP service is up and running
```
sudo systemctl status ntp
```

## Client

### Installation
``` 
sudo apt install ntpdate ntp
```

### Configuration
Add server your.ip.addr.ess prefer iburst
```
sudo vi /etc/ntpsec/ntp.conf
```
sudo systemctl restart ntp && systemctl status ntp && ntpq -p
