# SSL Certificate Expiry Checker

The SSL Certificate Expiry Checker is a Python script that checks the expiration dates of SSL certificates for a list of endpoints and sends renewal reminders via email using SMTP. It also fetches email recipient addresses from a file hosted on GitLab.

## Requirements

- Python 3.x
- requests
- cryptography

Install the required Python packages using the following command:

pip install requests cryptography


## Configuration

Before running the script, you need to set up the following configuration:

### GitLab Configuration

- Create a personal access token on GitLab to access the file with email recipient addresses. Replace `YOUR_GITLAB_PERSONAL_ACCESS_TOKEN` in the script with your actual token.

### SMTP Configuration

- Replace `your_smtp_server`, `your_sender_email@example.com`, `your_sender_email_password` with your SMTP server details and sender email credentials.

### Endpoint URLs

Create a file named `endpoint_urls.txt` and list the URLs of the endpoints whose SSL certificate you want to check, one URL per line.

### Email Recipients

Create a file named `email_recipients.txt` on GitLab and list the email addresses of the recipients to whom the renewal reminders will be sent, one email address per line.

## Usage

1. Ensure you have correctly set up the GitLab and SMTP configurations as mentioned above.

2. Add the URLs of the endpoints to be checked in the `endpoint_urls.txt` file.

3. Add the email recipients' addresses to the `email_recipients.txt` file on GitLab.

4. Run the script using the following command:

python script.py


The script will check the SSL certificate expiration for each endpoint and send renewal reminders to the specified recipients if the certificates are expiring in less than 30 days.

## License

