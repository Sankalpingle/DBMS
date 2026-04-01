# 🩸 Blood Bank Management System

A Python CLI application with SQLite for managing blood donations, stock, and requests.

## ▶️ How to Run

```bash
python3 blood_bank.py
```

> No external libraries needed — uses only Python standard library.

---

## 📋 Features

| Feature | Details |
|---|---|
| **Donor Registration** | Register donors with name, age, blood group, contact, city. Auto-adds 1 unit to stock. |
| **Blood Stock Management** | View stock levels (colour-coded), add units manually from drives. |
| **Search by Blood Group** | Find all donors for a given blood group + see current stock. |
| **Request / Issue Blood** | Submit requests — auto-approved if stock sufficient, else saved as Pending. |

---

## 🗃️ Database Schema

**`donors`** — Donor records  
**`blood_stock`** — Units per blood group (A+, A-, B+, B-, AB+, AB-, O+, O-)  
**`blood_requests`** — Patient blood requests with approval status

---

## 🗂️ Project Structure

```
blood_bank/
├── blood_bank.py   ← Main application
├── blood_bank.db   ← SQLite DB (auto-created on first run)
└── README.md
```

---

## 💡 Validations

- Age must be between 18–65
- Contact must be exactly 10 digits
- Blood requests auto-check available stock before approval
- Stock status: 🔴 Out of Stock | 🟡 Low (<5 units) | 🟢 Sufficient
