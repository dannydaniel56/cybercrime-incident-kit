# cybercrime-incident-kit
An educational toolkit for documenting and organizing suspected cyber incidents.
# 🛡️ Cybercrime Incident Kit

A small, educational toolkit for documenting and organizing information about suspected cybercrime and cybersecurity incidents.

When something goes wrong online, it can be surprisingly difficult to remember exactly **what happened, when it happened, and what evidence was available**. This project provides simple templates and examples that make incident documentation easier.

> **Educational project:** This toolkit is designed for documentation and awareness. It does not investigate attackers, access systems, or provide offensive security capabilities.

---

## What Is This?

The **Cybercrime Incident Kit** is a collection of simple resources for recording information about online security incidents.

It can be useful for documenting situations such as:

* Suspicious account access
* Phishing attempts
* Online scams and suspicious transactions
* Identity misuse
* Unauthorized access
* Website security incidents
* Suspicious emails or messages
* Possible data exposure
* Online harassment or threats

The project focuses on **recording what happened**, rather than trying to investigate or identify the person responsible.

---

##  Repository Structure

```text
cybercrime-incident-kit/
│
├── README.md
│
├── templates/
│   ├── incident-report.md
│   ├── evidence-checklist.md
│   └── timeline.md
│
├── examples/
│   └── sample-incident.json
│
└── scripts/
    └── create_incident.py
```

---

##  Incident Documentation

A good incident report should start with basic facts.

For example:

```text
Incident date:
Incident time:
Affected system:
Affected account:
Incident type:
How it was discovered:
Initial actions taken:
Current status:
```

Try to record information as soon as possible instead of relying on memory later.

The full reusable report template is available in:

```text
templates/incident-report.md
```

---

##  Create a Timeline

A timeline can help turn a confusing incident into a sequence of events.

Example:

```text
09:15 — Suspicious login notification received
09:18 — Account activity reviewed
09:22 — Password changed
09:30 — Relevant notifications saved
09:45 — Incident documented
```

The goal isn't to make assumptions about what happened. The goal is to record **observable events in chronological order**.

A reusable timeline template is available in:

```text
templates/timeline.md
```

---

##  Evidence Checklist

Depending on the situation, potentially useful records may include:

```text
[ ] Date and time
[ ] Affected account or system
[ ] Screenshots
[ ] Relevant URLs
[ ] Login/access records
[ ] Emails or messages
[ ] Transaction records
[ ] Server/application logs
[ ] Error reports
[ ] Notifications
[ ] Timeline of events
[ ] Actions taken
```

Not every incident will require every item.

The important thing is to preserve relevant information appropriately and avoid altering or deleting useful records unnecessarily.

See:

```text
templates/evidence-checklist.md
```

for the reusable checklist.

---

##  JSON Incident Record

Incident information can also be stored in a structured format such as JSON.

Example:

```json
{
  "incident_id": "INC-001",
  "reported_at": "2026-10-06T09:15:00",
  "type": "Suspicious login",
  "affected_system": "example.com",
  "status": "investigating",
  "evidence": [
    "login-notification.png",
    "activity-log.txt"
  ]
}
```

The example is available at:

```text
examples/sample-incident.json
```

###  Never Store Secrets

Do **not** put sensitive credentials into incident reports or Git repositories.

Never commit:

```text
passwords
API keys
private keys
session tokens
authentication cookies
access tokens
database credentials
```

If sensitive information appears in a log, remove or securely handle it before sharing the file.

---

##  Simple Python Example

This project also contains a small Python script that creates a basic incident record.

```python
from datetime import datetime
import json

incident = {
    "incident_id": "INC-001",
    "reported_at": datetime.now().isoformat(),
    "type": "Suspicious login",
    "affected_system": "example.com",
    "status": "investigating"
}

with open("incident.json", "w", encoding="utf-8") as file:
    json.dump(incident, file, indent=2)

print("Incident record created: incident.json")
```

The script is intentionally simple.

It does **not** scan networks, collect credentials, identify attackers, or access another person's system.

You can find it here:

```text
scripts/create_incident.py
```

---

##  Basic Incident-Response Principles

When documenting a suspected cyber incident:

### 1. Record facts

Write down what you actually observed instead of making assumptions.

### 2. Preserve useful information

Relevant logs, notifications, messages, and timestamps may help explain what happened.

### 3. Protect sensitive information

Incident documentation can contain private information. Store it securely and don't publish confidential data.

### 4. Use timestamps

Dates and times make it easier to build an accurate sequence of events.

### 5. Keep copies where appropriate

When possible, work with copies of files rather than unnecessarily modifying original records.

### 6. Don't retaliate

If you believe someone attacked an account or system, don't attempt to break into their system in response.

### 7. Report serious incidents

Depending on the circumstances, use appropriate platform, organizational, cybersecurity, or law-enforcement reporting channels.

---

##  Project Workflow

The basic idea behind this project is:

```text
       OBSERVE
          ↓
       RECORD
          ↓
      PRESERVE
          ↓
       REVIEW
          ↓
   REPORT IF NEEDED
```

This isn't a replacement for professional incident response.

It's simply a way to avoid the common problem of having important information scattered across screenshots, messages, emails, and memory.

---

##  Example Scenario

Imagine you receive an unexpected login notification.

Instead of immediately deleting the notification, you could record:

```text
Date: 2026-10-06
Time: 09:15
Incident: Unexpected account login
Affected account: example@example.com
Action: Password changed
Evidence: Login notification + account activity
Status: Investigating
```

You can then create a timeline of what happened before and after the notification.

This creates a much clearer record than simply writing:

> "Someone hacked my account."

The first version contains information that can actually be reviewed.

---

##  What This Project Does NOT Do

This repository is intentionally limited.

It does not:

* ❌ Hack accounts
* ❌ Identify attackers
* ❌ Track people
* ❌ Steal credentials
* ❌ Scan systems without authorization
* ❌ Exploit vulnerabilities
* ❌ Bypass authentication
* ❌ Conduct surveillance
* ❌ Replace professional digital forensics

The purpose is **documentation, education, and awareness**.

---

##  Contributing

Suggestions and improvements are welcome.

If you want to contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Test your changes.
5. Open a pull request.

Useful contributions could include:

* Better incident-report templates
* Additional documentation examples
* Improvements to the Python script
* Privacy and security guidance
* Better Markdown organization
* Translations of the templates

Please keep contributions focused on **defensive, educational, and documentation purposes**.

---

##  Disclaimer

This project is provided for educational and informational purposes.

The templates and examples are not professional legal advice, cybersecurity advice, or digital-forensics guidance.

Only access systems, accounts, files, and information that you are authorized to access.

If an incident involves serious financial loss, threats, unauthorized access, personal-data exposure, or other potentially criminal activity, consider contacting the appropriate professional or reporting authority.

---

## 📜 License

This project is available under the **MIT License**.

You are free to use, modify, and distribute the project according to the terms of the license.

---

##  Why This Project Exists

Cybersecurity discussions often focus on preventing attacks.

Prevention is important, but when something actually happens, **documentation matters too**.

A clear timeline, organized records, and careful handling of evidence can make it much easier to understand an incident and decide what to do next.

That's the simple idea behind the **[Cybercrime Incident Kit](https://www.solicitor.pk/cyber-lawyer/)**.

```text
Good security prevents problems.

Good documentation helps you understand them.
```
