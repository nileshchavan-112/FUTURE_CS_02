# FUTURE_CS_02
Incident Response Summary

Name: Nilesh KisanChavan

Date: 23 Aug 2025

Title: Multiple Security Alerts Detected Through Splunk

Key Findings:

Multiple failed login attempts for users (alice, bob, charlie, david) from various IPs (public and private).

IP 203.0.113.77 and 172.16.0.3 have the highest number of suspicious activities (60 and 48 events).

Multiple malware types detected: Ransomware, Rootkit, Spyware, Trojan, Worm.

Users (charlie, david, bob) showing high connection attempts from IPs including suspicious ones (192.168.1.101, 203.0.113.77, 10.0.0.5).


Risk Assessment:

High Risk

Malware infections (Ransomware, Rootkits) → Potential data exfiltration, encryption, or privilege escalation.

Multiple failed logins & brute-force attempts → Risk of account compromise.

Suspicious IPs accessing multiple accounts → Strong indication of attacker pivoting.

Medium Risk

Internal IPs involved (10.0.0.5, 172.16.0.3, 192.168.1.101) suggest possible infected insider systems.

High connection attempts → Possible reconnaissance or lateral movement.

Low Risk

Some login failures may be legitimate user errors, but given correlation with malware and suspicious IPs, they cannot be ignored.


Recommendations:

Block suspicious IPs: 203.0.113.77, 198.51.100.42, 172.16.0.3, 10.0.0.5, 192.168.1.101.

Isolate infected machines (bob’s, alice’s, eve’s, charlie’s, david’s devices).

Disable compromised accounts until verified.
Run full malware scans and forensic investigation on infected hosts.

Patch systems, update antivirus/EDR signatures.

Restore from clean backups if ransomware/rootkit persists.

Conclusion: Immediate remediation is needed to contain threats and secure infrastructure.
