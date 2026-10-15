# 🛡️ SIEM Tool Project - Custom Wazuh SOC Dashboard

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![React](https://img.shields.io/badge/Frontend-React-cyan)
![Python](https://img.shields.io/badge/Backend-Python-yellow)

## 📖 Overview

**SIEM Tool Project** is a custom-built Security Information and Event Management (SIEM) dashboard designed to integrate seamlessly with the Wazuh API. Built with a React frontend and a Python backend, it transforms raw security data into actionable intelligence for SOC (Security Operations Center) analysts. 

Inspired by modern threat detection and XDR (Extended Detection and Response) architectures, this tool provides real-time monitoring, intelligent alerting, and active response tracking, deployed in an Azure infrastructure.

## ✨ Key Features

* **📊 Interactive SOC Dashboard:** A real-time, React-based frontend providing a quick overview of active threats and system health.
* **🚨 Intelligent Alerting:** Reduces background noise by filtering insignificant events and highlighting critical security alerts. Clicking on any alert opens a modal with complete details (Rule ID, MITRE tactics, timestamps).
* **🖥️ Agent Monitoring:** Track the health, status, and connectivity of all active agents within the Manager-Agent architecture.
* **🛑 Active Response & IP Blocking History:** A dedicated history page that provides a complete record of all IP blocking actions triggered by the SIEM's automated defense mechanisms.
* **📈 Attack Timeline:** Visual representation of attacks (e.g., SSH Brute-Force) in real-time to help analysts understand the attack lifecycle.

## 🏗️ Architecture & Technologies

The system is designed on a **Manager-Agent** architecture, ready for future evolution towards XDR.

* **Frontend:** React, Vite, CSS (Tailwind/Custom components for Dashboard, Alerts, Agents, Timeline).
* **Backend:** Python (FastAPI/Flask) acting as a middleware/client (`wazuh_client.py`) to interact with the Wazuh API.
* **Infrastructure:** Microsoft Azure (Virtual Machines).

## 🚀 Getting Started

### Prerequisites
* Python 3.8+
* Node.js & npm
* A running instance of Wazuh Manager with API access enabled.

### Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd backend/siem-backend
Set up the virtual environment:

Bash
python -m venv siem-env
source siem-env/bin/activate  # On Windows use `siem-env\Scripts\activate`
Install dependencies:

Bash
pip install -r requirements.txt
Configure your .env file based on .env.example with your Wazuh API credentials.

Run the backend server:

Bash
python main.py
Frontend Setup
Navigate to the frontend directory:

Bash
cd src
Install dependencies:

Bash
npm install
Start the development server:

Bash
npm run dev
🎯 Red Teaming & Validation
This SIEM tool has been successfully validated against live Red Teaming scenarios, specifically detecting and mitigating SSH Brute-Force attacks. The system successfully captures the raw events and translates them into actionable SOC alerts mapped to the MITRE ATT&CK framework.
