# Gagan Chandra

**Backend / Software Engineer** — Python · FastAPI · Node.js · Docker · PostgreSQL · MongoDB

[gaganchandra02@gmail.com](mailto:gaganchandra02@gmail.com) · [LinkedIn](https://linkedin.com/in/gagan-chandra) · [Portfolio](https://gaganchandra.in) · [GitHub](https://github.com/gagannchandra)

---

Final-year B.Tech CS (AI) student at PSIT, Kanpur — graduating July 2026 and actively looking for **SDE / Backend / ML Engineering roles**.

I spend most of my time building backend systems and ML-integrated tools: designing APIs, thinking through data models, and getting models out of notebooks into something that runs reliably in production. Four live projects shipped. Two GATE 2026 streams qualified. Open to relocation.

---

## Projects

### [Shortly — URL Shortener with Analytics](https://github.com/gagannchandra/shortly-url-shortener) · [Live ↗](https://shortly.gaganchandra.in)
`Python` `Flask` `MongoDB` `Docker` `GitHub Actions`

Built in two versions — v1 was a prototype, v2 is a proper production rebuild. The interesting parts: MongoDB TTL indexes handle link expiry without a cron job, `secrets.choice` instead of `random` for short-code generation (predictable randomness is an actual attack vector), and a pytest suite that runs against `mongomock` so CI never touches a real database.

- Per-IP rate limiting (Flask-Limiter), security headers (Flask-Talisman), multi-stage non-root Docker image
- App-factory pattern with Blueprint routing and service layer; GitHub Actions CI validates + builds on every push
- QR code returned as base64 data URI; analytics shows a 14-day click chart with zero-fill so there are no gaps

---

### [GitHub Repository Health Checker](https://github.com/gagannchandra/github-health-checker) · [Live ↗](https://repo.gaganchandra.in) · [Demo ↗](https://youtu.be/M27N7L4T-bE)
`Python` `FastAPI` `GitHub REST API` `LLaMA 3.1 (NVIDIA)`

Wanted to see if an LLM could give a structured, signal-based health report on a GitHub repo — not vibes, but actual metrics. Turns out it does reasonably well with the right prompt and data.

- Concurrently fetches 7 metrics (stars, forks, issues, contributors, last commit, license, size) — no sequential waiting
- Sends to NVIDIA-hosted LLaMA 3.1 8B Instruct; returns strengths, concerns, summary, and score out of 100
- Optional PAT raises rate limit from 60 → 5,000 req/hr; status badge (Active / Inactive / Needs Review) assigned deterministically from activity signals
- Deployed as an async FastAPI service on Render

---

### [TaskFlow — Team Task Manager](https://github.com/gagannchandra/team-task-manager) · [Live ↗](https://taskflow.gaganchandra.in)
`React 19` `Node.js` `Express` `MongoDB Atlas` `JWT` `Railway`

Built this to get real experience with role-based auth — not toy auth, but the kind where different users genuinely can and can't do different things. Tested by actually trying to break it.

- JWT + bcrypt; role middleware enforces Admin (full CRUD) vs Member (view + update assigned tasks only)
- Mongoose models for User, Project, ProjectMember, Task; `express-validator` on all inputs
- Kanban board with status tracking and team analytics dashboard; monorepo deployed on Railway

---

### [HealthAI — Disease Prediction System](https://github.com/gagannchandra/healthai-disease-prediction) · [Live ↗](https://healthai.gaganchandra.in)
`Python` `FastAPI` `Scikit-learn` `XGBoost` `React 19` `Docker` · *Final Year Project*

The core question was whether a soft-voting ensemble actually beats any single classifier here, or just adds complexity. It does help — 87.84% vs marginally lower — which was a more interesting result than a clean sweep would have been.

- Soft-voting ensemble (Decision Tree, Random Forest, Naive Bayes) on **102,238 samples** · 141 disease classes · 343 symptom features
- **87.84% accuracy** · **~5.3 ms avg latency** · **~187 req/s per core** on Render's free tier
- Returns top-3 diagnoses with confidence scores, specialist, medications, diet, and precautions from structured medical CSVs
- Voice input via Web Speech API; Recharts chart lets you compare model confidence visually

---

## Experience

**Open Source Contributor** · Remote · Jan 2026 – Present  
`Python` `C` `JavaScript`

- Fixed a GPIO debounce initialization bug in [torvalds/ScrollWheel](https://github.com/torvalds/ScrollWheel) — traced incorrect state-machine pin assignment, submitted PR with root-cause analysis
- Improved test coverage and documentation across Python and JavaScript projects; participated in issue triage and code review with distributed maintainers

---

## Skills

**Languages** — Python, JavaScript, C++, Java, SQL

**Backend** — FastAPI, Flask, Node.js, Express.js, SQLAlchemy, Pydantic, JWT Auth, Role-Based Authorization, REST API Design, Async I/O, Rate Limiting, Microservices

**AI / ML** — Scikit-learn, XGBoost, Pandas, NumPy, LLM API Integration, Model Deployment

**Databases** — PostgreSQL, MongoDB, MySQL, SQLite, Redis

**Frontend** — React, Vite, Tailwind CSS, Streamlit, Recharts

**DevOps / Tools** — Docker, GitHub Actions, CI/CD, Linux, Git, Postman, Render, Railway, Vercel, PythonAnywhere

---

## Education

**B.Tech — Computer Science & Engineering (AI Specialization)**  
Pranveer Singh Institute of Technology (PSIT), AKTU · Kanpur · Expected July 2026

Relevant coursework: Data Structures & Algorithms, OOP, OS, DBMS, Computer Networks, Software Engineering

---

## Highlights

| | |
|---|---|
| 🧪 GATE 2026 | Qualified in both CS & IT and DS & AI streams |
| 💻 DSA | 520+ problems — LeetCode, GeeksforGeeks, HackerRank |
| ⭐ HackerRank | 5-Star in Problem Solving & Python |
| 🏆 Salesforce | Agentblazer Champion — Mountaineer Rank (46+ badges) |

**Certifications:** CS50 (Harvard) · Google AI Essentials · Data Science — IBM/edX · Agile with Atlassian Jira (Coursera)

---

*Open to SDE, Backend, and ML Engineering roles. Happy to talk systems, trade-offs, or whatever you're stuck on.*  
📧 [gaganchandra02@gmail.com](mailto:gaganchandra02@gmail.com) · 💼 [linkedin.com/in/gagan-chandra](https://linkedin.com/in/gagan-chandra)
