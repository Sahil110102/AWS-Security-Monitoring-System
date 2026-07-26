# AWS Security Monitoring System

## Project Summary

This project is an AWS-based security monitoring system built to detect and alert on access to sensitive secrets stored in AWS Secrets Manager. The solution uses AWS CloudTrail to record secret access activity, CloudWatch Logs and metric filters to detect specific events, CloudWatch Alarms to trigger alerts, and Amazon SNS to send email notifications.

The goal of the project was to create a simple but effective security workflow that can help identify when a secret is accessed and notify the relevant person quickly. I also explored direct CloudTrail SNS notifications and compared them with the CloudWatch-based alerting approach to understand the difference between broad log delivery and targeted security alerts.

## Architecture

The system follows this flow:

**AWS Secrets Manager → AWS CloudTrail → Amazon CloudWatch Logs → CloudWatch Metric Filter → CloudWatch Alarm → Amazon SNS Email Alert**

## Key Features

* Secure storage of a dummy secret in AWS Secrets Manager
* CloudTrail logging for secret access events
* CloudWatch log integration for monitoring and filtering
* Metric filter for detecting `GetSecretValue` events
* Alarm creation for access detection
* SNS email notifications for real-time alerts
* Troubleshooting and validation of the full notification pipeline

## AWS Services Used

* AWS Secrets Manager
* AWS CloudTrail
* Amazon CloudWatch
* Amazon SNS
* Amazon S3
* AWS CloudShell / AWS CLI

## What I Learned

* How sensitive secrets can be stored and monitored securely in AWS
* How CloudTrail records access events and supports security auditing
* How CloudWatch metric filters and alarms can be used for event-based alerting
* How SNS subscriptions work for email notifications
* How to troubleshoot missing alerts across CloudTrail, CloudWatch, and SNS

## Project Outcome

This project successfully demonstrated how to build a cloud security monitoring system that detects access to a secret and sends notifications when suspicious activity occurs. It also showed the importance of testing, validation, and troubleshooting in real-world cloud security setups.
