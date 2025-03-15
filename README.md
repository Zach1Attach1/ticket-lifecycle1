# osTicket: Ticket Lifecycle Examples

## Project Overview
This project demonstrates the complete lifecycle of support tickets in osTicket, from creation to resolution, showcasing how the help desk system works in a simulated environment.

## Environments and Technologies Used
- Microsoft Azure (Virtual Machine)
- Windows 10
- osTicket (Help Desk Ticketing System)

## Prerequisites
- osTicket fully installed and configured
- Agents, departments, SLAs, and help topics set up

## Ticket Lifecycle Demonstrations

### Ticket Example 1: Critical System Outage

#### 1. Ticket Creation (End-User Perspective)
- Accessed the end-user portal at http://localhost/osTicket/
- Created a ticket with the following details:
  - Topic: Business Critical Outage
  - Issue Summary: "Entire mobile/online banking system is down"
  - Details: "Customers are reporting they cannot access their accounts online or through the mobile app. This is affecting all users."

![Ticket Creation](https://i.imgur.com/7uZnYHf.png)

#### 2. Initial Ticket Properties (Help Desk Agent Perspective)
- Logged in as Agent John
- Observed the ticket's initial properties:
  - Default priority
  - Assigned to general department
  - No SLA assigned yet
  - Unassigned status

![Initial Properties](https://i.imgur.com/tbxRLnz.png)

#### 3. Ticket Triage
- Set the following properties to properly categorize the issue:
  - Severity: Sev-A (1 hour, 24/7)
  - Department: Online Banking
  - Assigned to Jane (SysAdmin)
- Added an internal note documenting the triage decision

![Ticket Triage](https://i.imgur.com/JqFhDQC.png)

#### 4. Testing Department Access Restrictions
- Logged out and logged back in as John
- Attempted to view the ticket (now unable to access due to department restrictions)
- Confirmed department-based access control is working correctly

#### 5. Ticket Resolution
- Logged in as Jane (SysAdmin)
- Added updates as the issue was investigated:
  - Internal note: "Investigating database connectivity issues"
  - Response to customer: "We are aware of the outage and working to resolve it"
  - Update: "Database server restarted, testing connectivity"
- Resolved the ticket with final response:
  - "The banking system has been restored. A database connection pool was exhausted and has been expanded to prevent future occurrences."
- Changed ticket status to "Resolved"

![Ticket Resolution](https://i.imgur.com/UCtXqCx.png)

### Ticket Example 2: Software Upgrade

#### 1. Ticket Creation
- Created a new ticket as end-user:
  - Topic: Personal Computer Issues
  - Issue: "Accounting department needs Adobe upgrade, broken"
  - Details: "The Adobe software in the accounting department is outdated and causing files to be unreadable."

#### 2. Ticket Triage
- Logged in as Agent John
- Set properties:
  - Severity: Sev-B (4 hours, 24/7)
  - Department: Support
  - Assigned to self (John)

#### 3. Ticket Resolution
- Added investigation notes
- Responded to customer with updates
- Documented solution implementation
- Closed ticket with resolution details

### Ticket Example 3: Hardware Issue

#### 1. Ticket Creation
- Created a new ticket as end-user:
  - Topic: Equipment Request
  - Issue: "CFO's laptop will no longer turn on"
  - Details: "CFO's laptop won't power on at all, even when plugged in."

#### 2. Ticket Triage
- Logged in as Agent John
- Set properties:
  - Severity: Sev-B (4 hours, 24/7)
  - Department: Support
  - Assigned to self (John)

#### 3. Ticket Resolution
- Documented troubleshooting steps
- Created equipment replacement request
- Updated ticket with resolution
- Closed ticket after confirming CFO received new laptop

### Department Escalation Demonstration

#### 1. Testing Department-Based Access
- Set all tickets to SysAdmins with Sev-A priority
- Observed that some tickets became inaccessible to certain agents
- Switched to admin panel to modify access rights
- Assigned view-access to SysAdmins department for testing purposes
- Confirmed ability to see but not modify escalated tickets

![Department Access Control](https://i.imgur.com/d8LVpVJ.png)

## Ticket Management Best Practices
- Created tickets for all support interactions, even quick fixes
- Used consistent documentation in ticket updates
- Leveraged internal notes for team communication
- Maintained appropriate SLA assignments
- Demonstrated proper ticket closure procedures

## Lessons Learned
- The importance of proper ticket categorization for response prioritization
- How access controls affect ticket visibility across departments
- The value of detailed documentation throughout the ticket lifecycle
- SLA impact on ticket handling and prioritization
- The different perspectives of end-users versus help desk agents
