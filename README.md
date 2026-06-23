Project Overview

This project demonstrates how to analyze DNS log files using Splunk SIEM to identify suspicious network behavior, detect anomalies, and investigate potentially malicious domains. The project covers the complete workflow from log ingestion and indexing to threat hunting and security monitoring using Splunk Search Processing Language (SPL).

Objectives
Ingest DNS log data into Splunk SIEM.
Extract and analyze DNS-related fields.
Identify abnormal DNS activity and traffic spikes.
Detect suspicious or malicious domains.
Gain hands-on experience with SIEM-based threat monitoring.
Features
DNS log ingestion and indexing.
Custom source type configuration.
DNS event searching and filtering.
Domain frequency analysis.
Top DNS source identification.
Suspicious domain investigation.
SPL-based security monitoring and reporting.
Technologies Used
Splunk Enterprise / Splunk SIEM
SPL (Search Processing Language)
DNS Log Data
Security Information and Event Management (SIEM)
Implementation Workflow
Download and prepare DNS log files.
Upload logs into Splunk using the Add Data feature.
Configure source type and indexing settings.
Verify successful log ingestion.
Perform DNS event searches using SPL queries.
Extract and analyze relevant DNS fields.
Identify traffic anomalies and unusual patterns.
Investigate suspicious domains using threat intelligence techniques.
Generate insights for security monitoring and incident response.
Key SPL Queries
Search DNS Events
index=* sourcetype=dns_sample
Extract DNS Related Events
index=* sourcetype=dns_sample | regex _raw="(?i)\b(dns|domain|query|response|port 53)\b"
Domain Frequency Analysis
index=* sourcetype=dns_sample | stats count by fqdn
Top DNS Sources
index=* sourcetype=dns_sample | top fqdn, src_ip
Investigate Suspicious Domains
index=* sourcetype=dns_sample fqdn="maliciousdomain.com"
Learning Outcomes
SIEM log management and monitoring.
DNS traffic analysis techniques.
Security event investigation.
Threat hunting using SPL queries.
Detection of suspicious network activities.
Future Enhancements
Integration with threat intelligence feeds.
Automated alert generation.
Real-time DNS anomaly detection dashboards.
Machine learning-based threat detection.
Advanced visualizations and reporting.
Conclusion

This project provides practical experience in DNS security monitoring using Splunk SIEM. By analyzing DNS logs and investigating anomalies, security analysts can proactively detect threats, improve visibility into network activity, and strengthen organizational cybersecurity defenses.
