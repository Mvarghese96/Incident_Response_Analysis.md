# Incident_Response_Analysis.md
# SOC Incident Response Investigation

**Incident ID:** SOC-2026-001  
**Incident Type:** Suspected Account Compromise  
**Affected Account:** ajones  
**Investigation Status:** Simulated Investigation Completed  
**Severity:** High (Training Assessment)

## 1. Executive Summary

Security monitoring identified 10 failed login attempts followed by one successful login from the same unfamiliar IP address, 198.51.100.45.

Following the successful login, an email-forwarding rule was created and a Finance mailbox message was accessed.

These activities suggest a possible brute-force attack followed by unauthorized account access.

## 2. Incident Timeline

| Time | Security Event |
|---|---|
| 09:05:02 | First failed login |
| 09:06:15 | Successful login |
| 09:06:40 | Email inbox opened |
| 09:07:18 | Email-forwarding rule created |
| 09:07:59 | Finance mailbox message accessed |
| 09:10:00 | Suspicious session remained active |

## 3. Evidence Collected

- **Affected Account:** ajones
- **Source IP:** 198.51.100.45
- **Failed Login Attempts:** 10
- **Successful Logins:** 1
- **Forwarding Destination:** archive@external.example
- **Suspicious Activity:** Email-forwarding rule created
- **Potential Data Exposure:** Finance mailbox accessed
- **Confirmed Data Exfiltration:** Not established

## 4. MITRE ATT&CK Mapping

| Technique ID | Technique | Evidence |
|---|---|---|
| T1110 | Brute Force | Repeated failed login attempts |
| T1114.003 | Email Forwarding Rule | Suspicious forwarding rule created |

These mappings indicate possible attacker behavior, not confirmed attribution.

## 5. Incident Assessment

The evidence suggests a possible account compromise.

The creation of an external email-forwarding rule raises concerns about unauthorized access and potential data exposure.

However, the available logs do not conclusively establish data theft.

## 6. Recommended Response Actions

1. Escalate to the incident response team.
2. Verify the login activity with the employee.
3. Revoke suspicious active sessions.
4. Reset compromised credentials if warranted.
5. Investigate and remove unauthorized forwarding rules.
6. Review mailbox audit logs for potential data exposure.
7. Continue monitoring suspicious activity.

## 7. Conclusion

This investigation demonstrates how authentication logs and mailbox activity can help identify possible account compromise.

Additional investigation would be required to confirm unauthorized access and determine the extent of any data exposure.

## 8. Supporting Evidence

- SOC_Incident_Alert_01.log
- SOC_Incident_Alert_02.log

**Disclaimer:** This project uses fictional security logs for educational purposes. No real systems were compromised or investigated.
