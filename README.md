# 🎓 Smart Attendance Tracker & Notifier
[![Python Version](https://img.shields.io/badge/python-3.13-blue.svg)](https://www.python.org/)
[![Library](https://img.shields.io/badge/library-openpyxl-green.svg)](https://openpyxl.readthedocs.io/)
[![Automation](https://img.shields.io/badge/automation-SMTP-orange.svg)](https://docs.python.org/3/library/smtplib.html)

A powerful, beginner-friendly Python automation tool that manages classroom attendance using Excel and sends automated email alerts to students and faculty.

---

## 🌟 Overview
Monitoring attendance shouldn't be a manual chore. This project automates the workflow of tracking absences, identifying students at risk of low attendance, and notifying them via email before they cross the critical threshold.



---

## 📂 Project Structure

| File | Description |
| :--- | :--- |
| `python_code.py` | The main engine that handles Excel logic and email triggers. |
| `attendance.xlsx` | **(Example Output)** The database where attendance records are stored. |
| `requirements.txt` | Lists the external libraries needed to run the script. |
| `.gitignore` | Prevents sensitive credential files and temp data from being uploaded. |

---

## 🛠️ Tech Stack
* **Language:** Python 3.13
* **Data Management:** `openpyxl` (Excel manipulation)
* **Communication:** `smtplib` & `email.mime` (Standard Python Email Protocols)

---

## 📊 Logic & Workflow

The system operates based on specific absence thresholds:

1.  **Input Phase:** User enters the subject and roll numbers of absent students.
2.  **Processing:** * If a student reaches **2 leaves**, they receive a **Warning Email** ("One more leave allowed").
    * If a student reaches **>2 leaves**, they are flagged for **Critical Lack of Attendance**.
3.  **Communication:**
    * **Students** receive an alert regarding their eligibility.
    * **Faculty** receive a summary list of all students currently in the "Lack of Attendance" category for their specific subject.



---

## 🚀 Getting Started

### 1. Installation
Clone this repo and install the requirements:
```bash
pip install -r requirements.txt
```
### 2. Configuration
Open python_code.py and update the sender credentials:
```bash
SENDER_EMAIL = "your-email@gmail.com"
SENDER_PWD = "your-app-password"  # Do not use your regular password!
```
### 2. Run the App
```bash
python python_code.py
```
## 🛡️ Security & Best Practices

* **Credentials**: This project is designed to use Environment Variables or App Passwords. Never hardcode your actual Gmail password.
* **Ignored Files**: The .gitignore file ensures that __pycache__ and temporary Excel files (~$attendance.xlsx) do not clutter your repository.

## 🤝 Contributing
Contributions make the open-source community an amazing place to learn and create. Any contributions you make are greatly appreciated.

1. Fork the Project
2. Create your Feature Branch
3. Commit your Changes
4. Push to the Branch
5. Open a Pull Request
