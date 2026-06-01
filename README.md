# Sale And Ticket Record

## Overview
This scheduled n8n workflow operates every Monday morning. It extracts all sales records and ticket records from Supabase databases, combines the data to build a weekly summary report, saves the analysis to Google Sheets, sends a wrap-up email, and posts the summary to Slack.

## Nodes Used
- **Schedule Trigger**: Fires every week on Monday at 8 AM.
- **Supabase (Multiple)**: Retrieves batches of both Sales Records and Ticket Records.
- **Merge Report Data**: Combines the database inputs together.
- **Code - Build Weekly Report**: Summarizes or parses the joined dataset metrics via custom code.
- **Google Sheets - Save Weekly Report**: Adds the generated tabular weekly report data to Sheets.
- **Gmail - Send Weekly Email**: E-mails the customized summary to key stakeholders.
- **Slack - Slack Summary**: Notifies teams via Slack chat regarding the latest metric drops.

## Setup Requirements
- Supabase credentials
- Google OAuth (Sheets & Gmail)
- Slack credentials
