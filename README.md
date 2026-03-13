# SOC Detection Engineering Lab

A cybersecurity detection engineering project that demonstrates how Security Operations Center (SOC) teams detect attacker activity using Sigma rules, log analysis, and SIEM queries.

## Project Overview

This project simulates real-world security monitoring performed by SOC analysts. It includes detection rules for common attacker techniques such as brute force attacks, credential dumping, suspicious PowerShell execution, and lateral movement.

Detection rules are written using **Sigma** and mapped to the **MITRE ATT&CK framework**. The rules are converted into SIEM queries to demonstrate how they would be deployed in security monitoring platforms.

## Technologies Used

* Sigma (Detection Rule Format)
* Splunk Query Conversion
* Bash (Attack Simulation Scripts)
* Log Analysis
* MITRE ATT&CK Framework

---

## Detection Rules Implemented

| Detection Rule                  | Description                                    |
| ------------------------------- | ---------------------------------------------- |
| Brute Force Login Detection     | Detects repeated failed login attempts         |
| Suspicious PowerShell Execution | Detects encoded PowerShell commands            |
| Credential Dumping Detection    | Detects access to LSASS process memory         |
| Admin Account Creation          | Detects creation of new administrator accounts |
| Suspicious RDP Login            | Detects remote desktop logins                  |
| Scheduled Task Persistence      | Detects scheduled task creation                |
| Pass-the-Hash Detection         | Detects NTLM authentication anomalies          |
| SMB Lateral Movement            | Detects suspicious SMB connections             |

---

## MITRE ATT&CK Mapping

| Technique             | MITRE ID | Description                           |
| --------------------- | -------- | ------------------------------------- |
| Brute Force           | T1110    | Password guessing attacks             |
| PowerShell Execution  | T1059    | Command execution through scripting   |
| Credential Dumping    | T1003    | Extraction of credentials from memory |
| Create Account        | T1136    | Creation of new user accounts         |
| Remote Services (RDP) | T1021    | Remote access for lateral movement    |
| Scheduled Task        | T1053    | Persistence using scheduled tasks     |
| Pass-the-Hash         | T1550    | Authentication using password hashes  |
| Lateral Movement      | T1021    | Movement between systems              |

---

## Project Structure

```
SOC-Detection-Rules
│
├── sigma_rules
│   ├── bruteforce_login.yml
│   ├── suspicious_powershell.yml
│   ├── credential_dumping_lsass.yml
│   ├── admin_account_creation.yml
│   ├── suspicious_rdp_login.yml
│   ├── scheduled_task_persistence.yml
│   ├── pass_the_hash.yml
│   └── lateral_movement_smb.yml
│
├── logs
│   ├── bruteforce_log.txt
│   ├── powershell_attack_log.txt
│   └── credential_dumping_log.txt
│
├── queries
│
├── mitre_mapping
│
└── lab
    ├── simulate_attacks.sh
    └── detect_attacks.sh
```

---

## Attack Simulation Lab

A small SOC lab environment is included in the project. It simulates attacker behavior by generating log events that trigger the detection rules.

Example simulations:

* Brute force login attempts
* Suspicious PowerShell execution
* Credential dumping attempts

---

## Example Detection Workflow

1. Attack simulation generates log events
2. Logs are analyzed by detection scripts
3. Sigma rules identify suspicious patterns
4. Rules are converted into SIEM queries
5. Alerts can be generated for SOC analysts

---

## Learning Outcomes

Through this project, the following cybersecurity concepts were explored:

* Detection Engineering
* Log Analysis
* SOC Monitoring Workflows
* Threat Detection Techniques
* MITRE ATT&CK Mapping
* SIEM Query Generation

---

## Future Improvements

* Integration with real SIEM platforms
* Automated alerting system
* More MITRE ATT&CK detection rules
* Integration with threat intelligence feeds

---

## Author

Aryan Yadav
Cybersecurity Enthusiast | SOC Analyst Aspirant
