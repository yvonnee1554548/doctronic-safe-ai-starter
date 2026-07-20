# doctronic-safe-ai-starter

Fork, clone, and harden a vulnerable AI prescription system inspired by the real Doctronic incident - build safe validation, audit trails, and tests from scratch.

## The Incident

In January 2026, an AI system called Doctronic accepted a fabricated regulatory bulletin and generated a dangerously incorrect prescription dosage recommendation. No input validation. No audit trail. No safety checks. Full writeup: [`docs/incident-summary.md`](docs/incident-summary.md).
Over the course of today, you'll rebuild it into something safer, one module at a time.

## What You'll Build

No prior coding or AI background needed. We'll go step by step, and each step fixes one specific way the real Doctronic system failed. Check off each one as you finish it - by the end, your commit history tells the story of how you turned a broken system into a safe one.

- [ ] **How the app talks to the world (APIs)** - See how a piece of software receives information from outside, like a restaurant taking an order through a menu. This is how Doctronic received the fake bulletin in the first place.
- [ ] **Checking your inputs ((Data Types & Pydantic)** - Add rules so the system rejects junk or fake information instead of blindly trusting it. Doctronic never did this - it accepted a made-up bulletin without question. 
- [ ] **Teaching the system to make decisions (Logic through if-else)** - Add "if this, then that" rules so the system can catch a dangerous dosage before it's ever recommended.
- [ ] **Doing things automatically (loops)** - Get the system to repeat a check across many inputs instead of doing it one at a time by hand.
- [ ] **Organizing the code (functions)** - Break the system into clear, reusable pieces.
- [ ] **Keeping a record (databases & audit trails)** - Every decision the system makes gets logged, so if something goes wrong, you can trace exactly what happened and why. Doctronic kept no such record.
- [ ] **Making sure it actually works (testing)** - Write simple checks that automatically catch mistakes before they reach a real patient.
- [ ] **Turning numbers into pictures (data visualization basics)** - Learn how to pick the right chart for your data, and how to spot a chart that's misleading you.
- [ ] **Building a simple dashboard (Streamlit)** - Turn your audit trail and safety checks into a live, visual dashboard anyone can look at - no web design experience needed.

## Getting Started

1. **Fork this repo** (top right → Fork) - this creates your own copy under your GitHub account
2. **Clone your fork** (not this original!):
   ```bash
   git clone https://github.com/<your-username>/doctronic-safe-ai-starter.git
   cd doctronic-safe-ai-starter
   ```
3. **Set up your environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate      # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
4. **Commit as you go**, at each checkpoint above:
   ```bash
   git add .
   git commit -m "Add Pydantic validation to bulletin input"
   git push origin main
   ```

## Repo Structure

```
doctronic-safe-ai-starter/
├── README.md #this file briefing you on where to start
├── docs/
│   └── incident-summary.md   # the real case, in brief
├── app/
│   ├── main.py                # FastAPI entrypoint
│   ├── models/                 # you'll add Pydantic schemas here
│   ├── routes/
│   │   └── bulletin.py         # the vulnerable endpoint - fix this
│   ├── db/                     # you'll add audit trail logic here
└── tests/                      # you'll add tests here
```

By the end of today, this repo - under *your* GitHub account - is yours to keep and show off.
