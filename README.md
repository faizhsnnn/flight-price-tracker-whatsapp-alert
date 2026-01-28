# ✈️ Flight Price Tracker with WhatsApp Alerts (Python)

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Challenge](https://img.shields.io/badge/Challenge-90DaysOfCode-orange)

---

## 📌 Overview

The Flight Price Tracker is a Python-based automation project that monitors flight prices for multiple destinations and sends WhatsApp alerts when prices drop below a predefined threshold.

The application integrates multiple external services including Sheety, Amadeus Flight APIs, and Twilio WhatsApp messaging. It was built as part of my **#90DaysOfCode** journey to practice real-world automation, API integration, and modular application design.

---

## 🚀 Key Features

✈️ Live flight price tracking using Amadeus API  
📊 Destination data management using Google Sheets (via Sheety)  
🔍 Automatic IATA code detection for destinations  
💰 Cheapest flight detection logic  
📨 WhatsApp alerts for price drops using Twilio  
🔐 Secure configuration via environment variables  
🧩 Modular, object-oriented project structure  

---

## 📁 Project Structure
```
flight-price-tracker-whatsapp-alert/
│
├── main.py
│ └── Application entry point and automation workflow
│
├── data_manager.py
│ └── Manages destination data using Sheety API
│
├── flight_search.py
│ └── Handles Amadeus API authentication and flight search
│
├── flight_data.py
│ └── Processes flight data and determines cheapest flights
│
├── notification_manager.py
│ └── Sends WhatsApp alerts using Twilio
│
└── README.md
└── Project documentation
```

---

## 🛠️ Application Workflow

1. Destination data is fetched from a Google Sheet using Sheety.
2. Missing IATA codes are automatically retrieved using the Amadeus API.
3. Destination data is updated back into the sheet.
4. Flight prices are searched for each destination within a six-month window.
5. The cheapest available flight is identified.
6. If a cheaper price is found:
   - A WhatsApp alert is sent with flight details.
7. The process repeats for all destinations.

This demonstrates real-world automation across data storage, APIs, and messaging services.

---

## ▶️ Execution Instructions

### 1️⃣ Clone the Repository
```
git clone https://github.com/your-username/flight-price-tracker-whatsapp-alert.git
cd flight-price-tracker-whatsapp-alert
```

---

### 2️⃣ Install Dependencies
```
pip install requests python-dotenv twilio
```

---

### 3️⃣ Configure Environment Variables (IMPORTANT)

Create a `.env` file or set the following environment variables:

```
# Sheety
SHEETY_USERNAME=your_username
SHEETY_PASSWORD=your_password

# Amadeus
AMADEUS_API_KEY=your_api_key
AMADEUS_SECRET=your_api_secret

# Twilio
TWILIO_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_WHATSAPP_NUMBER=+1415523xxxx
TWILIO_VERIFIED_NUMBER=+91xxxxxxxxxx
```
# ⚠️ Security Note:
Never commit .env files or credentials to public repositories.

---
# 4️⃣ Run the Application
```
python main.py
```

---
# ⚠️ Important Notes

Python 3.x is required

Internet connection is required

Valid API credentials are required for all services

WhatsApp messaging requires a Twilio sandbox or approved number

Designed for educational and personal automation use

---
# 🧠 Concepts Demonstrated

REST API integration

OAuth authentication

Object-oriented programming

Modular application design

Data persistence and synchronization

Automation workflows

Notification systems


---
# 🎯 Project Significance

This project simulates a real-world price monitoring and alert system similar to commercial flight deal trackers. It demonstrates how Python can orchestrate multiple services to automate data-driven decision-making and user notifications.

---
# 👨‍💻 Author

Faiz Hasan

BCA Final Year — Graphic Era University

🚀 Python Learner | #90DaysOfCode

---
*“Automation turns data into timely opportunities.”*
