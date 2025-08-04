# FUTURE_CS_02

## 🔍 Objective

To analyze simulated web server logs using Splunk SIEM and identify suspicious activities.

## 🛠 Tools Used

- Splunk Cloud (Free Trial)
- Sample Apache access logs

## 📊 Activities Performed

- Uploaded access log into Splunk
- Created queries to identify:
  - Multiple 401 Unauthorized attempts
  - SQL Injection patterns (`' OR '1'='1`)
  - Admin page hits

## 🔎 Sample Queries Used

```spl
source="sample_access.log" status=401
source="sample_access.log" uri="/admin"
source="sample_access.log" uri_query="*' OR '1'='1*"

