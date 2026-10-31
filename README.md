# Campus Pulse 🎓⚡
> Real-time intelligent campus incident reporting, sentiment tracking, and resolution workflow.

Built during **PROMPTWARS × CSSS 2026** (MIT Moradabad) in collaboration with Google for Developers & Hack2Skill.

---

## 📌 Problem Overview
Campuses often suffer from fragmented communication when dealing with student grievances, infrastructure breakdowns (labs, Wi-Fi, sanitation), and urgent administrative announcements. Traditional complaint forms are slow, unstructured, and lack automated triage.

**Campus Pulse** bridges this gap by leveraging Generative AI to automatically parse, classify, prioritize, and route student reports to the correct department while keeping the campus community updated in real time.

---

## 🚀 Key Features

### 1. 🧠 Smart Grievance Parsing
- Powered by **Google Gemini Flash API** via Google AI Studio.
- Automatically analyzes informal, messy student complaint descriptions into:
  - Concise synthesized headline
  - Actionable department routing (*Hostel & Housing*, *IT & Campus Network*, *Academic Affairs*, *Facilities & Maintenance*, *Sanitation & Hygiene*, *Campus Security*, *Student Welfare*)
  - Inferred campus premises/location (*CS Lab 3*, *Hostel B 2nd Floor*, *LH 204*, *Central Library*)
  - Dual-mode architecture: seamlessly connects to live Gemini Flash API with built-in instant NLP heuristic fallback.

### 2. 🚨 Urgency Scoring & SLA Triage
- High Severity (*4-hour resolution SLA target*, highlighted with pulsing indicators)
- Medium Priority (*24-hour SLA*)
- Low Priority (*72-hour SLA*)
- Live SLA tracking and countdown metrics.

### 3. 📜 Formal Petition & Ticket Generation
- Converts raw, informal student frustration into a structured, highly articulate administrative brief and petition.
- Includes official subject line, addressed university authority (*Dean of Student Welfare, Chief Warden, IT Administrator*), factual context, student impact assessment, and recommended corrective action.
- 1-click clipboard copy and print-ready document view.

### 4. 📊 Real-Time Sentiment & Campus Hotspots Analytics
- Live breakdown of campus sentiment (*Urgent/Critical, Frustrated, Concerned, Neutral*).
- Active campus incident hotspots counter identifying recurring failure points.
- Department load distribution bar visualization.

### 5. 👥 Student Endorsements & Resolution Workflow
- Interactive "Endorse" (Upvote) feature with confetti feedback to validate community impact.
- Live administrative status pipeline (*Reported* ➔ *In Triage* ➔ *Assigned* ➔ *Resolved*).
- Anonymous reporting toggle for sensitive student grievances.

---

## 🛠️ Tech Stack
- **Framework:** Next.js 15 (App Router), React 19, TypeScript
- **Styling:** Tailwind CSS (with seamless dark/light mode and custom animations)
- **AI Core:** Google Gemini Flash API (`gemini-1.5-flash`) via Google AI Studio (`@google/generative-ai`)
- **Icons & Micro-interactions:** Lucide React, Canvas Confetti
- **Deployment:** Vercel-ready

---

## ⚙️ Getting Started Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/adhayanvishnoi9-stack/campus-pulse-.git
   cd campus-pulse-
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure Environment Variable (Optional):**
   Copy `.env.example` to `.env.local` and add your Google Gemini API key:
   ```bash
   cp .env.example .env.local
   ```
   Add your key:
   ```env
   GEMINI_API_KEY=your_gemini_api_key_here
   ```
   *(Note: You can also configure or test your Gemini API key directly through the in-app modal at any time, or use the built-in fallback NLP engine without any API key!)*

4. **Run the development server:**
   ```bash
   npm run dev
   ```

5. **Open in browser:**
   Open [http://localhost:3000](http://localhost:3000) to view Campus Pulse.

6. **Production Build:**
   ```bash
   npm run build
   ```

---

## 🏫 Developed For
**PROMPTWARS × CSSS 2026** — MIT Moradabad  
In collaboration with **Google for Developers & Hack2Skill**.
