# AWS CloudWatch Alarms – EC2 Instance Monitoring

## Overview
This project demonstrates how to monitor the health and performance of an Amazon EC2 instance using **Amazon CloudWatch alarms**.  
The goal is to track instance status and CPU utilization and get alerted when thresholds are crossed.

## AWS Services Used
- Amazon EC2
- Amazon CloudWatch
- (Optional) Amazon SNS

## Project Implementation

### EC2 Instance
- Launched an EC2 instance for monitoring purposes
- No SSH access or key pair was required

### CloudWatch Alarms

#### CPU Utilization Alarm
- Metric: CPUUtilization
- Statistic: Average
- Threshold: CPU usage ≥ 70%
- Evaluation period: 5 minutes
- Alarm name: EC2-High-CPU-Alarm

#### Instance Health Alarm
- Metric: StatusCheckFailed
- Monitors both system and instance status checks
- Threshold: StatusCheckFailed ≥ 1
- Alarm name: EC2-Instance-Health-Alarm

### Alarm State
- Alarms are currently in **OK** state
- Indicates the instance is healthy and operating normally

## Monitoring & Alerts
- CloudWatch continuously monitors EC2 metrics
- Alarms trigger when defined thresholds are breached
- SNS notifications can be configured for email alerts (optional)

## Screenshots
Screenshots included in the repository show:
- Alarm list with OK state
- Alarm configuration details
- Metric graphs for CPU utilization and instance health

## Key Learnings
- Understanding CloudWatch metrics and alarms
- Monitoring EC2 performance and availability
- Setting thresholds and evaluation periods
- Implementing basic cloud monitoring best practices

## Notes
- EC2 instance can be safely stopped after alarm creation
- CloudWatch alarms do not incur additional cost
