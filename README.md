# 🔐 The Strongest Link
## People Security Risk Management (PSRM)

> **Simulate. Educate. Strengthen the Human Layer.**

The Strongest Link is a **People Security Risk Management (PSRM)** platform built to help organizations identify, measure, and reduce human-factor security risks through realistic phishing simulations and security awareness campaigns.

---

## 🤔 What Is PSRM?

In cybersecurity, the most sophisticated firewall can be bypassed by a single employee clicking the wrong link. **People are both the greatest vulnerability and the greatest asset** in any security posture.

**The Strongest Link** addresses this by providing:

- 🎣 **Phishing Simulations** — Send realistic phishing emails to employees to test their vigilance
- 📊 **Risk Scoring** — Track who clicked, who submitted credentials, who reported the email
- 🎓 **Awareness Training** — Redirect susceptible users to training content automatically
- 📈 **Campaign Analytics** — Measure improvement over time across teams and departments
- 🔁 **Repeat Testing** — Run ongoing campaigns to build a security-aware culture

---

## 💡 Why "The Strongest Link"?

Security awareness programs traditionally focus on the *weakest* link. We believe every person in an organization *can become* the strongest line of defense — with the right education, practice, and feedback loop.

```
Traditional mindset:  Humans = Weakest Link  ❌
Our mindset:          Humans = Strongest Link (with training) ✅
```

---

## ✅ Key Features

| Feature | Description |
|---|---|
| **Campaign Management** | Create and schedule phishing campaigns across groups |
| **Email Templates** | Library of realistic phishing email templates |
| **Landing Pages** | Convincing credential-capture pages for simulation |
| **Sending Profiles** | Configure SMTP sending infrastructure |
| **User Groups** | Organize targets by department, role, or risk level |
| **Real-Time Dashboard** | Live tracking of opens, clicks, submissions, and reports |
| **Results Export** | Download campaign results as CSV for reporting |
| **REST API** | Full API for integration with SIEM, HRIS, or LMS systems |
| **Webhooks** | Push events to external systems in real-time |

---

## 🚀 Quick Start

### Prerequisites

- Go 1.10+
- Node.js & npm (for building frontend assets)

### Build from Source

```bash
# Clone the repository
git clone https://github.com/kholiffaiz/the-strongest-link-psrm.git
cd the-strongest-link-psrm

# Build
go build -o the-strongest-link

# Run
./the-strongest-link
```

Access the dashboard at: `http://localhost:3333`

Default credentials:
- **Username:** `admin`
- **Password:** *(generated on first run — check terminal output)*

### Docker

```bash
docker build -t the-strongest-link .
docker run -p 3333:3333 the-strongest-link
```

---

## 🗂️ Architecture

```
the-strongest-link-psrm/
├── controllers/        # API route handlers
├── models/             # Database models (SQLite)
├── static/             # Frontend assets (JS, CSS)
├── templates/          # Go HTML templates
├── db/                 # Database migrations
├── mailer/             # Email sending engine
├── webhook/            # Webhook dispatcher
└── config.json         # Runtime configuration
```

---

## ⚙️ Configuration

Edit `config.json` before running:

```json
{
  "admin_server": {
    "listen_url": "0.0.0.0:3333",
    "use_tls": false
  },
  "phish_server": {
    "listen_url": "0.0.0.0:80",
    "use_tls": false
  },
  "db_name": "sqlite3",
  "db_path": "the-strongest-link.db",
  "logging": {
    "filename": ""
  }
}
```

---

## 📡 REST API

The Strongest Link exposes a full REST API for automation and integration.

```bash
# Authenticate
curl -X POST http://localhost:3333/api/login \
  -H "Content-Type: application/json" \
  -d '{"username":"admin","password":"yourpassword"}'

# List campaigns
curl -H "Authorization: Bearer YOUR_API_KEY" \
  http://localhost:3333/api/campaigns/
```

Full API documentation available at `/api/` on your running instance.

---

## 🔒 Security & Ethics

> **⚠️ IMPORTANT:** This platform is intended **exclusively** for authorized security awareness testing within your own organization.

- Only run campaigns against users/employees covered by organizational policy
- Never use against external targets without explicit written authorization
- Ensure compliance with local privacy laws (GDPR, PDPA, etc.)
- Simulation-captured credentials should be deleted immediately after analysis

---

## 📄 License

Distributed under the **MIT License**.

---

*The Strongest Link — because every person in your organization can be a security asset, not a liability.*
