# Valdrix Systems — Website Build & Deploy Instructions
> Use this file with Claude Code in VS Code to build and deploy your website to GitHub Pages

---

## 🎯 Project Overview

**Goal:** Build a professional one-page website for Valdrix Systems LLC and deploy it free on GitHub Pages, connected to valdrixsystems.com

**Stack:** Pure HTML + CSS + JavaScript (no frameworks needed)

**Hosting:** GitHub Pages (free forever)

**Domain:** valdrixsystems.com (purchased on Namecheap)

---

## 📋 About Valdrix Systems

Use this information when building the website:

### Company Details
- **Company Name:** Valdrix Systems LLC
- **Tagline:** Software Engineering & IT Consulting
- **Email:** samuel@valdrixsystems.com
- **Phone:** 954-702-7152
- **Location:** Remote — Based in the United States

### What Valdrix Does
Valdrix Systems is a software engineering and IT consulting firm providing full-stack development, backend systems, CI/CD automation, and technical program support to commercial and government clients.

### Services To Highlight
1. **Full-Stack Software Development** — End-to-end application development using Python, C#, React, TypeScript, Java, C++
2. **Backend API & Systems Engineering** — Scalable backend services, data pipelines, and multi-source data workflows
3. **CI/CD Pipeline Engineering** — Automated build, test, and deployment pipelines using GitLab CI/CD and Docker
4. **Technical Program Support** — Technical leadership, architecture decisions, stakeholder management
5. **IT Consulting** — System modernization, legacy migration, DevSecOps

### Key Differentiators
- Active Final Top Secret Security Clearance
- 5+ years delivering mission-critical defense systems at Johns Hopkins APL
- Technical Lead experience on classified government programs
- Full-stack expertise across 15+ programming languages
- Available for fully remote engagements

### Tech Stack (for a skills section)
Python, C#, Java, C++, React, TypeScript, JavaScript, SQL, PostgreSQL, MATLAB, GitLab CI/CD, Docker, Git, Linux, Agile/Scrum

---

## 🎨 Design Direction

Build a website that feels like a serious defense/tech company — NOT a generic freelancer site.

**Aesthetic:** Dark, sophisticated, military-tech inspired
- Dark background (near black — #0a0a0f or similar)
- Electric blue or cyan accent color (#00d4ff or similar)
- Clean, sharp typography — suggest using Google Fonts: "Space Grotesk" or "IBM Plex Mono" for headings
- Subtle grid or circuit-board texture in background
- Minimal animations — professional, not flashy
- Think: Anduril, Palantir, Rebellion Defense vibes

**Layout (Single Page):**
1. Hero section — company name, tagline, CTA button
2. About section — what Valdrix does
3. Services section — 4-5 service cards
4. Tech stack — logos or text list
5. Contact section — email, phone, contact form (mailto link is fine)
6. Footer — copyright, LLC notice

---

## 🛠️ Step-by-Step Build Instructions for Claude Code

### Prompt 1 — Initial Setup
Tell Claude Code:
```
Create a professional one-page website for Valdrix Systems LLC, a software engineering and IT consulting firm. 

Use pure HTML, CSS, and JavaScript (no frameworks). 

Design direction: Dark sophisticated military-tech aesthetic. Dark background (#0a0a0f), electric blue/cyan accents (#00d4ff), clean sharp typography using IBM Plex Mono from Google Fonts for headings and IBM Plex Sans for body text.

Create these files:
- index.html
- styles.css  
- script.js

The website should have these sections:
1. Navigation bar — logo (Valdrix Systems) + nav links
2. Hero — "Valdrix Systems" heading, tagline "Software Engineering & IT Consulting", brief description, "Get In Touch" CTA button
3. About — what the company does, mention government and commercial clients, mention remote capability
4. Services — 6 service cards: Full-Stack Development, Backend Systems, CI/CD Automation, Technical Leadership, IT Consulting, DevSecOps
5. Tech Stack — clean display of: Python, C#, Java, C++, React, TypeScript, SQL, GitLab CI/CD, Docker, Linux
6. Contact — email: samuel@valdrixsystems.com, phone: 954-702-7152
7. Footer — "© 2026 Valdrix Systems LLC. All Rights Reserved."

Make it look like Anduril or Palantir's website — serious, professional, defense-tech aesthetic. Subtle animations on scroll. Mobile responsive.
```

### Prompt 2 — Review & Refine
After Claude Code generates the files, open them in a browser (right-click index.html → Open in Browser) and tell Claude Code:
```
Review the website and make these improvements:
- Make sure it's fully mobile responsive
- Add a subtle animated background (moving particles or grid lines — keep it subtle)
- Make the navigation sticky so it follows on scroll
- Add smooth scroll behavior when clicking nav links
- Make the hero section full viewport height
- Ensure all text is readable and professional
```

### Prompt 3 — Final Polish
```
Final polish:
- Add a favicon (simple "V" letter in the brand color)
- Make sure all links work
- Add meta tags for SEO (title, description, keywords)
- Ensure the site loads fast — no unnecessary resources
- Double check mobile layout on narrow screens
```

---

## 🚀 Deploy to GitHub Pages

### Step 1 — Create GitHub Account
1. Go to **github.com**
2. Sign up with your personal email
3. Choose a username (suggestion: **valdrix-systems** or **samuelavrahami**)

### Step 2 — Create New Repository
1. Click the **"+"** icon top right
2. Click **"New repository"**
3. Name it exactly: **valdrixsystems.github.io** (this is important!)
   - OR name it anything and use a custom domain
4. Set to **Public**
5. Check **"Add a README file"**
6. Click **"Create repository"**

### Step 3 — Upload Your Files
**Option A: Via GitHub website (easiest)**
1. Open your repository
2. Click **"Add file"** → **"Upload files"**
3. Drag and drop your index.html, styles.css, script.js
4. Click **"Commit changes"**

**Option B: Via VS Code + Git (cleaner)**
```bash
# In VS Code terminal:
git init
git add .
git commit -m "Initial Valdrix Systems website"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
```

### Step 4 — Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **"Settings"** tab
3. Click **"Pages"** in the left sidebar
4. Under **"Source"** select **"Deploy from a branch"**
5. Select **"main"** branch, **"/ (root)"** folder
6. Click **"Save"**
7. Wait 2-3 minutes
8. GitHub will show you your site URL (yourname.github.io/yourrepo)

---

## 🌐 Connect valdrixsystems.com Domain

### Step 1 — Add Custom Domain in GitHub Pages
1. In GitHub Settings → Pages
2. Under **"Custom domain"** type: **valdrixsystems.com**
3. Click **"Save"**
4. GitHub will create a CNAME file in your repo

### Step 2 — Update DNS in Namecheap
1. Go to **namecheap.com** → Domain List → Manage → Advanced DNS
2. Delete the existing URL Redirect Record (the parking page one)
3. Add these 4 A Records:

| Type | Host | Value | TTL |
|------|------|-------|-----|
| A Record | @ | 185.199.108.153 | Automatic |
| A Record | @ | 185.199.109.153 | Automatic |
| A Record | @ | 185.199.110.153 | Automatic |
| A Record | @ | 185.199.111.153 | Automatic |

4. Add this CNAME Record:

| Type | Host | Value | TTL |
|------|------|-------|-----|
| CNAME | www | YOUR_GITHUB_USERNAME.github.io | Automatic |

5. Save all changes

### Step 3 — Wait for DNS Propagation
- DNS changes take **24-48 hours** to fully propagate
- After propagation, valdrixsystems.com will show your website
- GitHub Pages will also automatically provide a **free SSL certificate** (https://)

### Step 4 — Enforce HTTPS
1. Go back to GitHub Settings → Pages
2. Check **"Enforce HTTPS"** checkbox
3. Your site is now secure at **https://valdrixsystems.com**

---

## 📁 Final File Structure

Your project should look like this:
```
valdrix-website/
├── index.html          # Main HTML file
├── styles.css          # All styling
├── script.js           # Animations and interactions
├── CNAME               # Created by GitHub (contains: valdrixsystems.com)
└── README.md           # Optional project description
```

---

## ✅ Final Checklist Before Going Live

- [ ] Website looks professional on desktop
- [ ] Website looks good on mobile (test on your phone)
- [ ] All sections present: Hero, About, Services, Tech Stack, Contact, Footer
- [ ] Email link works (clicking email opens mail app)
- [ ] No spelling errors
- [ ] Company name spelled correctly: **Valdrix Systems LLC**
- [ ] Contact information correct: samuel@valdrixsystems.com / 954-702-7152
- [ ] Copyright year is 2026
- [ ] Files uploaded to GitHub
- [ ] GitHub Pages enabled
- [ ] Custom domain connected in GitHub Pages settings
- [ ] DNS A records added in Namecheap
- [ ] HTTPS enforced

---

## 💡 Tips for Using Claude Code

- Open the entire project folder in VS Code before starting
- Use **"Open Preview"** in VS Code to see HTML changes live
- Ask Claude Code to fix one thing at a time — don't ask for too many changes at once
- If something looks wrong, screenshot it and describe what needs to change
- After every major change, refresh the browser preview to check

---

## 🆘 Common Issues & Fixes

| Problem | Fix |
|---------|-----|
| Site not showing at valdrixsystems.com | DNS hasn't propagated yet — wait 24-48 hours |
| GitHub Pages not working | Make sure repository is Public and Pages is enabled |
| HTTPS not working | Wait for GitHub to issue SSL cert (can take a few hours) |
| Mobile layout broken | Ask Claude Code to fix responsive CSS |
| Fonts not loading | Check Google Fonts link is in the HTML head section |

---

*Created May 31, 2026 — Valdrix Systems LLC*
