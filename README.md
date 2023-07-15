# 💥 eJPTv2 Command Notes 🖥️

This collection of essential commands was instrumental in helping me successfully pass the eLearnSecurity Junior Penetration Tester (eJPTv2) exam. Explore the comprehensive references for network scanning, password cracking, web application testing, privilege escalation, and more. 💪🚀

## 🔍 Network Scanning and Enumeration

### 📊 Initial Network Scan
```
nmap -sC -sV -T4 -O -Pn 10.10.10.10/24 -p-
```

### 📈 TCP Port Scanning with Metasploit
```
use auxiliary/scanner/portscan/tcp
set RHOSTS 10.10.10.10/24
set PORTS 1-65535
set THREADS 32
set TIMEOUT 500
run
```

### 🕵️ Version Detection and Script Scanning with Metasploit
```
use auxiliary/scanner/portscan/versions
set RHOSTS 10.10.10.10/24
set PORTS 1-65535
set THREADS 32
run
```

### 💻 Operating System Detection with Metasploit
```
use auxiliary/scanner/portscan/os
set RHOSTS 10.10.10.10/24
set PORTS 1-65535
set THREADS 32
run
```

## 🔒 Password Cracking with Hydra

### 🔓 SMB Password Cracking
```
hydra -l administrator -P /usr/share/wordlists/rockyou.txt 1.1.1.1 smb
```

### 🔑 RDP Password Cracking
```
hydra -l administrator -P /usr/share/wordlists/rockyou.txt 1.1.1.1 rdp
```

### 🔑 SSH Password Cracking
```
hydra -l administrator -P /usr/share/wordlists/rockyou.txt 1.1.1.1 ssh
```

## ☁️ WebDAV Testing

### ✅ WebDAV Vulnerability Check
```
davtest -url http://10.0.16.177/webdav
```

### ✅ WebDAV Support Check
```
davtest -url http://1.1.1.1
```

## 💾 FTP

### 👥 Anonymous Login Check
```
ftp-anon
```

### ⬇️ Downloading File from FTP Server
```
ftp
get filename.txt
```

## 📂 Directory Brute-Forcing

### 🔑 Brute-Forcing Directories with Wordlist
```
dirb <url> <wordlist>
```

### 🔑 Brute-Forcing Directories with Default Wordlist
```
dirb <url>
```

### 🔑 Default Wordlist for Directory Brute-Forcing
```
/usr/share/wordlist/dirb/
```

