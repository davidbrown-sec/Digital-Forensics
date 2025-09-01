# DFIR Foundations and Techniques  
## Security Operations in Enterprise Environments  

---

## Table of Contents  
- [Case Introduction](#case-introduction)  
- [Objectives](#objectives)  
- [Provided Evidence](#provided-evidence)  
- [PCAP Analysis](#pcap-analysis)  
  - [1. DNS Resolution](#1-dns-resolution)  
  - [2. Malicious HTTP Requests](#2-malicious-http-requests)  
  - [3. File Transfer Identified](#3-file-transfer-identified)  
  - [4. Malicious Script Analysis](#4-malicious-script-analysis)  
  - [5. Command and Control (C2) Activity](#5-command-and-control-c2-activity)  
  - [PCAP Findings](#pcap-findings)  
- [Disk Analysis](#disk-analysis)  
  - [General System Information](#1-general-system-information)  
  - [Evidence of File Download](#2-evidence-of-file-download)  
  - [Persistence Mechanisms](#3-persistence-mechanisms)  
  - [User Activity](#4-user-activity)  
  - [Disk Findings](#disk-findings)  
- [Memory Analysis](#memory-analysis)  
  - [Suspicious Processes](#1-suspicious-processes)  
  - [Network Connections in Memory](#2-network-connections-in-memory)  
  - [Loaded Modules and Scripts](#3-loaded-modules-and-scripts)  
  - [Memory Findings](#memory-findings)  
- [Timeline Analysis](#timeline-analysis)  
- [Indicators of Compromise (IOCs)](#indicators-of-compromise-iocs)  
- [Conclusion](#conclusion)  

---

## Case Introduction  
On **August 30, 2024, at 22:56:20 UTC**, the SOC detected that user **Alice** (host: `CLIENT2 – 192.168.0.104`) downloaded a suspicious file from: 
URL http[:]//w1ndowsupdate.com:8000/update.exe.hta onto her Windows workstation. 
As a result, an alert was triggered, prompting an incident response investigation to assess the situation
