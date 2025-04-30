# Nmap Network Scan Detection and IP Block Automation

## Detection Engineering
Detects potential reconnaissance by identifying Source IPs making connections to more than 30 distinct Destination IPs using Sysmon Event ID 3.

## Threat Hunting Process
- **Tactic:** Reconnaissance (TA0043)
- **Technique:** Network Service Scanning (T1046)
- **Data Source:** Sysmon Event ID 3
- **Hypothesis:** Source IPs connecting to 30+ hosts within a short timeframe are likely scanning

## SOAR Automation
A Python script simulates sending a block command to a firewall or SOAR API.

## Testing with Kali Linux
To simulate the scan that triggers detection:
```bash
nmap -sT 192.168.1.100
