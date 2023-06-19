## Postmortem: Incident Report - The JusticeGuard App Service Outage


![ALX postmortem](https://github.com/Victornwaonicha/alx-system_engineering-devops/assets/113601482/23cca1c1-2621-4c99-b66f-59d1fd0d60b6)

## Issue Summary:

Duration: June 15, 2023, 10:00 AM to June 15, 2023, 12:30 PM (UTC)
Impact: The JusticeGuard App experienced a complete outage during the specified timeframe. Users were unable to access the service, resulting in a 40% decrease in active users during the incident period.

## Timeline:

10:00 AM: The issue was detected when monitoring alerts indicated a sudden drop in service availability.
10:05 AM: The on-call engineer received the alert and initiated an investigation into the root cause of the issue.
10:15 AM: Initial assumption was that the issue was related to the database, so the database team was notified and joined the investigation.
10:30 AM: After analyzing the database logs, it was determined that the issue did not originate from the database.
10:45 AM: The investigation was escalated to the networking team as preliminary findings suggested a network connectivity problem.
11:00 AM: Network team identified a misconfiguration in the firewall rules that led to blocked incoming traffic, causing the service outage.
11:30 AM: The incident was resolved by updating the firewall rules to allow the necessary incoming traffic.
12:30 PM: Service availability was fully restored, and user access returned to normal.

## Root Cause and Resolution:

Root Cause: The root cause of the service outage was identified as a misconfiguration in the firewall rules, which resulted in blocking the incoming traffic necessary for service operation.

Resolution: The issue was resolved by updating the firewall rules to allow the required incoming traffic. Additionally, the team implemented a validation process to ensure proper configuration of firewall rules during future updates.

## Corrective and Preventative Measures:

Improvements/Fixes:
Enhance monitoring capabilities to proactively detect and alert for firewall misconfigurations.
Conduct regular firewall rule audits to identify and address potential misconfigurations.
Implement automated testing for firewall rules before deployment to production.

Tasks:
Patch the network firewall software to include automated validation of rule configurations.
Conduct a comprehensive review of all existing firewall rules to ensure accuracy and remove redundant or obsolete rules.
Develop and implement a recurring training program to educate the team on best practices for firewall rule management.

