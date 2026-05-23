# IoT Penetration Testing Lab

> A structured lab environment for discovering and exploiting vulnerabilities in consumer IoT devices — ethically, in a controlled setup.

## Objective
Set up and operate a controlled penetration testing lab targeting smart cameras, smart bulbs, and home routers. Covers network reconnaissance, firmware extraction, protocol analysis, and physical hardware access.

## Tools Used
| Tool | Purpose |
|------|---------|
| Kali Linux | Primary attack OS |
| Nmap | Port scanning & service fingerprinting |
| Wireshark | Packet capture & protocol analysis |
| Shodan | Internet-exposed device recon & CVE lookup |
| Binwalk | Firmware extraction & entropy analysis |
| Firmwalker | Post-extraction filesystem crawler |
| Ghidra | Binary reverse engineering |
| RouterSploit | Embedded device exploit framework |
| MQTT Explorer | IoT message broker inspection |

## Lab Setup
- Isolated VLAN / travel router for all IoT devices
- Kali Linux (VM or bare metal), 8 GB RAM minimum
- Monitor-mode Wi-Fi adapter (Alfa AWUS036ACH)
- CP2102 USB-to-Serial adapter for UART access

## Attack Phases
1. **Network Recon** — Nmap host discovery, port & service scan
2. **OSINT** — Shodan CVE lookup by device model
3. **Traffic Analysis** — Wireshark capture, MQTT/RTSP decode
4. **Default Credential Testing** — Hydra brute-force on Telnet/HTTP
5. **Firmware Analysis** — Binwalk extract → Firmwalker secrets scan
6. **Reverse Engineering** — Ghidra binary analysis for overflow bugs
7. **Protocol Exploitation** — MQTT wildcard subscribe, RTSP hijack, UPnP SOAP abuse

## Skills Learned
- Embedded device security (UART, JTAG, flash dump)
- IoT communication protocols (MQTT, RTSP, Zigbee, CoAP, BLE)
- Firmware reverse engineering (MIPS/ARM, QEMU emulation)
- Physical security & hardware hacking
- OSINT & Shodan recon
- Penetration test report writing

## Disclaimer
All techniques are demonstrated on personally owned devices in an isolated lab. Unauthorized access to IoT devices is illegal. This repository is for educational purposes only.

