# ✈️ PiLOT — Precision Engineered Ambition

> **The ultimate abroad study guide for Bangladeshi students** — built as a single, fully self-contained HTML file with zero dependencies.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20Site-blue?style=for-the-badge)](https://your-username.github.io/pilot)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)]()
[![Made For](https://img.shields.io/badge/Made%20For-BD%20Students-red?style=for-the-badge)]()

---

## 🌟 What is PiLOT?

PiLOT is a comprehensive, offline-capable web application that guides Bangladeshi students through every step of studying abroad — from choosing a university to landing at the airport. It is written in a **single HTML file** (~7,800 lines) with all CSS and JavaScript embedded inline.

---

## 🚀 Features

### 🎯 Profile Matcher Engine
Smart form that filters universities by CGPA, subject, country, degree level, and budget — instantly showing matched universities with acceptance likelihood.

### 🌍 Interactive 3D University Globe
A fully custom WebGL-style canvas globe with:
- 31 universities plotted across 7 countries
- Drag to rotate, hover for tooltips
- Click any dot → info panel with full university name, country flag, and direct website link
- Country labels rendered on the globe surface
- Depth-based sizing (near = large, far = small)

### 🏫 University Database
**47+ universities** across 9 countries with complete data per institution:
- Official minimum GPA + hidden competitive cutoff
- GRE/IELTS requirements
- Annual tuition in USD
- BD students accepted per year
- Scholarship tags (full/partial)
- Hidden requirements specific to Bangladeshi applicants
- Direct official website links

**Countries covered:** 🇺🇸 USA · 🇨🇦 Canada · 🇩🇪 Germany · 🇬🇧 UK · 🇦🇺 Australia · 🇯🇵 Japan · 🇰🇷 S. Korea · 🇨🇳 China · 🇪🇺 Europe

### 💰 Real-Time Cost Calculator (BDT)
Live currency conversion engine showing full cost of studying abroad in Bangladeshi Taka — tuition, living, visa, flights, insurance.

### 📚 Test Prep Guide (IELTS · TOEFL · GRE · GMAT · SAT)
Complete free prep roadmaps for all 5 major tests:
- Month-by-month study plan
- Free resource cards with direct links
- BD-specific tips and registration info
- Target scores per university tier

### 📋 Country-Specific Checklist
Complete document checklist (passport → flight) for USA, Canada, Germany, and UK — nothing missed.

### 🗓️ 365-Day Action Calendar
Visual roadmap from 3rd year of university to flight date — every milestone mapped out month by month.

### 💼 Part-Time Jobs Guide
Country-by-country guide to working while studying — legal hours, average wages, popular job types for international students.

### 🔬 Low CGPA / Research-First Strategy
Dedicated section for students with CGPA below 3.0 — how to use research publications, supervisor emails, and portfolio to overcome GPA gaps.

### 🛂 Visa Interview Guide
Embassy do's and don'ts specifically for Bangladeshi students — common rejection reasons and how to avoid them.

### ✍️ AI-Powered SOP Reviewer
Built-in Statement of Purpose reviewer powered by Claude AI — paste your SOP and get structured feedback.

### 📧 Cold Email Generator
AI-powered professor cold email generator — fill in your details and get a personalized, research-specific email draft.

### 🏆 Alumni Success Stories
Real BD student success stories from various universities with GPA, country, and scholarship details.

### 🪟 Immersive Plane Window Hero
- Animated airplane window frame with turbulence physics
- Real sky video playing through the oval porthole
- Mouse parallax — the view shifts as you move your cursor
- Stat pills floating around the window

### 🌐 Interactive Globe
Full 3D spinning globe with university dots, country labels, and click-to-info interaction.

---

## 🗂️ Project Structure

```
pilot/
├── index.html        ← Entire application (HTML + CSS + JS, ~7,800 lines)
├── window_sky.mp4    ← Sky video for the plane window hero
└── README.md         ← This file
```

> **Note:** `index.html` also exists as a **fully self-contained single-file version** (`vr_13_fixed.html`) where the video is Base64-embedded — no `window_sky.mp4` needed. Use that version for GitHub Pages or Vercel single-file deploys.

---

## ⚡ Quick Start

### Option 1 — Open Locally
```bash
# Just double-click index.html
# OR serve with any local server:
npx serve .
# Then open http://localhost:3000
```

### Option 2 — GitHub Pages
1. Fork or upload this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your site is live at `https://your-username.github.io/pilot`

### Option 3 — Vercel (30 seconds)
```bash
npm install -g vercel
cd pilot
vercel
```
Or drag the folder to [vercel.com/new](https://vercel.com/new).

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Structure | Semantic HTML5 |
| Styling | Pure CSS3 with CSS Variables, Grid, Flexbox |
| Animation | CSS keyframes + Web Animations API |
| Globe | Custom Canvas 2D (no Three.js, no libraries) |
| AI Features | Anthropic Claude API (claude-sonnet-4-5) |
| Fonts | Google Fonts (Space Grotesk, Bebas Neue, DM Mono, Syne, Orbitron) |
| Icons | Emoji-native (no icon library needed) |
| Dependencies | **Zero** — no npm, no bundler, no framework |

---

## 🎨 Design System

```css
--bg:        #0d0d0f   /* Deep black background */
--surface:   #1a1a1f   /* Card surfaces */
--primary:   #a6c8ff   /* Sky blue accent */
--saffron:   #F5A623   /* Gold highlight */
--emerald:   #4ade80   /* Success green */
--on:        #e5e2e1   /* Primary text */
```

Fonts: `Bebas Neue` (display) · `Space Grotesk` (body) · `DM Mono` (data/labels) · `Syne` (editorial) · `Barlow Condensed` (condensed headers)

---

## 📱 Browser Support

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile Chrome | ✅ Full |
| Mobile Safari | ✅ Full |

---

## 🔧 Customisation

The entire app is in one file. Key areas to edit:

- **University data** → Search for `<!-- USA -->`, `<!-- CANADA -->` etc. Each `uni-card` div contains all data
- **Globe dots** → Search for `var unis = [` in the globe engine script
- **Colour tokens** → `:root { }` at the top of the `<style>` block
- **AI prompts** → Search for `fetch("https://api.anthropic.com`
- **Window video** → Replace `window_sky.mp4` with any MP4

---

## 📄 License

MIT — free to use, modify, and distribute.

---

## 🙏 Built With

- Designed and developed with [Claude](https://claude.ai) by Anthropic
- Typography by [Google Fonts](https://fonts.google.com)
- AI features powered by [Anthropic Claude API](https://anthropic.com)

---

<p align="center">Made with ❤️ for every Bangladeshi student with a dream to study abroad</p>
