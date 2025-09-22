# 💌 Interactive Email Spoofer (Safe & Legal Version)

> **Disclaimer:** This tool is for **educational purposes only**. Always test with your own email accounts. The developer is **not responsible** for unauthorized or illegal use. Use responsibly.

---

## Table of Contents

* [Overview](#overview)
* [Requirements](#requirements)
* [Installation](#installation)

  * [Linux/macOS](#linuxmacos)
  * [Windows](#windows)
* [Operating the Script](#operating-the-script)
* [User Manual](#user-manual)
* [Gmail App Password Guide](#gmail-app-password-guide)
* [License](#license)

---

## Overview

The **Interactive Email Spoofer** allows you to:

* Send emails with a **custom 'From' address** and **Reply-To** field.
* Test email layouts and awareness safely.
* Input multi-line email body, preserving blank lines.
* Authenticate securely via Gmail **App Passwords**.
* Clear terminal automatically on launch for clean operation.

---

## Requirements

* Python 3.8 or higher
* Standard Python modules (all built-in):

  * `smtplib`, `email`, `sys`, `os`
  * `tty` & `termios` (Linux/macOS)
  * `msvcrt` (Windows)

No additional pip packages required.

---

## Installation

### Linux / macOS

```bash
# Clone repository
git clone https://github.com/YOUR_USERNAME/email-spoofer.git
cd email-spoofer

# Make script executable (optional)
chmod +x email_spoofer.py

# Run script
python3 email_spoofer.py
```

### Windows

```powershell
# Clone repository
git clone https://github.com/YOUR_USERNAME/email-spoofer.git
cd email-spoofer

# Run script
python email_spoofer.py
```

---

## Operating the Script

1. Terminal will **clear automatically** at start.
2. Follow the **interactive prompts**:

| Step | Input Field            | Notes                                                                                     |
| ---- | ---------------------- | ----------------------------------------------------------------------------------------- |
| 1️⃣  | **Sender Email**       | Your Gmail account (used for SMTP authentication).                                        |
| 2️⃣  | **Gmail App Password** | 16-character App Password (acknowledges immediately after 16 chars).                      |
| 3️⃣  | **Receiver Email**     | The target email (for safe testing, use your own).                                        |
| 4️⃣  | **From Email**         | Appears in the 'From' field (spoofed).                                                    |
| 5️⃣  | **Reply-To Email**     | Replies will go here.                                                                     |
| 6️⃣  | **Email Subject**      | Subject line of the email.                                                                |
| 7️⃣  | **Email Body**         | Multi-line content; finish with **Ctrl+D** (Linux/macOS) or **Ctrl+Z + Enter** (Windows). |

* The script uses Gmail **SMTP** with `STARTTLS`.
* Custom headers:

  * `X-Priority: 3`
  * `X-Mailer: Microsoft Outlook 16.0`
* Multi-line formatting and blank lines are preserved.

---

## User Manual

* **Password Handling:** Immediate acknowledgement after 16 non-space characters. Spaces are stripped before sending.
* **Email Features:** Multi-line body, custom headers, reply-to management, secure Gmail authentication.
* **Terminal:** Clears automatically for each run, making output readable and clean.

---

## Gmail App Password Guide

1. Visit [Google Account Security](https://myaccount.google.com/security)
2. Enable **2-Step Verification** if not already enabled.
3. Click **App passwords**
4. Select **Mail** as the app and **Other** for the device (e.g., "SpoofMail").
5. Click **Generate**
6. Use the **16-character password** in this script. Remove spaces if any.

---

## License

## License
This project is licensed under the **GNU General Public License v3.0 (GPL-3.0)**.  
You are free to use, modify, and distribute this software **for educational and legal purposes only**, following the terms of the GPL.  

For more information, see the [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0.en.html).

