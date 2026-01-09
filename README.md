# 🔐 AWS IAM User Management & Security Setup

## 📌 Objective
This document explains step-by-step **AWS IAM user creation, MFA setup, access keys, AWS CLI configuration, password policies, and auditing**.

---

## 1️⃣ IAM Account – Create User

- Go to **AWS Management Console**
-  Open **IAM Dashboard**
- Click **Users**
- Click **Create user**
- Enter **Username**  
   - Example: `kumlesh-kurre`
- Enable  
   ☑️ *Provide user access to the AWS Management Console*
- Choose **Custom password**
- Enable  
   ☑️ *User must create a new password at next sign-in*
- Create a **User Group**
   - Group name: `admin`
   - Policy: **AdministratorAccess**
- Click **Create user group**
 Review configuration
- Click **Create user**
- Download the **CSV file**
- Sign out from AWS

---

## 2️⃣ Add Multi-Factor Authentication (MFA)

- Login using **IAM user**
-  Enter:
   - Account ID
   - Username
   - Password
- Access the **AWS Console**
- Go to **IAM Dashboard**
- Open **Security recommendations**
- Click **Add MFA for yourself**
- Create a **Device name**
- Select device option:
   - **Authentication app**
- Click **Next**
- Install **Google Authenticator** on mobile
  - Scan the **QR Code**
  - Enter **MFA codes**
- Complete MFA setup

---

## 3️⃣ Set Account Alias

- Go to **IAM Dashboard**
- Select **Account settings**
- Edit **Account alias**
- Example:
   - `kumlesh711`
- Click **Save**

---

## 4️⃣ Create Access Key

- Click **Account name → Security credentials**
- Go to **Access keys**
- Click **Create access key**
- Choose use case:
   - **Command Line Interface (CLI)**
- Tick confirmation:
   ☑️ *I understand the security recommendations*
- Click **Next**
- Create access key
- Download the **CSV file**

> ⚠️ Never upload this CSV file to GitHub.

---

## 5️⃣ AWS CLI Setup (Windows)

- Open browser
-  Download **AWS CLI for Windows**
- Install AWS CLI
- Open **Command Prompt (CMD)**
- Verify installation:
   ```bash
   aws --version

---
## Configure AWS CLI:

aws configure
- Enter:
- Access Key ID
- Secret Access Key
- Default region
- Output format
- Verify IAM user:
- aws iam list-users
---
## 6️⃣ Customize AWS Password Policies

- Go to IAM → Users
- Open Security credentials
- Click Manage console access
- Enable Custom password
- Edit password settings
- Click Save changes
---
## 7️⃣ Audit Permissions Using IAM Credential Report

- Go to IAM Dashboard
- Open Credential reports
- Click Download credential report
- Review:
- Password status
- Access key usage
- MFA status
---
## 8️⃣ Check User Allowed Services

- Go to IAM → Users
- Select a user
- Open Last accessed
- Review allowed and recently accessed services
---
## ⚠️ Security Best Practices

❌ Never share:

Account ID
Passwords
Access keys
CSV files

✅ Always enable MFA

✅ Follow Principle of Least Privilege

✅ Regularly audit IAM users

 ## 🎯 Purpose of This Project

- Demonstrates **AWS IAM fundamentals**
- Shows understanding of **cloud security best practices**
- Useful for **IT Support / IT Administrator / Network Support** roles
- Documentation

---
## 👨‍💻 Author

**Kumlesh Kurre**  
 IT Support & Network Engineer  

---

⭐ If you find this project helpful, please give it a star on GitHub.

