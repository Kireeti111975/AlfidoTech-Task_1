# Active Reconnaissance and Vulnerability Assessment

## Overview

This repository contains the deliverables for an internship task focused on Active Reconnaissance and Vulnerability Assessment of an authorized web application. The objective was to identify exposed services, gather information about the target, perform vulnerability scanning, and document security findings using Kali Linux.

## Objective

- Perform active reconnaissance on the target web application.
- Identify open ports and running services.
- Conduct vulnerability assessment using industry-standard security tools.
- Analyze SSL/TLS configuration and HTTP security headers.
- Document findings and provide security recommendations.

## Target

**Authorized Test Target:**  
`https://interview-quiz-buddy.lovable.app`

---

## Tools Used

### Kali Linux
Primary operating system used for reconnaissance and vulnerability assessment.

### Nmap
Used for:
- Port Scanning
- Service Enumeration
- Version Detection
- Vulnerability Scanning (NSE Scripts)

Commands Used:

```bash
nmap interview-quiz-buddy.lovable.app
nmap -sV interview-quiz-buddy.lovable.app
sudo nmap -A interview-quiz-buddy.lovable.app
nmap --script vuln interview-quiz-buddy.lovable.app
```

### Nikto
Used for:
- Web Server Vulnerability Assessment
- Security Misconfiguration Detection
- Information Disclosure Checks

Command Used:

```bash
nikto -h https://interview-quiz-buddy.lovable.app
```

### SSLScan
Used for:
- SSL/TLS Configuration Analysis
- Cipher Suite Enumeration
- Certificate Validation

Command Used:

```bash
sslscan interview-quiz-buddy.lovable.app
```

### DNS Utilities
Used for domain and DNS information gathering.

Commands Used:

```bash
nslookup interview-quiz-buddy.lovable.app
host interview-quiz-buddy.lovable.app
```

### cURL
Used for HTTP response and security header analysis.

Command Used:

```bash
curl -I https://interview-quiz-buddy.lovable.app
```

---

## Methodology

### 1. Information Gathering
- DNS Enumeration
- Host Resolution
- Target Identification

### 2. Port Scanning
- Discovery of open ports
- Service identification

### 3. Service Enumeration
- Detection of running services
- Version identification

### 4. Vulnerability Assessment
- Nmap NSE vulnerability scanning
- Nikto web vulnerability scanning

### 5. SSL/TLS Analysis
- Certificate inspection
- Protocol and cipher analysis

### 6. Security Header Analysis
- Evaluation of HTTP security headers
- Identification of missing security controls

---

## Repository Structure

```text
├── screenshots/
│   ├── dns_lookup.png
│   ├── host_lookup.png
│   ├── nmap_basic.png
│   ├── nmap_services.png
│   ├── nmap_aggressive.png
│   ├── nmap_vuln.png
│   ├── nikto_scan.png
│   ├── sslscan.png
│   └── security_headers.png
│
├── reports/
│   ├── nslookup.txt
│   ├── host.txt
│   ├── nmap_basic.txt
│   ├── nmap_services.txt
│   ├── nmap_aggressive.txt
│   ├── nmap_vuln.txt
│   ├── nikto_report.txt
│   ├── sslscan_report.txt
│   └── security_headers.txt
│
└── Vulnerability_Assessment_Report.pdf
```

---

## Deliverables

- Scan Result Screenshots
- Raw Scan Output Files
- Vulnerability Assessment Report
- Security Recommendations

---

## Key Learning Outcomes

- Active Reconnaissance Techniques
- Network Service Enumeration
- Vulnerability Assessment Methodology
- SSL/TLS Security Analysis
- Security Header Evaluation
- Technical Documentation and Reporting

---

## Disclaimer

This assessment was conducted solely for educational and internship purposes on an authorized target. No exploitation, unauthorized access, or destructive testing was performed.
