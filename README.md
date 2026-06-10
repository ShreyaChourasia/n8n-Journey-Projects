# n8n-Journey-Projects
This contains my journey of learning and making projects on n8n
cat > README.md << 'EOF'
# n8n Form-to-Email Automation Workflow

An automated workflow built with [n8n](https://n8n.io/) that captures form submissions, stores them in Google Sheets, filters and routes based on occupation, and sends personalized emails via Gmail.

## Workflow Overview

![Workflow Screenshot](./images/workflow-overview.png)

### Pipeline

1. **On Form Submission** — User submits First Name, Last Name, Email, and Occupation.
2. **Append to Google Sheet** — Data is stored in a connected Google Sheet.
3. **Filter** — Filters out entries where Occupation is "Student".
4. **Switch** — Routes based on occupation (Engineer / Doctor).
5. **Send Emails** — Sends occupation-specific emails via Gmail.
6. **Merge** — Combines outputs from both branches.
7. **Final Email** — Sends a confirmation email.

## Screenshots

### Switch Node — Routing Rules
![Switch Node](./images/switch-node.png)

### Filter Node
![Filter Node](./images/filter-node.png)

### Gmail — Engineer Branch
![Gmail Engineer](./images/gmail-engineer.png)

### Gmail — Doctor Branch
![Gmail Doctor](./images/gmail-doctor.png)

### Final Gmail Node
![Gmail Final](./images/gmail-final.png)

### Emails Received Successfully
![Emails Received](./images/email-received.png)

## Setup Instructions

1. Install n8n locally or use Docker
2. Import `workflow/form-to-email-workflow.json` into n8n
3. Create a Google Cloud project and enable Google Sheets API, Google Drive API, and Gmail API
4. Create OAuth 2.0 credentials (Web application type) and configure them in n8n
5. Activate the workflow and test

## Tech Stack

- **n8n** — Workflow automation
- **Google Sheets API** — Data storage
- **Gmail API** — Email delivery
- **Google Cloud Console** — OAuth 2.0 authentication

## Author

**Shreya Chourasia**
EOF
