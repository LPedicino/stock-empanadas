# 🥟 Empanada Stock Management System

![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Active-success)
![Supabase](https://img.shields.io/badge/Supabase-Database%20%26%20Auth-emerald)
![Security](https://img.shields.io/badge/Security-RLS%20Protected-orange)

A lightweight, secure, and production-ready web application designed for artisanal food businesses to manage real-time inventory. Built with a modern **defense-in-depth** architecture, separating frontend hosting from a strictly secured backend.

---

## 🚀 Tech Stack

* **Frontend:** HTML5, Modern CSS (Custom Kitchen Design System), JavaScript (ES6+).
* **Hosting & CI/CD:** GitHub Pages deployed via structured Git branching workflows and Pull Requests.
* **Backend & Database:** Supabase (PostgreSQL).
* **Security:** Supabase Auth (Email/Password) paired with Row Level Security (RLS) database policies.

---

## 🛡️ Security Architecture

The application implements a strict **Defense-in-Depth** model:
1. **Authentication:** Only verified administrative users can obtain an active session via Supabase Auth tokens.
2. **Authorization (RLS):** 
   - **Public Access (`SELECT`):** Open read access to display live stock data.
   - **Admin Access (`UPDATE`):** Restricted strictly to `authenticated` users via Row Level Security policies.

---

## 💡 Key Features

* **Real-Time Sync:** Instant database updates reflecting live kitchen stock.
* **Artisanal UI/UX:** Warm, custom-tailored kitchen aesthetic designed for high readability and ease of use.
* **Keyboard Accessibility:** Native `Enter` key execution on authentication forms.
* **Robust Session Sanitization:** Handled asynchronous client-side cleanup preventing lingering authentication tokens on page reload.

---

## 📂 Project Structure

```text
├── index.html        # Main application UI & Supabase client logic
└── README.md         # Project documentation
```

## 🔧 Setup & Local Configuration

To configure or deploy your own instance of this application:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   ```
2. **Configure Supabase Credentials:**
   Open `index.html` and insert your project keys:
   ```javascript
   const SUPABASE_URL = 'YOUR_SUPABASE_URL';
   const SUPABASE_ANON_KEY = 'YOUR_SUPABASE_ANON_KEY';
   ```
3. **Database Requirements:** Ensure your PostgreSQL table (`stock_empanadas`) has RLS policies configured for `SELECT` and `UPDATE` operations.

---

## 🌿 Development Workflow

This project follows a strict **Feature-Branch Git Workflow**:

* `main` branch is reserved for live production deployments.
* All new features and bug fixes are isolated in dedicated branches (`feature/*`, `fix/*`).
* Changes are reviewed and merged via GitHub Pull Requests.
