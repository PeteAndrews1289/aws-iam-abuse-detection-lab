# AWS IAM Abuse Detection Lab

## Overview

This project focuses on AWS identity and access security by simulating IAM-related activity and analyzing it using CloudTrail and Splunk.

The goal is to understand how identity behavior appears in cloud logs and how it can be detected using SIEM tools.

This project complements a separate AWS infrastructure monitoring lab by focusing specifically on identity, privilege, and access control events.

---

## Project Goals

- Create a controlled AWS IAM lab environment
- Simulate identity-related activity including enumeration, role usage, and policy changes
- Generate CloudTrail logs reflecting real-world identity behavior
- Ingest logs into Splunk for analysis
- Build detection queries for IAM activity and misuse

---

## Architecture

- AWS IAM (Users, Roles, Policies)
- AWS CloudTrail (logging)
- AWS S3 (log storage)
- Splunk Enterprise (log ingestion and analysis)

---

## Key Activities Simulated

- IAM user creation and deletion
- IAM policy attachment and detachment
- Role assumption using AWS STS
- Identity and resource enumeration
- Failed API calls due to insufficient permissions

---

## Detection Capabilities

- Detection of IAM administrative actions (CreateUser, DeleteUser)
- Detection of role assumption activity (AssumeRole)
- Detection of failed or denied API calls
- Detection of identity enumeration behavior
- Analysis of identity activity across AWS services

---

## Result

Built a cloud identity security lab that demonstrates how IAM-related activity can be monitored and analyzed using CloudTrail and Splunk.

---

## Insight

Identity is one of the most critical security layers in AWS because it directly controls access to resources.

This project highlights how identity-related activity is distributed across multiple AWS services and how effective detection requires broad visibility across event sources.

---

## Screenshots

### IAM Setup
![IAM Setup](screenshots/aws/iam-user-created.png)

### Splunk Detection Example
![Splunk Detection](screenshots/splunk/assume-role.png)

---

## Future Improvements

- Automate log ingestion from S3 into Splunk
- Build real-time alerting for IAM misuse
- Add correlation rules across multiple event types
- Expand detection coverage to include additional AWS services
