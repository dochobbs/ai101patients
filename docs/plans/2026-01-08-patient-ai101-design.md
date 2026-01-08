# AI 101 for Patients - Design Document

**Date:** 2026-01-08
**Status:** Approved
**Parent Project:** Forked from AI 101 (provider-focused)

---

## Overview

**Purpose:** Help patients safely and effectively use AI tools like ChatGPT Health with their medical information.

**Catalyst:** OpenAI's January 2026 launch of ChatGPT Health, which allows patients to connect medical records directly to ChatGPT. With 40M+ daily health queries and 800M weekly users, patients need education on using these tools safely.

**Target Audience:** All patients - broad accessibility, no technical background assumed.

---

## Core Principles

- Plain language first, optional depth for curious readers
- Safety and practical skills equally weighted
- Self-paced, bite-sized modules (10-15 min each)
- Actionable, not academic - minimal sources, maximum usefulness
- Tool-agnostic principles with ChatGPT Health as primary example

---

## Project Structure

**Location:** `/Users/dochobbs/Downloads/ai101-patients/`
**Repository:** Separate git repo from provider site

```
ai101-patients/
├── index.html              # Landing page with module cards
├── styles.css              # Forked from provider site
├── favicon.png             # Site icon
├── images/                 # Patient-relevant images/screenshots
├── docs/
│   └── plans/              # Design documents
├── [module pages].html     # 14 module pages
└── modules/                # Downloadable resources (if any)
```

---

## Content Design

### Reading Level
- **Core content:** Plain language (6th-8th grade)
- **Learn More sections:** Optional deeper content for curious readers
- **No required readings:** Just optional links

### Callout Box System

| Type | Purpose | Visual |
|------|---------|--------|
| **Pearl** | Practical tips, memorable takeaways | Highlight/tip style |
| **In the News** | Recent headlines with context | News style |
| **Try This** | Hands-on mini-activities | Activity style |
| **Warning** | Safety-critical information | Alert/danger style |
| **Learn More** | Optional deeper content | Expandable `<details>` |

---

## Module Structure (14 Modules)

### Getting Started
1. **Start Here** (`start-here.html`)
   - What this site is, why AI literacy matters now
   - How to use these modules
   - The ChatGPT Health moment

### Safety Foundation (4 modules)
2. **What AI Can and Can't Do** (`what-ai-can-do.html`)
   - Setting realistic expectations
   - AI isn't a doctor
   - Strengths and limitations

3. **Your Privacy and Health Data** (`privacy-health-data.html`)
   - The HIPAA gap explained (AI companies aren't covered entities)
   - What happens to your data in ChatGPT Health
   - Making informed choices about sharing

4. **Spotting AI Mistakes** (`spotting-mistakes.html`)
   - Hallucinations - confident-sounding errors
   - Outdated information
   - How to verify AI claims

5. **When to Trust AI vs. Call Your Doctor** (`when-to-call-doctor.html`)
   - Red flags that need human care
   - Emergencies - never use AI
   - When AI is helpful vs. harmful

### Practical Skills (6 modules)
6. **AI Tools You Should Know** (`ai-tools.html`)
   - **Big Chatbots:** ChatGPT/ChatGPT Health, Claude, Gemini, Copilot
   - **AI Search:** Perplexity, Google AI Overviews, Bing Chat
   - **Specialized:** NotebookLM, Sora 2, Nano Banana Pro
   - **Health-Focused:** Ada, K Health, AI telehealth platforms
   - What each does well, limitations, data access differences

7. **ChatGPT Health Deep Dive** (`chatgpt-health.html`)
   - How to connect your records (b.well integration)
   - What it can access (320+ health plans, 2.2M providers)
   - Privacy settings and controls
   - Hands-on walkthrough
   - Connected apps: Apple Health, Peloton, MyFitnessPal

8. **How to Talk to AI About Your Health** (`talking-to-ai.html`)
   - Prompting basics for patients
   - Being specific about your situation
   - Providing helpful context
   - Example prompts that work

9. **Understanding AI Responses** (`understanding-responses.html`)
   - What's reliable vs. questionable
   - Checking sources and claims
   - Healthy skepticism
   - When responses conflict with your doctor

10. **Preparing for Doctor Appointments** (`doctor-appointments.html`)
    - Using AI to organize your questions
    - Summarizing symptoms and concerns
    - Understanding your options before visits
    - What to bring vs. what to verify

11. **Researching Your Health Safely** (`researching-safely.html`)
    - Looking up conditions without spiraling
    - Medication and treatment research
    - Separating good info from bad
    - When to stop researching and call someone

### Optional/Advanced (3 modules)
12. **How AI "Thinks"** (`how-ai-thinks.html`)
    - Simplified LLM explainer
    - Why AI makes the mistakes it makes
    - Training data and its limits
    - Why AI sounds confident even when wrong

13. **AI Bias and Your Health** (`ai-bias.html`)
    - Why AI might give different answers to different people
    - Training data gaps
    - Health equity concerns
    - What to watch for

14. **The Future of AI in Healthcare** (`future-ai-healthcare.html`)
    - What's coming next
    - AI in your doctor's office
    - Staying informed as things change

---

## Page Template Structure

```
Header
├── Site logo/title
├── Module navigation
└── Progress indicator (optional)

Hero Section
├── Module title
├── Time estimate ("10 min read")
└── One-sentence summary

Core Content
├── Plain language main content
├── Callout boxes (Pearl, In the News, Try This, Warning)
├── "Learn More" expandable sections (<details>)
└── Images/diagrams where helpful

Bottom Section
├── Key Takeaways (3-5 bullets)
├── "Next Module" navigation
└── "Questions for Your Doctor" (where relevant)

Footer
```

---

## Technical Implementation

### Forked from Provider Site
- `styles.css` - Full design system (3,156 lines)
- `favicon.png` - Site icon
- HTML structure and navigation patterns
- Callout box CSS classes

### Design System (inherited)
- **Typography:** Fraunces (headers), Source Sans 3 (body), JetBrains Mono (code)
- **Colors:** Keep provider site phase colors or adapt slightly
- **Spacing:** 8-point system
- **Responsive:** Breakpoints at 900px and 600px

### New CSS Additions
- Pearl callout style
- In the News callout style
- Learn More expandable sections (using `<details><summary>`)

---

## What We're NOT Including (for now)

- Companion Flask app (Spark chatbot)
- RSS feed
- Separate glossary page (terms woven into modules)
- Academic reading lists and citations
- Facilitator guides
- 12-week curriculum structure

---

## Key Differences from Provider Site

| Aspect | Provider Site | Patient Site |
|--------|---------------|--------------|
| Audience | Clinicians, medical learners | All patients |
| Reading level | College-level | Plain language + optional depth |
| Structure | 12-week curriculum | Self-paced modules |
| Sources | Extensive academic readings | Minimal, optional |
| Focus | Governance, supervision, liability | Safety, practical skills |
| Companion app | Spark (Flask) | None (for now) |
| ChatGPT Health | Reference | Major dedicated module |

---

## ChatGPT Health Context

**Launched:** January 7, 2026

**Key Features:**
- Dedicated health tab, isolated from other chats
- Medical record connection via b.well (2.2M+ providers, 320+ plans)
- Wellness app integration (Apple Health, Peloton, MyFitnessPal)
- Not used for model training
- US-only for medical records, requires ChatGPT Free/Go/Plus/Pro

**Privacy Reality:**
- NOT covered by HIPAA (OpenAI isn't a covered entity)
- Self-regulated, no federal oversight
- Encrypted, stored separately
- User controls what's shared

**Scale:**
- 800M weekly active users
- 25% ask health questions weekly
- 40M+ daily medical/health insurance queries

---

## Files to Create

| File | Status |
|------|--------|
| `index.html` | To create |
| `styles.css` | Fork from provider |
| `favicon.png` | Fork from provider |
| `start-here.html` | To create |
| `what-ai-can-do.html` | To create |
| `privacy-health-data.html` | To create |
| `spotting-mistakes.html` | To create |
| `when-to-call-doctor.html` | To create |
| `ai-tools.html` | To create |
| `chatgpt-health.html` | To create |
| `talking-to-ai.html` | To create |
| `understanding-responses.html` | To create |
| `doctor-appointments.html` | To create |
| `researching-safely.html` | To create |
| `how-ai-thinks.html` | To create |
| `ai-bias.html` | To create |
| `future-ai-healthcare.html` | To create |

---

## Sources

- [OpenAI Introduces ChatGPT Health](https://openai.com/index/introducing-chatgpt-health/)
- [b.well Partnership Press Release](https://www.prnewswire.com/news-releases/openai-selects-bwell-to-power-secure-health-data-connectivity-for-ai-driven-health-experiences-in-chatgpt-302655598.html)
- [Privacy Concerns - Decrypt](https://decrypt.co/353919/openai-users-medical-data-ai-chatgpt-privacy-concerns)
