# Cyber Security Internship - Task 1: Scan Your Local Network for Open Ports

## Objective
Discover open ports and active devices on the local network using Nmap/Zenmap to understand network exposure and service reconnaissance[cite: 1].

## Tools Used
* **Nmap / Zenmap:** Used for network discovery and executing a TCP SYN scan (`-sS`) across the local subnet (`192.168.x.x`)[cite: 1].

## Execution Steps
1. Identified local network range via configuration settings (`192.168.x.x`)[cite: 1].
2. Executed the Nmap scan command: `nmap -sS -o scan_test.txt 192.168.x.x`[cite: 6].
3. Discovered **3 active hosts** on the network[cite: 6]:
   - **Router (`192.168.x.x`):** Port 53 (DNS), Port 80 (HTTP), Port 49152 (UPnP)[cite: 6].
   - **Secondary Host (`192.168.x.x`):** Firewall-protected (all ports filtered/no response)[cite: 6].
   - **Local Host / PC (`192.168.x.x`):** Ports 135, 139, 445 (SMB/NetBIOS file sharing), Ports 902, 912 (VMware services), Port 5432 (PostgreSQL database)[cite: 6].
4. Saved output logs into `scan_results.txt` for documentation[cite: 1].

## Visual Evidence
![Zenmap Scan Output](Screenshot%202026-11-05%20163014.png)

## Files Included
* `scan_results.txt` — Full scan output log containing discovered hosts, states, and open ports.
## Key Takeaways
* **Network Reconnaissance:** Learned how to map local subnet ranges and identify active devices using Nmap/Zenmap[cite: 1].
* **TCP SYN Scanning:** Understood how stealth port scanning (`-sS`) works by analyzing handshake states without fully establishing connections[cite: 1].
* **Service Exposure & Attack Surface:** Identified open ports and their corresponding services (such as DNS, HTTP, SMB, and PostgreSQL) to evaluate network exposure risks[cite: 1].
