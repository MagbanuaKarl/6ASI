# JIRA Ticket Creator

This Google Apps Script automates the creation of JIRA tickets based on data entered into a Google Sheets spreadsheet. It also monitors the status of the created tickets and sends email notifications upon completion.

## Prerequisites

Before using this script, ensure you have the following:

- A Google account
- Access to Google Sheets
- Access to Google Apps Script
- A JIRA account
- API access enabled in your JIRA account
- Basic understanding of Google Apps Script and JIRA API

## Setup

1. Open the Google Sheets spreadsheet where you want to create JIRA tickets.
2. Go to `Extensions` > `Apps Script`.
3. Paste the provided script into the script editor.
4. Save the script.
5. Authorize the script to access your Google Sheets data.
6. Update the `username`, `apiToken`, and JIRA `apiUrl` variables in the script with your JIRA credentials and API URL.
7. Create a trigger for the `createJiraTicket()` function to execute it automatically whenever new data is added to the spreadsheet.

## Usage

1. Enter data into your Google Sheets spreadsheet. The script will automatically create a JIRA ticket based on the last row of data.
2. Once the ticket is created, its key will be added to the spreadsheet.
3. The script will then monitor the status of the ticket. When the status changes to "Done," it will send an email notification to the specified recipient with the most recent comment from the JIRA ticket.
4. The trigger for monitoring the ticket status will be stopped automatically once the ticket status is "Done."

## Additional Notes

- Error handling: The script contains basic error handling for failed API requests. You may customize the error handling according to your requirements.
- Security: Ensure to keep your JIRA API credentials secure. Avoid hardcoding sensitive information directly into the script for enhanced security.
- Customization: Feel free to customize the script according to your specific workflow and requirements.

For detailed information on each function and its purpose, refer to the comments within the script itself.

