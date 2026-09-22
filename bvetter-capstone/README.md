# 🐾 BVetter — Data-Driven Veterinary Services System

**A web-based veterinary management platform with predictive analytics, built for the Baliuag Veterinary Services Office (Baliuag City, Bulacan) to replace manual logbooks with centralized data, disease forecasting, and vaccination planning.**

🔗 **Live site:** [bvetter.me](https://bvetter.me) — public portal is open to browse
📊 Capstone Project — BS Information Technology, Bulacan State University (Bustos Campus)

---

## 📌 The Problem

The Baliuag Veterinary Services Office relied on paper logbooks and scattered spreadsheets to track consultations and vaccinations. This made it hard to spot disease trends early, plan vaccination drives, or respond quickly to outbreaks — and pet owners had no easy way to get information or find lost pets.

## 💡 What We Built

BVetter centralizes veterinary records and layers predictive analytics on top of them, so the office can move from reactive record-keeping to proactive planning. It has three portals — **Pet Owner**, **Veterinarian**, and **Admin** — plus two machine learning models running in the background:

| Model | Purpose |
|---|---|
| **Random Forest** | Predicts disease frequency and risk level per barangay, using historical consultation data |
| **ARIMA (time-series)** | Forecasts vaccine demand per barangay for upcoming mass vaccination drives |

---

## 📊 Key Insights the System Surfaces

These are pulled directly from the live dashboards:

- **684 total disease cases** tracked across all barangays (Jan–Jul 2026 baseline)
- **Skin Infection** is the most common diagnosis, at **33%** of all cases — Upper Respiratory Infection is 2nd
- **7 barangays** are flagged as "needs action" based on current case volume, with **2 more** to watch
- Disease forecast model performs **within 7.8%** accuracy of municipality-wide totals
- **14,387 pets vaccinated** to date, with next-month demand forecasted at a stable ~400
- Vaccine demand forecasting breaks down by species (dogs vs. cats) and by client volume, not just totals
- Lost-and-found matching uses a similarity algorithm (breed, size, location, photo color profile) to auto-suggest matches with a confidence score — e.g., a Pomeranian lost/found pair matched at 59% confidence

The goal isn't just to display numbers — it's to turn raw consultation logs into decisions the office can act on: which barangay to prioritize, how much vaccine stock to prepare, and where outbreaks might be starting.

---

## 🖥️ Screenshots

### Veterinarian Dashboard
Real-time overview of patient volume trends and disease cases by barangay.
![Dashboard](screenshots/dashboard.png)

### Disease Analytics
Historical case data vs. Random Forest–projected annual forecasts, sorted side-by-side per barangay.
![Disease Analytics](screenshots/disease-analytics.png)
![Disease Analytics by Barangay](screenshots/disease-analytics-barangay.png)

### Disease Risk Map
Barangays plotted on an interactive map, color-coded by risk level (Needs Action / Watch / Normal) and sized by case count.
![Disease Risk Map](screenshots/disease-map.png)

### Mass Vaccination Forecasting
ARIMA-based 3-month vaccine demand forecast, broken down by barangay, species, and expected client turnout.
![Mass Vaccination](screenshots/mass-vaccination.png)
![Vaccination Overview](screenshots/mass-vaccination-overview.png)

### Reports
Auto-generated statistics: total patients, most common disease, most active barangay — exportable for LGU reporting.
![Reports](screenshots/reports.png)

### Lost & Found Matching
Similarity-based matching engine that compares breed, size, location, and photo color profile to suggest lost/found pet matches with a confidence score.
![Lost and Found](screenshots/lost-and-found.png)

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, Vanilla JavaScript |
| Backend | PHP 8.x |
| Database | MySQL |
| Analytics | Python — Random Forest (scikit-learn), ARIMA/SARIMA (statsmodels) |
| Image Matching | Python — Pillow (perceptual hashing + color histogram) |


## 🎯 Study Objectives

This system was built to answer:
1. How can fragmented, paper-based veterinary records be structured into a centralized system?
2. How can machine learning transform historical data into actionable disease and vaccination forecasts?
3. How can predictive models be evaluated for accuracy and reliability (precision, recall, F1-score)?
4. How can a chatbot and similarity-matching module improve service accessibility?

Evaluated against **ISO/IEC 25010** software quality standards and the **Technology Acceptance Model (TAM)**.

---

## 📎 Related Links

- 🔗 Live site: [bvetter.me](https://bvetter.me)
