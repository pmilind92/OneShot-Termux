**Disclaimer**: I am not responsible for what you do with this tool or this information. The use of this tool should only be attempted on networks you own or have permission to test. please use this tool wisely.

# OneShot-Termux
OneShot-Termux is a Implementation of [OneShot](https://github.com/drygdryg/OneShot) on Termux with DEB package, is a WiFi Hacking tool that allows to run WPS PIN attacks ([Pixie Dust](https://forums.kali.org/showthread.php?24286-WPS-Pixie-Dust-Attack-Offline-WPS-Attack) and bruteforce) without monitor mode with the wpa_supplicant, Originally made by @rofl0r and modded by @drygdryg (the original repository removed, somehow).

# Requirements
- An Android device with Termux installed
- Root Access
- Working brain with minimal cli knowledge 🧠 

# Installation
```shell
apt update -y && apt upgrade -y
apt install wget root-repo openssl -y
wget https://github.com/pmilind92/OneShot-Termux/releases/download/0.1/oneshot.deb
apt install ./oneshot.deb
```

# DEB package build
```shell
make pack-deb
```

## Usage examples
Start Pixie Dust attack on a specified BSSID:
 ```shell
 sudo oneshot -i wlan0 -b 00:90:4C:C1:AC:21 -K
 ```
Show avaliable networks and start Pixie Dust attack on a specified network:
 ```shell
 sudo oneshot -i wlan0 -K
 ```
 
