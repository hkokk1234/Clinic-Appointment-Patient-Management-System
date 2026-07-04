# 🏥 Clinic Appointment & Patient Management System


⭐ If you find this project useful, consider starring the repo! ⭐

A lightweight, role-based **Clinic Appointment & Patient Management System** for healthcare facilities, built to make appointment booking, patient records, and doctor scheduling simple for clinics that don't need (or can't afford) an enterprise-grade hospital ERP.

🩺 Simple enough for a small clinic, structured enough to scale
🔄 A learning-friendly alternative to bloated hospital management suites
🌐 Built with PHP, MySQL, HTML/CSS & JavaScript

![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![License](https://img.shields.io/badge/license-Educational-lightgrey)
![Status](https://img.shields.io/badge/status-in%20development-yellow)

---

## 🚀 Features

| 👤 Patient Portal | 🩺 Doctor Portal | 🛠️ Admin Panel |
|---|---|---|
| Create an account & manage profile | View and manage personal schedule | Manage patients, doctors & staff |
| Book appointments with available doctors | Accept / view booked appointments | Assign & edit doctor sessions |
| View upcoming & past appointments | Manage available time sessions | Full appointment oversight |
| Cancel or edit bookings | Access patient details for bookings | Add / remove patient & doctor records |
| Update personal & medical info | Update profile & settings | Bulk import patients |

*All three roles run from a single, unified login system with role-based redirects and access control.*

---

## 📸 Screenshots

> _Add screenshots here once available — e.g. `docs/screenshots/login.png`, `docs/screenshots/patient-dashboard.png`, `docs/screenshots/admin-panel.png`_

```md
![Login Page](docs/screenshots/login.png)
![Patient Dashboard](docs/screenshots/patient-dashboard.png)
![Admin Panel](docs/screenshots/admin-panel.png)
```

---

## 🧱 Tech Stack

- **Backend:** PHP (procedural, `mysqli`)
- **Database:** MySQL
- **Frontend:** HTML, CSS, vanilla JavaScript
- **Auth:** PHP Sessions with role-based access (`admin`, `doctor`, `patient`)

---

## ❗ Requirements

- PHP 7.4+ (with `mysqli` extension enabled)
- MySQL 5.7+ or MariaDB
- Apache / Nginx (or XAMPP / WAMP for local development)

---

## ⚡ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/hkokk1234/Patient-Management-in-Healthcare-System.git
   ```

2. **Create the database**
   - Open phpMyAdmin (or your MySQL client of choice)
   - Create a new database, e.g. `personaldoctor`
   - Import the included schema:
     ```bash
     mysql -u root -p personaldoctor < healthcare_system.sql
     ```

3. **Configure the database connection**
   - Open `healthcare_system/connection.php`
   - Update the credentials to match your local setup:
     ```php
     $database = new mysqli("localhost", "your_user", "your_password", "personaldoctor");
     ```

4. **Deploy**
   - Copy the `healthcare_system/` folder into your server's web root (e.g. `htdocs/` for XAMPP)
   - Navigate to `http://localhost/healthcare_system/` in your browser

5. **Sign up** for a new account or use a seeded admin account (see `healthcare_system.sql`) to get started.

---

## 🗂️ Project Structure

```
healthcare_system/
├── admin/          # Admin dashboard, patient/doctor management, scheduling
├── doctor/         # Doctor dashboard, session & appointment management
├── patient/        # Patient dashboard, booking, profile settings
├── css/            # Stylesheets
├── img/            # Static assets & icons
├── informations/   # Static info page
├── connection.php  # Database connection config
├── login.php       # Unified login for all roles
├── signup.php      # Patient registration
└── index.php       # Landing page
```

---

## 🔒 Known Limitations & Roadmap

This project started as an academic exercise, so a few production-readiness items are still open:

- [ ] Move from raw/interpolated queries to **prepared statements** across all files
- [ ] Hash passwords with `password_hash()` / `password_verify()` instead of storing them in plain text
- [ ] Externalize DB credentials into a `.env` / config file (not committed to git)
- [ ] Add CSRF protection to forms
- [ ] Add automated tests

Contributions and suggestions on any of the above are very welcome!

---

## 🤝 Contributing

Found a bug or have an idea for a feature? Open an issue or submit a pull request — this project is a great sandbox for learning secure PHP practices.

---

## 📜 License

This project was built for educational purposes as part of a university course.
