# email-verification-code

A simple Python script for verifying email addresses using syntax, DNS, and SMTP mailbox verification.

## Description

This project provides a Python-based email verification tool that validates email addresses through a three-step process: syntax checking using regex, DNS MX record lookup, and SMTP mailbox verification. It's useful for developers who need to verify whether an email address exists before sending emails, helping reduce bounce rates and improve email deliverability.

## Features

- Email syntax validation using regular expressions
- DNS MX record lookup to verify domain mail servers
- SMTP mailbox verification to check if the email address exists
- Interactive command-line interface for email input
- Debug level configuration for detailed SMTP conversation output

## Technologies Used

- Python 3
- dnspython (dns.resolver) - For DNS MX record lookups
- smtplib - For SMTP communication
- re - For regex pattern matching

## Installation

```bash
# Clone the repository
git clone https://github.com/bryanseah234/Python-Email-Verification-Script.git

# Navigate to project directory
cd Python-Email-Verification-Script

# Install dependencies
pip install dnspython
```

## Usage

```bash
# Run the script
python src/VerifyEmailAddress.py
```

When prompted, enter the email address you wish to verify. The script will:
1. Check the email syntax
2. Look up the domain's MX records
3. Connect to the mail server and verify if the mailbox exists
4. Display "Success" if the email is valid, or "Bad" if verification fails

## Warnings

- Excessive use may result in being blacklisted (e.g., Spamhaus), especially with dynamic IP addresses
- B2C addresses (Hotmail, Yahoo, etc.) may not work well due to their spam protection rules
- Some mail servers may give incorrect results (e.g., catch-all servers that accept all addresses)

## Disclaimer

1. FOR EDUCATIONAL PURPOSES ONLY
2. USE AT YOUR OWN DISCRETION

## License

Apache License 2.0

---

**Author:** <a href="https://github.com/bryanseah234">bryanseah234</a>
