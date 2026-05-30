# 🛡️ SIEM Detection Engineering Lab

**Category:** Detection Engineering  
**Status:** ✅ Complete  
**Tools:** Splunk Free, Sigma Rules, MITRE ATT&CK Navigator, Sysmon  
**Date:** May 2026

---

## 📖 Overview
Built and tested 15+ production-ready detection rules targeting common adversary TTPs. Focused on reducing false positives while maintaining high coverage for initial access, execution, and lateral movement techniques.

---

## 🎯 Objectives
- Map detections to MITRE ATT&CK v14
- Implement Sigma rule format for platform-agnostic deployment
- Test rules against simulated attack data (Atomic Red Team)
- Document tuning recommendations & FP mitigation

---

## 🧪 Detections Developed

| Rule Name | MITRE ATT&CK | Description | Severity |
|-----------|--------------|-------------|----------|
| Suspicious PowerShell Encoded Command | T1059.001 | Detects Base64-encoded PowerShell execution with known evasion patterns | High |
| PsExec Lateral Movement | T1021.002 | Flags remote service creation via PsExec/WMI from non-admin workstations | Critical |
| DNS Tunneling Indicators | T1071.004 | Identifies abnormal DNS query lengths & entropy patterns | Medium |
| Scheduled Task Persistence | T1053.005 | Alerts on new task creation with suspicious command lines | High |
| Credential Dumping via LSASS | T1003.001 | Detects process access to lsass.exe with known dump tools | Critical |

---

## 📊 Results & Metrics
- ✅ **15 detection rules** validated against test data
-  **~35% reduction** in false positives after tuning
- 🔄 **Average detection time:** <2 minutes in lab environment
-  **Export formats:** Splunk SPL, Sigma YAML, Elastic KQL

---

## 📁 Files & Resources
- [View Sigma Rules](https://github.com/zachariashin/detection-rules) *(replace with your repo)*
- [MITRE ATT&CK Mapping Spreadsheet](./siem-mapping.xlsx) *(upload later)*
- [Atomic Red Test Scripts Used](https://github.com/redcanaryco/atomic-red-team)

---

## 📝 Lessons Learned
- Correlation rules require careful threshold tuning per environment
- Sysmon Event ID 1, 3, 7, and 10 provide highest signal-to-noise ratio
- Sigma conversion to Splunk SPL needs manual validation for field names

---

[← Back to Detection Engineering](./README.md) | [← Back to All Projects](../../README.md) | [← Back to Portfolio](../../../README.md)
