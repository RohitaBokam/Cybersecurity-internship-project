# Cybersecurity-internship-project-2
# Ethical_Email_Phishing_Simulation
Email phishing simulation is a cybersecurity training exercise where organizations send fake, but realistic, phishing emails to their own employees. The purpose is not to hack them, but to test and improve their ability to recognize and avoid phishing attacks in a safe environment.

**Gophish** is an open-source phishing framework designed for businesses and penetration testers to simulate real-world phishing attacks. It makes it easy to create, launch, and track phishing campaigns in a user-friendly and powerful way.

> 🚀 Gophish is fast, self-hosted, and highly customizable to fit your organization’s security awareness needs.

---

## Table of Contents

- [About Gophish](#about-gophish)
- [Features](#features)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Creating a Campaign](#creating-a-campaign)
- [Sending Emails](#sending-emails)
- [Monitoring Results](#monitoring-results)
- [Important Notes](#important-notes)
- [Resources](#resources)
- [License](#license)

---

## About Gophish

Gophish is designed to be a simple and powerful tool for running phishing campaigns. It provides a full web interface to manage:
- Sending emails
- Hosting landing pages
- Tracking opens, clicks, and submitted credentials
- Generating detailed reports

Gophish empowers security teams to train their employees and increase awareness against phishing attacks.

---

## Features

- 📧 Easy Email Template Management
- 🎯 Target Groups Creation
- 🌐 Landing Page Hosting
- 🕵️ Real-time Campaign Tracking
- 📊 Reporting and Analytics
- ⚙️ RESTful API for automation

---

## Installation

You can download Gophish prebuilt binaries or build from source.

### 1. Download Prebuilt Binaries
Go to the [Gophish Releases Page](https://github.com/gophish/gophish/releases) and download the version for your OS.

Extract the archive:
```bash
tar -xvf gophish-vX.X.X-linux-64bit.zip
cd gophish
```

### 2. Build from Source
Make sure you have [Go](https://golang.org/) installed.

```bash
git clone https://github.com/gophish/gophish.git
cd gophish
chmod +x gophish
```

---

## Getting Started

1. Start Gophish:
   ```bash
   ./gophish
   ```
2. Access the Admin Dashboard:
   Open your browser and navigate to:
   ```
   https://127.0.0.1:3333
   ```
   Default credentials:
   - **Username**: admin
   - **Password**: (Password printed in console at first startup)

3. **Change Password:** Always change the default password after first login.

---

## Creating a Campaign

Follow these steps to create a campaign from start to finish:

### Step 1: Setup Sending Profile
- Navigate to **Sending Profiles**.
- Create a new sending profile.
- Input SMTP server details (SMTP host, username, password, and from address).
- Use app password fot the password session.
- Use `smtp.gmail.com:587`
![1](https://github.com/user-attachments/assets/6dc824c3-576f-4956-927c-8a7f1822e5a5)

### Step 2: Create Email Template
- Go to **Email Templates**.
- Create a new template.
- Customize the subject and body (you can insert phishing links, company branding, etc.).
- Use `index.html` for Email Template.
![2](https://github.com/user-attachments/assets/f65aa51a-8817-476f-a5fc-b2b6cf469950)

### Step 3: Create Landing Page
- Navigate to **Landing Pages**.
- Create a new landing page.
- You can clone real login pages or design a custom page.
- Use `login.html`.
- (Optional) Enable **Capture Submitted Data**.
![3](https://github.com/user-attachments/assets/a8ba62c1-9c4e-4c5e-8b49-2b053856651b)


### Step 4: Create a Group of Targets
- Go to **Users & Groups**.
- Create a new group.
- Upload a CSV or manually add target users (name, email).
![4](https://github.com/user-attachments/assets/1853f79b-1e36-4de6-b83c-936d9b2ccd12)


### Step 5: Launch a Campaign
- Navigate to **Campaigns**.
- Create a new campaign by selecting:
  - Name
  - Email template
  - Landing page
  - Url - Use `ngrok http 80` to use public url.
  - Sending profile
  - Group of targets
- Click **Launch Campaign**.
![5](https://github.com/user-attachments/assets/2664e294-2198-4761-b202-3722d53e0529)

---

## Sending Emails

- Once the campaign is launched, Gophish will immediately begin sending emails using your configured sending profile.
- Emails are sent one-by-one with delays to appear more natural (you can configure sending speed).

---

## Monitoring Results

- Gophish tracks:
  - Email opened
  - Link clicked
  - Data submitted
  - Email reported (optional)
- You can view the campaign dashboard for real-time tracking.
- Export campaign results as CSV for reporting.

---

## Important Notes

- **Anti-virus Detection:** Some anti-virus or email services may flag Gophish emails as phishing.
- **Domain and Hosting:** To reduce detection, use your own domain, SSL certificates, and trusted SMTP servers.
- **Legal Disclaimer:** Always obtain proper authorization before sending phishing simulations. Unauthorized phishing is illegal.

---

## Resources

- [Official Documentation](https://docs.getgophish.com/)
- [Gophish GitHub](https://github.com/gophish/gophish)
- [Community Discussions](https://github.com/gophish/gophish/discussions)
