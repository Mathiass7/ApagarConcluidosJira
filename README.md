# ApagarConcluidosJira

Graphical interface to check the status of requirements in Jira and automatically delete local folders marked as "Done".

---

## 📘 Overview

This tool was designed to make it easier for users to clean up folders based on the status of Jira issues.

When executed, the app allows you to check the status of requirements inside a given folder and delete the ones that are marked as **"Done"** in Jira.

---

## 🚀 How It Works

When you open the EXE, you’ll see 3 fields to fill in:

### 📁 Folder Path  
Click **"Select Folder"** → Browse to the folder you want to scan → Click **"Select Folder"**.  
Example:  
`M:/BD - Qualidade AGRO/Matheus`

### 📧 Jira Email  
Enter the email address you use to access Jira. Make sure it has permission to view the issues.

### 🔑 Jira API Token  
This token allows the program to access the Jira API on your behalf.

To generate a token:  
1. Go to: https://id.atlassian.com/manage-profile/security/api-tokens  
2. Click **"Create API token"**  
3. Name it (e.g., `token_jira_app`)  
4. Copy and save the token (it won’t be shown again)

---

## ✅ After Filling All 3 Fields

Click **"Check Status on Jira"**  
- The system will search all subfolders and check the Jira status for each requirement.  
- It will list the results in the interface.

If some requirements are marked as **"Done"**, you can click:  
**"Delete Folders with Status Done"**  
- The program will delete only the subfolders that match this status.

---

## 📁 Subfolder Naming Rules

For the program to detect requirements correctly, the subfolder names must follow these formats:

### 🟢 For AGRO project:
- Just the number: `12345`  
- Or with the prefix: `AGRO-12345`  
(No spaces or extra characters)

### 🔵 For other projects:
- Use Jira-style prefixes, like:  
  `AP-1234`, `AVEND-5678`, `AA-9012`  
(Always format: `LETTERS-NUMBER`, no spaces)

---

## ⚠️ Notes

- Subfolders with names outside these patterns will be ignored.  
- The **Delete** button only works after checking statuses and only removes folders with **"Done"** status.  
- You can also click **"Generate .txt Report"** to export the results to a text file.

---

## 🛠️ Technologies Used

- Python  
- CustomTkinter  
- Requests (HTTP client)  
- Jira REST API

---

## 📄 License

This project is licensed under the MIT License.
