🔐 Brute Force Attack Detection Using Windows Security Event Logs
📌 Project Overview

This project demonstrates the simulation and detection of an RDP brute force attack against a Windows 10 system. The attack was executed using Hydra from Kali Linux, and authentication events were analyzed through Windows Security Event Logs.

🖥 Lab Environment

Attacker: Kali Linux

Target: Windows 10

Service: RDP (TCP 3389)

Virtualization: VMware Workstation

Target IP: 192.168.240.128

Attacker IP: 192.168.240.129

⚔ Attack Simulation

Used Hydra for dictionary-based brute force attack.

Generated multiple failed login attempts (Event ID 4625).

Observed successful authentication (Event ID 4624).

Identified NTLM authentication (Logon Type 3).

🔍 Detection Logic

Alert if:

≥ 3 Event ID 4625 from same IP and same account

Within 60 seconds

Followed by Event ID 4624

🎯 MITRE ATT&CK Mapping

Technique: T1110 – Brute Force

Tactic: Credential Access
