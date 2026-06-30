# 🛡️ Duplicate Payment Prevention System

A production-ready Full-Stack AI-integrated transaction safety system designed to detect and block accidental duplicate payments within a 2-minute time window. 

This project features a secure **FastAPI** backend with automated **SQLite** database logging and a clean, responsive HTML/CSS dashboard frontend.

---

## 🚀 Live Demo
🌐 **Deployment Link:** [Paste Your Render Live Link Here]

---

## ✨ Features
* **Real-time Duplicate Validation:** Automatically tracks and blocks identical transactions (Same User, Vendor, and Amount) requested within 2 minutes.
* **Persistent SQLite Logging:** Transactions are securely recorded in a local SQLite database, ensuring data persistence even after server restarts.
* **Dynamic Countdown Alerts:** Provides immediate feedback with exact remaining cooldown seconds when a duplicate is triggered.
* **CORS Enabled:** Fully configured to communicate across multiple origins seamlessly.

---

## 🛠️ System Architecture & Database Structure
The backend tracks every inbound payload using the following schema:

| Column Name | Type | Purpose |
| :--- | :--- | :--- |
| **id** | `INTEGER` | Auto-incrementing primary key. |
| **user_id** | `TEXT` | Unique identifier of the payer. |
| **vendor_id** | `TEXT` | Unique identifier of the payee/vendor. |
| **amount** | `REAL` | Transaction value. |
| **timestamp** | `TEXT` | Exact date-time of the request (used for the 2-min lock). |
| **status** | `TEXT` | Transaction state (`Success` / `Blocked`). |

---

## 📂 Project Structure
```text
├── main.py            # FastAPI Backend Application & SQLite Logic
├── index.html         # Frontend Dashboard (UI & Fetch API)
├── requirements.txt   # Third-party Python Dependencies
└── Procfile           # Production WSGI/ASGI Server Configuration
## 🌐 Live Demo
[Duplicate Payment Prevention](https://duplicate-payment-prevention-1.onrender.com)
<img width="1895" height="969" alt="Screenshot 2026-06-30 230256" src="https://github.com/user-attachments/assets/1279d0c2-35e5-4fbe-a43d-44e04c4c4117" />
<img width="1912" height="964" alt="Screenshot 2026-06-30 230345" src="https://github.com/user-attachments/assets/93fdf688-e296-4d3e-9f76-7868815dca84" />
<img width="1916" height="971" alt="Screenshot 2026-06-30 230435" src="https://github.com/user-attachments/assets/0de00c0e-4ea5-4b8d-a951-e43e898d30a5" />


