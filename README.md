# Email Header Analysis & Phishing Investigation (SOC Case Study)

## Project Overview
This project documents a real-world style phishing email investigation conducted from a SOC L1 analyst perspective. The objective was to analyze a suspicious email, validate email authentication mechanisms, perform threat intelligence correlation, and document findings using SOC-standard incident reporting.

---

## Objectives
- Analyze raw email headers
- Validate SPF, DKIM, and DMARC authentication
- Trace email delivery path
- Perform domain and IP reputation analysis
- Identify phishing indicators
- Map attack to MITRE ATT&CK
- Document incident in a professional SOC report

---

## Tools & Platforms Used
- Google Admin Toolbox – Message Header Analyzer
- Yahoo Mail (Raw Header Extraction)
- WHOIS Lookup (GoDaddy)
- AbuseIPDB
- VirusTotal
- MITRE ATT&CK Framework

---

## Investigation Workflow

### Email Identification
- Suspicious email detected in spam folder
- Generic greeting and business lure observed
- Sender claimed to be an external supplier

### Header Analysis
- Extracted full raw headers
- Analyzed using Google Admin Toolbox
- Observed:
  - SPF: **None**
  - DKIM: **Pass**
  - DMARC: **Unknown**


---

### Email Path Analysis
- Traced email flow via Gmail infrastructure
- Identified sending IP: `209.85.219.66`
- Email originated from shared Google mail servers

---

### Domain Analysis
- Domain: `pbs.ac.th`
- WHOIS revealed long-standing academic domain
- DNS hosted via Cloudflare
- No direct malicious registration indicators


---

### IP Reputation Analysis
- AbuseIPDB:
  - Confidence of abuse: **73%**
  - Categories: Email spam, brute-force, port scanning
- VirusTotal:
  - Infrastructure shared with benign services
  - No direct malware hosting detected


---

## Indicators of Compromise (IOCs)

| Type        | Value |
|------------|------|
| Sender Email | pbs17192@pbs.ac.th |
| Reply-To    | elianareese1@outlook.com |
| IP Address  | 209.85.219.66 |
| Domain      | pbs.ac.th |

---

## MITRE ATT&CK Mapping
- **T1566** – Phishing
- **T1204** – User Execution

---

## Final Verdict
- **Severity:** Medium
- Email classified as phishing due to social engineering indicators, authentication weaknesses, and suspicious reply-to behavior.
- No user interaction observed.
- Incident contained at detection stage.

---

## Learning Outcome
This project strengthened hands-on skills in email header analysis, authentication validation, threat intelligence correlation, and SOC-style incident documentation.

---

## Full Incident Report
📎 Check out in Documents Section

---

## 👤 Author
**Shaiva Kumar**  
  
