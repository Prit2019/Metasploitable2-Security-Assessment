# Metasploitable 2 Vulnerability Assessment & Hardening Lab

## Objective
Perform a full vulnerability assessment against a deliberately vulnerable Linux system(Metasploitable 2), prioritize findings, remediate high-risk services, and verify risk reduction through rescanning.

## Environment
- Attacker: Kali Linux
- Target: Metasploitable 2
- Network: Host-only (VirtualBox)

## Methodology
1. Initial reconnaissance and full TCP port scan
2. Service enumeration and vulnerability identification
3. Risk-based prioritization of findings
4. Service hardening and attack surface reduction
5. Post-remediation validation scans
6. Evidence collection

## Key Findings  (Before Remediation)
- Multiple legacy services exposed (telnet, rsh, rlogin, rexec, FTP, bind shell)
- Weak SSH cryptographic algorithms
- Exposed Tomcat AJP and HTTP services
- Xinetd-managed insecure services
- High-risk backdoor shell (port 1524)

## Remediation Actions
- Disabled legacy remote access services via inetd/xinetd
- Removed unnecessary network daemons
- Stopped and disabled Tomcat and auxiliary Java services
- Reduced exposed ports to SSH and required management interfaces
- Verified services using ss and nmap rescans

## Validation
- Full port scan confirms significant attack surface reduction
- SSH service remains accessible for administration
- Evidence files included in /evidence

## Disclaimer
This lab was conducted in a controlled, offline environment for educational purposes only.
