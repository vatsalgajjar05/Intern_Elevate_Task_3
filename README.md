# Task 3 — Basic Vulnerability Scan Using Nessus Essentials

This repository contains the vulnerability scan I performed on my local PC using **Nessus Essentials**, as required in Task 3.  
All steps, findings, screenshots, and analysis are included below.

---

## 🔧 Tool Used
- **Nessus Essentials** (Free vulnerability scanner)

---

## 📝 Steps Performed

### 1. Installed Nessus Essentials
- Downloaded from Tenable’s official site.
- Installed and activated with free activation code.
- Allowed Nessus through Windows Firewall.
- Waited for plugin initialization (10–20 minutes).

### 2. Set Up Scan Target
- Created a new scan: **Basic Network Scan**
- Target used:

127.0.0.1 (localhost)
or
My PC’s local IP (from ipconfig)

- Named the scan **“My PC Scan”** (as visible in screenshot).

### 3. Ran the Full Vulnerability Scan
- Started the scan from the Nessus dashboard.
- The scan ran for several minutes.
- Nessus checked open ports, SMB services, Windows configuration, and local network exposure.

### 4. Reviewed Scan Results
Based on the screenshot, the scan found:

### ✔ **3 Vulnerabilities (Severity: Info Only)**

| Severity | Name                         | Category         | Count |
|----------|------------------------------|------------------|-------|
| Info     | SMB (Multiple Issues)        | Windows          | 4     |
| Info     | Netstat Portscanner (SSH)    | Port Scanners    | 42    |
| Info     | DCE Services Enumeration     | Windows          | 8     |

📌 **Important Note:**  
Your scan **did not find any Critical, High, Medium, or Low vulnerabilities** — everything falls under *Informational*, meaning no security risk was flagged.

---

## 🖼 Screenshots (Evidence)
Included screenshot:  
- `scan-results.png` → Vulnerability report with findings and severity chart.

(Place your actual screenshot inside a `/screenshots` folder.)

---

## 🧐 Understanding the Findings

### 1. SMB (Multiple Issues) — *Info*
SMB services were detected on your system.  
This is normal in Windows unless there are high-severity SMB vulnerabilities, which Nessus did **not** detect.

### 2. Netstat Portscanner (SSH) — *Info*
Nessus found that SSH port scanning behavior was visible.  
This typically means:
- Nessus scanned your SSH/port activity
- No vulnerabilities were found, only enumeration

### 3. DCE Services Enumeration — *Info*
Nessus identified Microsoft RPC/DCE services.  
These are normal Windows components and not a threat unless misconfigured.

---

## 🔐 Mitigation (Since No Critical/High Issues Found)
Even though only “Info” items appeared, these best practices improve security:

- Keep Windows updated (Windows Update)
- Disable unused network services (e.g., SMBv1)
- Use strong passwords
- Enable firewall protection
- Disable unnecessary ports/services

---


---

## ✅ Conclusion
The vulnerability scan completed successfully using Nessus Essentials.  
Based on the results:

- **0 Critical**
- **0 High**
- **0 Medium**
- **0 Low**
- **3 Info-level findings**

Your system does not have any harmful vulnerabilities according to this scan.



