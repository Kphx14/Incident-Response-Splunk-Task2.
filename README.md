# 🔍 Incident Response Report – Task FUTURE_CS_02

## 🛠 Tool: Splunk 9.4.3  
👨‍💻 Performed by: Kunal Phadtare  
📅 Date: 20 July 2025

---

## 🧾 Objective
Monitor simulated security alerts using **Splunk**, detect suspicious activities, classify incidents, and document a professional incident response report.

---

## 📘 Summary of Activity
1. **Log File Monitored**: `SOC_Task2_Sample_Logs.txt`  
2. **Source Type**: Custom source type `task2` configured  
3. **Searches**:
   - General logs:  
     `source="SOC_Task2_Sample_Logs.txt" sourcetype="task2"`
   - Internal errors:  
     `index=_internal "error" NOT debug source=*splunkd.log*`

---

## 🛑 Detected Suspicious Activities

| Timestamp       | User    | IP Address     | Action             | Threat/Notes                  |
|----------------|---------|----------------|--------------------|-------------------------------|
| 2025-07-03 06:13 | charlie | 10.0.0.5       | connection attempt | Unusual login time            |
| 2025-07-03 05:04 | bob     | 192.168.1.101  | login success      | Off-hour login                |
| 2025-07-03 04:27 | david   | 172.16.0.3     | login success      | Odd hour access               |
| 2025-07-03 05:48 | bob     | 10.0.0.5       | malware detected   | **Trojan Detected**           |
| 2025-07-03 09:10 | bob     | 172.16.0.3     | malware detected   | **Ransomware Behavior**       |
| 2025-07-03 09:24 | david   | 203.0.113.77   | login failed       | Repeated login failures       |

---

## 🚨 Event Classification
- **Critical Incidents**:
  - Ransomware and Trojan activity from user **bob**
- **Suspicious**:
  - Off-hour logins and failed attempts from **david**
- **Informational**:
  - Internal Splunk errors and legitimate connection attempts

---

## 📊 Visualization
- See screenshots in the `screenshots/` folder:
  - `splunk_log_monitoring.jpg`
  - `splunk_statistics.jpg`
  - `splunk_source_type.jpg`
  - `splunk_bar_chart.jpg`
  - `splunk_error_log.jpg`

---

## ✅ Response Actions
- Reviewed malware alerts
- Monitored internal error logs
- Flagged suspicious users/IPs for review

---

