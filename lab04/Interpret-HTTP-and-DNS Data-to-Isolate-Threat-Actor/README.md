# Lab: Interpret HTTP and DNS Data to Isolate Threat Actor

## Objective
Detect and investigate an SQL injection attack and DNS-based exfiltration using Security Onion and Kibana.
Identify attacker IPs and exfiltration domain(s), decode stolen data (redacted), and practice forensic techniques.

## Steps Taken
1. Set Kibana timeframe to **June 2020**.
2. Filtered HTTP logs and searched for SQLi patterns.
3. Identified attacker `source.ip` and victim `destination.ip`.
4. Opened alert details / pcap to inspect injected SQL payloads.
5. Switched to DNS logs; filtered for long/high-entropy queries to `redacted-domain.example`.
6. Exported DNS queries to CSV, isolated hex strings, decoded locally, and redacted sensitive content.
7. Correlated HTTP and DNS timelines to confirm compromise → extraction → exfiltration.

## Skills Practiced
- Kibana queries & time-range analysis
- HTTP payload forensics and pcap validation
- DNS exfiltration detection and decoding
- IOC generation and timeline correlation

## Lessons Learned
- Sanitize inputs and use parameterized queries to prevent SQLi.
- Monitor DNS for long/high-entropy labels and unusual query patterns.
- Preserve evidence (pcaps/logs) before containment and remediation.
- Redact PII during analysis and follow disclosure/incident response policies.

## Disclaimer
This repository is for educational and portfolio purposes only.
It does not provide step-by-step attack instructions.
No official Cisco lab instructions or copyrighted material are included.
