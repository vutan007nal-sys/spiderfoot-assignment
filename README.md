# spiderfoot-assignment
# SpiderFoot – OSINT Assignment

## 1. Introduction

SpiderFoot is an open-source reconnaissance and OSINT (Open-Source Intelligence) automation tool. It helps security professionals collect publicly available information about domains, IP addresses, email addresses, usernames, and other targets.

SpiderFoot automates the information-gathering process by using different modules and public data sources.

**Purpose:**  
To understand SpiderFoot, install and use it for authorized OSINT reconnaissance, and document the collected information.

---

## 2. Objective

The objectives of this assignment are:

- To understand the concept of OSINT.
- To install and configure SpiderFoot.
- To perform an authorized reconnaissance scan.
- To understand SpiderFoot modules.
- To collect publicly available information about a target.
- To analyze the scan results.
- To save and document the results.
- To understand the security advantages and limitations of SpiderFoot.

---

## 3. Tool Information

### Tool Name

**SpiderFoot**

### Category

OSINT / Reconnaissance / Security Intelligence

### Platform

- Linux
- Windows
- macOS

### License

Open-source

---

## 4. Description

SpiderFoot is an automated OSINT reconnaissance framework designed to collect information from publicly available sources.

It can investigate:

- Domains
- IP addresses
- DNS information
- Email addresses
- Usernames
- Subdomains
- WHOIS information
- SSL certificates
- Public breach-related information
- Network information
- Search-engine results
- Publicly available threat intelligence

SpiderFoot uses modules to collect and correlate information from different sources.

---

# 5. Installation on Kali Linux

First, update the package repository:

```bash
sudo apt update
```

Install Git if required:

```bash
sudo apt install git -y
```

Clone the SpiderFoot repository:

```bash
git clone https://github.com/smicallef/spiderfoot.git
```

Move into the SpiderFoot directory:

```bash
cd spiderfoot
```

Install the required Python dependencies:

```bash
pip3 install -r requirements.txt
```

If Kali reports an externally-managed-environment error, use a Python virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

# 6. Starting SpiderFoot

Run:

```bash
python3 sf.py -l 127.0.0.1:5001
```

After starting successfully, open a browser and visit:

```text
http://127.0.0.1:5001
```

The SpiderFoot web interface should appear.

---

# 7. Creating a Scan

### Step 1

Open the SpiderFoot web interface.

### Step 2

Select **New Scan**.

### Step 3

Enter an authorized target.

For example, use a domain that you own or have explicit permission to test:

```text
example.com
```

### Step 4

Select an appropriate scan profile.

For an initial assignment, a passive or general OSINT scan is recommended.

### Step 5

Start the scan.

SpiderFoot will execute the selected modules and collect information from available sources.

---

# 8. Important SpiderFoot Modules

SpiderFoot contains many modules. Examples include:

| Module | Purpose |
|---|---|
| DNS | Collects DNS-related information |
| WHOIS | Retrieves domain registration information |
| Subdomain Enumeration | Identifies possible subdomains |
| SSL Certificate | Examines certificate information |
| Email | Identifies publicly available email information |
| Search Engine | Searches publicly indexed information |
| IP Address | Collects IP-related information |
| Username | Searches for usernames on supported services |
| Website | Collects information about websites |
| Threat Intelligence | Uses supported threat-intelligence sources |

The exact modules and data sources available can depend on the SpiderFoot version and configuration.

---

# 9. Information Collected

During an authorized scan, SpiderFoot may identify information such as:

### Domain Information

- Domain name
- DNS records
- Nameservers
- Related domains

### IP Information

- IP addresses
- Network ownership information
- Related hosts

### Subdomain Information

Example:

```text
www.example.com
mail.example.com
api.example.com
```

### Email Information

SpiderFoot may identify publicly exposed email addresses from supported sources.

### WHOIS Information

Possible information includes:

- Registrar
- Registration dates
- Nameservers
- Domain status

### Certificate Information

SpiderFoot can identify information from publicly available SSL/TLS certificates.

---

# 10. Example Scan Workflow

```text
Target
   ↓
SpiderFoot
   ↓
DNS Enumeration
   ↓
WHOIS
   ↓
Subdomain Discovery
   ↓
IP Information
   ↓
Search Engines
   ↓
Email/Username Discovery
   ↓
Correlation
   ↓
OSINT Results
```

---

# 11. Saving Scan Results

Create a directory for assignment results:

```bash
mkdir -p ~/spiderfoot-assignment/results
```

SpiderFoot results can also be exported through the web interface depending on the version and available export functionality.

Save screenshots in:

```text
~/spiderfoot-assignment/screenshots/
```

Create the directory:

```bash
mkdir -p ~/spiderfoot-assignment/screenshots
```

Recommended screenshots:

1. SpiderFoot installation
2. SpiderFoot running in terminal
3. SpiderFoot web interface
4. New Scan page
5. Target entered
6. Scan in progress
7. Scan results
8. Important discovered information
9. Graph/visualization if available
10. Exported results

---

# 12. Advantages of SpiderFoot

### 1. Automation

SpiderFoot automates many OSINT reconnaissance tasks.

### 2. Multiple Data Sources

It can use multiple public and configured data sources.

### 3. Modular Architecture

Different modules can perform different types of reconnaissance.

### 4. Web Interface

The graphical interface makes it easier to create and monitor scans.

### 5. Information Correlation

SpiderFoot can connect information collected from different sources.

### 6. Security Research

It can assist security professionals during authorized reconnaissance and attack-surface assessment.

### 7. Open Source

The project can be inspected and used as an open-source security tool.

---

# 13. Limitations

SpiderFoot also has limitations:

- Results depend on available public information.
- Some modules require API keys.
- Some data sources may have rate limits.
- Results may contain false positives.
- Public information can become outdated.
- Some sources may become unavailable.
- SpiderFoot should only be used against authorized targets.

---

# 14. Ethical and Legal Considerations

SpiderFoot should be used responsibly.

Only scan:

- Your own domains
- Your own systems
- Training/lab targets
- Targets for which you have explicit authorization

Do not use SpiderFoot to collect or investigate private information about people without a legitimate and authorized purpose.

OSINT tools should be used for defensive security, research, education, and authorized penetration testing.

---

# 15. Practical Result

### Target

```text
Authorized target: __________________
```

### Scan Date

```text
____________________
```

### Modules Used

```text
1. DNS
2. WHOIS
3. Subdomain Enumeration
4. IP Information
5. SSL Certificate
6. Search Engine
```

### Key Findings

```text
1. __________________________________
2. __________________________________
3. __________________________________
4. __________________________________
5. __________________________________
```

### Number of Results

```text
____________________
```

### Observation

SpiderFoot successfully automated the OSINT reconnaissance process and displayed information collected from the selected modules and configured data sources.

---

# 16. Conclusion

SpiderFoot is a useful OSINT and reconnaissance framework for security professionals. It simplifies the process of collecting and correlating publicly available information.

Through this assignment, I learned how to install SpiderFoot, configure a scan, select OSINT modules, analyze reconnaissance results, and document the findings.

SpiderFoot can be useful in cybersecurity activities such as attack-surface discovery, reconnaissance, threat intelligence, and security assessment when used with proper authorization.

---

# 17. References

1. SpiderFoot Official GitHub Repository  
   https://github.com/smicallef/spiderfoot

2. SpiderFoot Documentation  
   https://www.spiderfoot.net/

3. OWASP – Open Source Intelligence  
   https://owasp.org/

4. OSINT Framework  
   https://osintframework.com/

---

## Submission Checklist

- [ ] SpiderFoot installed
- [ ] Authorized target selected
- [ ] Scan completed
- [ ] Screenshots taken
- [ ] Results documented
- [ ] Advantages/features included
- [ ] Conclusion included
- [ ] References included
- [ ] Report reviewed before LinkedIn submission
