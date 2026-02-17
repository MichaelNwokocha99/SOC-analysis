# SOC-analysis
Enhancing Linux Server Security Using Wazuh
Netcat Detection and Malicious IP Blocking

Author: Michael Nwokocha
Date: April 2025

# 1. Introduction

This project focuses on improving the security posture of Linux systems by leveraging Wazuh, an open-source security monitoring platform.

The primary goal is to:

- Detect Netcat-based unauthorized access

- Automatically block malicious IP addresses

- Strengthen host-based intrusion detection (HIDS)

- Implement real-time monitoring with automated response

- By integrating Wazuh with firewall rules, this project demonstrates proactive defense against reverse shell attacks and suspicious network activity.

# 2. Objectives

- Detect and alert on suspicious Netcat activity in real time

- Identify and automatically block malicious IP addresses

- Strengthen the Host-Based Intrusion Detection System (HIDS)

- Demonstrate automation using custom rules and active response scripts

# 3. Tools and Technologies Used

- Operating System: Ubuntu 22.04 LTS

- Security Platform: Wazuh Manager & Agent

- Log Collection: Syslog, Auditd

- Network Tool (Attack Simulation): Netcat (nc)

- Firewall: UFW (Uncomplicated Firewall)

- Scripting Language: Bash

- SIEM Stack: Elasticsearch, Kibana (Wazuh Stack)

# 4. Methodology
# 4.1 Wazuh Installation and Configuration

- Installed Wazuh Manager on a central server

- Installed Wazuh Agent on a monitored Linux host

- Configured log collection from:

- System logs

- Network activity

- Auditd logs

# 4.2 Netcat Detection Setup

- Simulated reverse and bind shell attacks using Netcat

- Created custom decoders and rules in Wazuh

# Configured Wazuh to:

- Parse logs

- Recognize Netcat execution patterns

- Generate real-time alerts

# 4.3 Malicious IP Blocking

- Configured Wazuh Active Response

- Developed a custom Bash script triggered upon detection

- Script automatically adds attacker IP to UFW deny list

- sudo ufw deny <attacker_ip>

- Validated real-time blocking using simulated attacks

# 4.4 Testing and Validation

- Launched Netcat from external test machines

- Confirmed alert generation in Wazuh Dashboard

- Verified malicious IP was successfully blocked

- Tuned detection rules to reduce false positives

# 5. Results

✅ Netcat activity detected within 3–5 seconds

✅ Malicious IPs automatically blocked

✅ Alerts visualized clearly in Kibana dashboard

✅ False positives minimized through rule tuning

# 6. Challenges Faced

- Fine-tuning Wazuh rules required deep understanding of log formats

- Initial Wazuh agent connection failures due to:

- Firewall misconfiguration

- Incorrect manager IP/port settings

- Service timeout errors

- Some IP blocking actions required elevated permissions

- Encrypted Netcat traffic remains a detection limitation

# 7. Conclusion

- This project demonstrates the effectiveness of Wazuh in detecting Netcat-based attacks and automatically responding by blocking malicious IP addresses.

- Through real-time monitoring and automation, the system significantly enhances the security resilience of Linux servers and reduces response time to threats.

## 8. Future Work

- Integrate threat intelligence feeds for proactive IP blacklisting

- Expand detection to include additional reverse shell tools (e.g., ncat, socat)

- Explore machine learning–based anomaly detection

** Extend monitoring across multiple Linux servers

## Key Skills Demonstrated

- Linux Security Hardening

- Wazuh Rule Creation

- Active Response Configuration

- Firewall Automation (UFW)

- Threat Simulation & Validation

- SIEM Monitoring & Log Analysis

<br> [READ REPORT](https://drive.google.com/file/d/1lKti23hWyqXCxj3XzdkaybHV5cQhCcNu/view?usp=drive_link)
