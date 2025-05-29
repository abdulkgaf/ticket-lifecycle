# ticket-lifecycle
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.

# osTicket - Ticket Lifecycle: Intake Through Resolution

This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.

## Environments and Technologies Used
* Microsoft Azure (Virtual Machines/Compute)
* Remote Desktop
* Internet Information Services (IIS)

## Operating Systems Used
* Windows 10 (21H2)

## Ticket Lifecycle Stages
* Intake
* Assignment and Communication
* Working the Issue
* Resolution

## Lifecycle Stages

![Screenshot 2025-05-28 111841](https://github.com/user-attachments/assets/e2a50bf2-118b-436a-9cf7-c13d383e22d4)

### Stage 1: Ticket Intake

#### Scenario 1: Business Critical Outage
**End User Creates Ticket:**
- Navigate to: http://localhost/osTicket/
- Click "Open a New Ticket"
- Fill out ticket form:
  - Email Address: karen@osticket.com
  - Full Name: Karen Karen
  - Help Topic: Business Critical Outage
  - Issue Summary: "Entire mobile/online banking system is down"
  - Details: "Customers are calling saying they are getting a 404 error when logging into online banking. Mobile app is also not working."
- Click "Create Ticket"
- Note the ticket number generated (e.g., #123456)

![Screenshot 2025-05-28 112345](https://github.com/user-attachments/assets/7ddf4732-555d-40c3-b8aa-06bacd3063de)

#### Scenario 2: Adobe Reader Request
**End User Creates Ticket:**
- Navigate to: http://localhost/osTicket/
- Click "Open a New Ticket"
- Fill out ticket form:
  - Email Address: ken@osticket.com
  - Full Name: Ken Ken
  - Help Topic: Equipment Request
  - Issue Summary: "Adobe Reader not working"
  - Details: "I need Adobe Reader installed on my computer to open PDF files for work."
- Click "Create Ticket"

#### Scenario 3: Password Reset Request
**End User Creates Ticket:**
- Create another ticket:
  - Email Address: karen@osticket.com
  - Help Topic: Password Reset
  - Issue Summary: "Locked out of accounting software"
  - Details: "I forgot my password for QuickBooks and now I'm locked out. Need access ASAP for month-end reporting."
- Click "Create Ticket"

![Screenshot 2025-05-28 112150](https://github.com/user-attachments/assets/5cf85621-429c-4895-8322-006ba16556d5)

### Stage 2: Assignment and Communication

#### Agent Reviews and Assigns Tickets
**Log into Agent Panel:**
- Navigate to: http://localhost/osTicket/scp/
- Log in as jane.doe (System Administrator agent)
- View ticket queue and observe:
  - Banking outage ticket assigned to System Administrators (SEV-A priority)
  - Adobe Reader ticket assigned to System Administrators (SEV-B priority)
  - Password reset ticket assigned to Support department (SEV-B priority)

#### Ticket Triage and Priority Assessment
**Banking Outage Ticket (Critical):**
- Click on the banking outage ticket
- Review details and assess impact
- Change priority to "Emergency" if not already set
- Change SLA Plan to SEV-A if needed
- Add internal note: "This affects all customers - escalating immediately"
- Assign to senior technician or escalate to Level II Support team

**Adobe Reader Ticket (Normal Priority):**
- Click on Adobe Reader ticket
- Review request details
- Set priority to "Normal"
- Assign to appropriate agent (john.doe from Level I Support)
- Add internal note: "Standard software installation request"

### Stage 3: Working the Issue

#### Resolving the Banking Outage (High Priority)
**Agent Communication and Troubleshooting:**
- Click on banking outage ticket
- Post reply to user:
  - "We have received your report and are investigating the online banking outage immediately. Our system administrators are working on this critical issue. We will provide updates every 30 minutes until resolved."
- Change status to "Open" and assign to yourself
- Add internal note documenting troubleshooting steps:
  - "Checked server status - web servers responding normally"
  - "Database connectivity confirmed"
  - "Issue identified: Load balancer configuration error after recent update"
  - "Implementing fix now"

**Progress Updates:**
- Add another reply to user:
  - "UPDATE: We have identified the issue as a configuration problem with our load balancer. Fix is being implemented now. Estimated resolution: 15 minutes."
- Continue documenting internal notes with technical details

#### Resolving Adobe Reader Request (Standard Process)
**Agent john.doe handles the request:**
- Log in as john.doe
- Click on Adobe Reader ticket
- Post reply to user:
  - "Hello Ken, I can help you install Adobe Reader. I will need to remote into your computer to complete the installation. Are you available now, and what is your computer name/IP address?"
- Wait for user response (simulate by adding another reply)
- User responds: "Yes, I'm available. Computer name is KEN-PC"
- Agent responds: "Perfect, I'm connecting now via remote desktop. The installation should take about 10 minutes."

**Resolution Process:**
- Add internal note: "Connected to KEN-PC via RDP, downloading Adobe Reader DC"
- Add another note: "Installation completed successfully, tested PDF opening functionality"
- Post final reply to user: "Adobe Reader has been successfully installed on your computer. You should now be able to open PDF files. Please test and let me know if you encounter any issues."

#### Working the Password Reset
**Agent handles password reset:**
- Click on password reset ticket
- Reply to user: "I can help you reset your QuickBooks password. For security purposes, I'll need to verify your identity. Can you please provide your employee ID and the last 4 digits of your phone number on file?"
- User provides verification details
- Internal note: "Identity verified, proceeding with password reset"
- Reply to user: "Identity confirmed. I'm resetting your QuickBooks password now. You will receive an email with your temporary password within 5 minutes."

### Stage 4: Resolution

#### Closing the Banking Outage Ticket
**Final Resolution:**
- Add final reply to banking outage ticket:
  - "RESOLVED: The online banking system has been fully restored. The issue was caused by a load balancer configuration error which has been corrected. All systems are now functioning normally. We apologize for the inconvenience and have implemented additional monitoring to prevent similar issues."
- Change ticket status to "Resolved"
- Add internal note: "Implemented additional load balancer monitoring alerts"
- Set resolution reason: "Configuration Error - Fixed"
- Click "Update Ticket"

#### Closing the Adobe Reader Ticket
**Confirmation and Closure:**
- Wait for user confirmation (simulate user reply): "Thank you! Adobe Reader is working perfectly now."
- Agent final reply: "Great! I'm glad Adobe Reader is working for you. This ticket is now resolved. Please don't hesitate to contact us if you need any further assistance."
- Change status to "Resolved"
- Resolution reason: "Software Installed Successfully"
- Click "Update Ticket"

#### Closing the Password Reset Ticket
**Final Steps:**
- User confirms: "Got the email and successfully logged into QuickBooks. Thank you!"
- Agent reply: "Excellent! Please remember to change your temporary password to something secure that you'll remember. This ticket is now resolved."
- Change status to "Resolved"
- Resolution reason: "Password Reset Completed"
- Add internal note: "User successfully accessed QuickBooks with new credentials"
- Click "Update Ticket"

### Ticket Lifecycle Analytics

#### Review Completed Tickets
**Generate Reports:**
- Navigate to Admin Panel → Dashboard
- Review ticket statistics:
  - Total tickets created: 3
  - Resolved tickets: 3
  - Average resolution time by priority
  - Agent performance metrics

#### SLA Compliance Check
**Verify SLA Adherence:**
- Banking outage (SEV-A): Resolved within 1 hour ✓
- Adobe Reader (SEV-B): Resolved within 4 hours ✓
- Password reset (SEV-B): Resolved within 4 hours ✓

#### Knowledge Base Updates
**Document Solutions:**
- Create knowledge base articles for common issues:
  - "How to Install Adobe Reader"
  - "Password Reset Procedures"
  - "Load Balancer Troubleshooting Steps"

## Lifecycle Complete!

This demonstration shows the complete ticket lifecycle in osTicket:

**Key Processes Demonstrated:**
- **Intake**: Multiple ticket types with different priorities
- **Assignment**: Automatic routing based on help topics and manual assignment
- **Communication**: Professional customer communication and internal documentation
- **Resolution**: Systematic problem-solving with proper closure procedures
- **Reporting**: SLA compliance tracking and performance metrics

The system effectively manages tickets from creation through resolution while maintaining professional communication, proper documentation, and adherence to service level agreements.
