# NMNH-2.0
NMNH 2.0 – Multi-strategy Nifty/BankNifty/Sensex/BTCUSD Hedged Dashboard. Real-time options data, live PNL, breakevens, and interactive trading dashboard with full DevOps CI/CD integration.

---

## Features

- Login page with **Postgres DB** for user authentication  
- Full-screen **candlestick animation** background  
- Live display of **BTC/USD or Nifty data**  
- Dashboard panels for **positions, PNL, and breakevens**  
- Multi-container setup:  
  - `web` → Flask app  
  - `db` → Postgres database  
- Ready for **CI/CD via GitHub + Jenkins**  
- Dockerized for easy deployment  

---

## Folder Structure

NMNH-2.0/
│
├─ backend/                     # Flask app + Python code
│   ├─ app.py                   # Main Flask application
│   ├─ requirements.txt         # Python dependencies
│   ├─ Dockerfile               # Dockerfile for web container
│   └─ templates/               # HTML templates
│       ├─ login.html           # Login page with candlestick background
│       └─ index.html           # Dashboard page after login
│
├─ docker-compose.yml           # Multi-container setup (web + db)
├─ README.md                    # Project description, setup, CI/CD instructions
├─ jenkins/                     # (Optional) Jenkins pipeline scripts
│   └─ Jenkinsfile              # Jenkins pipeline for CI/CD
├─ db_init/                     # (Optional) database initialization scripts
│   └─ init.sql                 # SQL scripts to create tables & dummy users
├─ static/                      # Static assets like CSS, JS, images
│   ├─ css/
│   │   └─ style.css            # Styles for login/dashboard
│   └─ js/
│       └─ main.js              # Custom JS scripts for animations or charts
└─ utils/                       # (Optional) Helper Python scripts
    └─ data_fetcher.py          # For fetching live BTC/Nifty data
