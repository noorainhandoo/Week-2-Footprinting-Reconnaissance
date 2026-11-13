# Week 2 – Footprinting & Reconnaissance

**Cybersecurity Internship | Networkwalks**  
**Participant:** Noorain Handoo  
**Batch:** B084

This repository contains the Week 2 practical work on footprinting, reconnaissance and local network discovery.

## Project Overview

The practical exercises involved collecting publicly available domain information, checking DNS and HTTP details, identifying website technologies, attempting WAF fingerprinting, and scanning the local subnet for active hosts.

**Target domain:** `networkwalks.com`

## Tools Used

- WHOIS – domain registration information
- Nslookup – DNS lookup
- WhatWeb – website technology identification
- cURL – HTTP response/header inspection
- DNSRecon – DNS enumeration
- WAFW00F – web application firewall fingerprinting
- Zenmap/Nmap – local network host discovery

## Repository Structure

```text
Week-2-Footprinting-Reconnaissance/
├── Screenshots/
│   ├── PM1_01_WHOIS.png
│   ├── PM1_02_NSLOOKUP.png
│   ├── PM1_03_WHATWEB.png
│   ├── PM1_04_CURL_HEADERS.png
│   ├── PM1_05_WAFW00F.png
│   ├── PM1_06_DNSRECON.png
│   ├── PM5_01_ZENMAP_PING_SCAN.png
│   └── PM5_02_ZENMAP_NETWORK_TOPOLOGY.pdf
├── Outputs/
│   ├── whois_summary.txt
│   ├── nslookup.txt
│   ├── whatweb.txt
│   ├── curl_headers.txt
│   ├── wafw00f.txt
│   ├── dnsrecon.txt
│   ├── zenmap_ping_scan.txt
│   └── findings_summary.txt
├── Reports/
│   └── Noorain_Handoo_B084_Penetration_Testing_Report.pdf
└── README.md
```

## Key Observations

- The target domain resolved to `192.232.216.135`.
- WhatWeb identified Apache, WordPress 7.1.4, WP Download Manager 3.3.76 and jQuery 3.7.1.
- The cURL header request returned `HTTP 200 OK` and identified Apache.
- DNSRecon reported 8 records, including SOA, NS, MX, A, TXT and SRV record categories.
- WAFW00F timed out, so WAF identification remained inconclusive.
- The local subnet `192.168.29.0/24` was scanned using `nmap -sn`.
- The scan covered 256 IP addresses and reported 10 hosts up in 5.10 seconds.

## Outputs and Evidence

The `Screenshots` folder contains the captured practical evidence. The `Outputs` folder contains readable summaries of the observed command results. These text files are summaries, not fabricated verbatim terminal logs; refer to the screenshots for the original captured output.

The `Reports` folder contains the detailed PDF report.

## Disclaimer

This repository is intended for educational purposes as part of the Networkwalks cybersecurity internship. Scanning and reconnaissance should only be performed on systems and networks for which appropriate authorization has been obtained.
