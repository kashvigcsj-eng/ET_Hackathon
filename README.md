# NewsletterAgent 🤖📧
### AI-Powered Multi-Agent Newsletter Pipeline
**ET AI Hackathon 2026 · Problem Statement 1 · AI for Enterprise Content Operations**

---

## The Problem
A typical content team takes 3 days and ₹15,000 to produce one newsletter.
Briefing → Drafting → Compliance Review → Approvals → Final Send.
Five people. Endless back and forth. All for one email.

## The Solution
NewsletterAgent automates the entire lifecycle.
Send one email with your brief. Get a polished, compliance-checked newsletter in your inbox in under 6 minutes.

---

## How It Works
```
[Email Brief] → [Draft Agent] → [Compliance Agent] → [Human Approval] → [Publish]
```

1. **Gmail Watch** — detects incoming emails tagged `[BRIEF]`
2. **Draft Agent** — guard-railed Gemini prompt converts brief into structured newsletter
3. **Compliance Agent** — independent Gemini instance checks tone, legal, brand, spam
4. **Human Approval Gate** — reviewer gets draft + compliance report, one click to approve
5. **Gmail Send** — approved newsletter auto-publishes to distribution list

---

## Tech Stack

| Layer | Tool |
|---|---|
| Orchestration | Make.com |
| LLM Agents | Google Gemini Flash |
| Trigger & Publish | Gmail API |
| Audit Log | Google Sheets |

---

## Key Features
- ✅ 3 specialised agents — each with a separate guard-railed prompt
- ✅ Compliance guardrails — tone, legal, brand, and spam checks
- ✅ Human-in-the-loop approval gate before any content goes out
- ✅ Zero custom code — fully no-code, maintainable by any team
- ✅ Auditable — every run logged with timestamp, draft, and approval status

---

## Impact
| Metric | Before | After |
|---|---|---|
| Time per newsletter | 19 hours | 6 minutes |
| Cost per newsletter | ₹15,200 | ₹70 |
| Compliance coverage | ~60% | 100% |
| Annual saving (4/month) | — | ₹7.3 lakh |

---

## Repository Structure
```
/
├── prompts/
│   ├── draft_agent_prompt.txt
│   ├── compliance_agent_prompt.txt
│   └── polish_agent_prompt.txt
├── docs/
│   ├── NewsletterAgent_Architecture.pdf
│   └── NewsletterAgent_Impact_Model.pdf
├── screenshots/
│   ├── canvas_overview.png
│   └── module_configs/
├── scenario_blueprint.json
└── README.md
```

---

## Setup Instructions

### Prerequisites
- Make.com account (free tier works)
- Google account with Gmail
- Google Gemini API key (free from aistudio.google.com)

### Steps
1. Clone this repository
2. Go to Make.com → Create new scenario
3. Import `scenario_blueprint.json` via the Import Blueprint option
4. Connect your Gmail account via OAuth
5. Add your Gemini API key to the Google Gemini AI connection
6. Set the Gmail Watch filter to `subject:[BRIEF]`
7. Turn on the scenario — you're live!

### Testing
Send an email to your connected Gmail account with:
- Subject: `[BRIEF] Your brief title here`
- Body: describe the newsletter you want written

The pipeline will run automatically and deliver the newsletter to your inbox.

---

## Agent Prompts
All guard-railed prompts are in the `/prompts/` folder.
Each prompt enforces a fixed output schema — no hallucinations, no off-brand content.

---

## Docs
- 📄 [Architecture Document](docs/NewsletterAgent_Architecture.pdf)
- 📊 [Impact Model](docs/NewsletterAgent_Impact_Model.pdf)

---

## Built By
Kashvi · BSc Student · ET AI Hackathon 2026

*"What used to take a content team 3 days now takes 6 minutes."*
