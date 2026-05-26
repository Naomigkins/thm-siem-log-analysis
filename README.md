# thm-siem-log-analysis
Hands-on Blue Team labs focusing on SOC workflows, multi-source SIEM log analysis, and incident triage across Windows, Linux, and Web application telemetry.

# TryHackMe: SOC Operations & SIEM Log Analysis 🚀

A public repository documenting hands-on Blue Team lab exercises from the TryHackMe SOC Level 1 path. This project demonstrates foundational capabilities in utilizing Security Information and Event Management (SIEM) architectures to centralize multi-source telemetry, parse raw security logs, correlate alerts, and reconstruct complex adversary attack timelines.

## 🎯 Strategic Benefits of SIEM in a SOC
In modern Security Operations Centers (SOC), managing separate log sources creates visibility silos. Implementing a central SIEM solution provides three primary enterprise advantages:
* **Centralized Log Ingestion:** Consolidates telemetry from disparate hosts, endpoints, firewalls, and cloud applications into a single searchable platform (e.g., Splunk / ELK).
* **Event Correlation:** Links independent events—such as an isolated anomalous IP discovery and a sudden local user credential change—to identify coordinated network compromises.
* **Historical Investigation & Auditing:** Allows security analysts to conduct retrospectives on past log data to discover advanced persistent threats (APTs) that initially bypassed active alerts.

---

## 💻 Technical Log Analysis Framework

### 1. Windows Logs & Endpoint Visibility
* **Data Sources Analyzed:** `WinEventLog` (Security, System, Application channels) and `Sysmon` (System Monitor).
* **Analysis Focus:** Evaluated the combination of native Windows logs and Sysmon telemetry to trace malicious local persistence mechanics.
* **Key Tasks:** Investigated the creation of unauthorized scheduled tasks (e.g., `Office365 Install`) and tracked administrative service manipulation.

### 2. Linux Logs & Privilege Escalation
* **Data Sources Analyzed:** `/var/log/auth.log` (authentication tracking) and `/var/log/syslog` (system-wide event messages).
* **Analysis Focus:** Mapped initial access vectors and host-centric privilege escalation patterns.
* **Key Tasks:** Triaged failed SSH password attempts, isolated successful remote logins by target users, tracked root privilege adjustments via `su` or `sudo`, and identified hidden command histories within `.bash_history`.

### 3. Web Application Logs & Traffic Spikes
* **Data Sources Analyzed:** Nginx and Apache Web Server logs (`access.log` and `error.log`).
* **Analysis Focus:** Triage of unexpected web app service alerts and traffic anomalies.
* **Key Tasks:** Parsed structured HTTP requests to differentiate legitimate user flows from malicious activities like automated reconnaissance, directory fuzzing, SQL Injection (SQLi), and Cross-Site Scripting (XSS) exploitation paths.

---

## 🛠️ Tools & Environments Used
* **SIEM Platforms:** Splunk / ELK Stack (Log query structuring, timeline analysis, and dashboard filtering)
* **Operating Systems:** Linux/Unix CLI, Kali Linux, Windows Enterprise
* **Lab Environments:** TryHackMe Interactive Attack Box & uCertify Security Environments

---

## 📑 Core Professional Competencies Demonstrated
* Deep understanding of Blue Team operational hierarchies and strict chain-of-command reporting.
* Proficiency in mapping raw, multi-source logs to established security attack frameworks.
* Ability to reduce organizational incident response times by executing rapid, root-cause diagnostics on ingestion anomalies.

---
*Note: This repository contains lab documentation and structured analysis framework write-ups aligned with the TryHackMe SOC Level 1 program to showcase enterprise threat hunting readiness.*
