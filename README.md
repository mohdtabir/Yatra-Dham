# Yatra Dham — Sacred Journeys Across India

A premium, static prototype of a Hindu pilgrimage & spiritual tourism platform, built with plain HTML, CSS and JavaScript (no build step required).

## How to run
Just open `index.html` in any modern browser — or serve the folder with any static server, e.g.:
```
npx serve .
```
The site needs an internet connection at runtime (for Google Fonts and Unsplash images used as placeholders).

## What's included
- **Homepage** — cinematic hero with search, featured categories, popular temples, AI planner teaser, festivals countdown, knowledge hub, state explorer, featured yatras, testimonials.
- **Temple pages** — full directory (`temples.html`) plus dedicated Jyotirlingas, Shakti Peethas and Char Dham pages, and a rich temple detail template (`temple-detail.html`) with history, timings, darshan info, map embed, gallery, FAQs and related temples.
- **Festivals** — live countdown calendar.
- **Knowledge Hub** — Aarti, Chalisa and Mantra libraries, plus a Blogs section with detail pages.
- **AI Yatra Planner** — generates a day-by-day itinerary from budget, days, starting city and preferred circuit.
- **Admin Panel** (`admin.html`) — full **Add / Edit / Delete** for Temples, Festivals, Aarti, Chalisa, Mantras and Blogs. Changes save to the browser's `localStorage` and instantly reflect across every page.

## Content included out of the box
12 Jyotirlingas, 3 sample Shakti Peethas, 3 Char Dham sites, 5 other famous temples, 8 festivals, 6 aartis, 4 chalisas, 5 mantras, and 5 blog posts — all fully editable and extendable from the Admin Panel.

## Important scope notes (read before presenting this as final)
The original brief asked for a much larger, backend-powered platform (500+ temples, 5,000+ blog articles, Firebase auth, cloud storage, a Next.js/TypeScript codebase, multi-language support, PWA, role-based admin, AI chat assistant, etc.). Building all of that is a multi-week engineering project, not something any single response can fully deliver. This build focuses on:
- The **full visual design system and page structure** requested (every page type from the brief exists and is wired up).
- **Real, working Add/Edit/Delete** functionality across every content type, backed by `localStorage` (see `js/store.js`).
- A **curated, realistic dataset** in each category instead of literal 500+/5,000+ placeholder entries, so you can see (and immediately extend) real, polished content rather than filler text.

### Not included (would require a backend/server)
- Firebase Authentication, user accounts, saved favorites/yatras, reviews & ratings persistence across devices.
- A true CMS/SEO manager, sitemap generator, or role management (these require a server + database).
- Multi-language (Hindi/English) toggle and PWA installability.
- The AI Yatra Planner and AI Chat Assistant here use simple client-side logic rather than a live LLM API — wiring in a real AI backend is straightforward to add if you want to go further.

If you'd like, I can help migrate this into a real Next.js + Firebase project, or extend the temple/blog datasets — just let me know which direction to take next.

## File structure
```
yatra-dham/
├── index.html              Homepage
├── temples.html            All-temples directory (search + filters)
├── jyotirlingas.html       Jyotirlinga circuit
├── shakti-peethas.html     Shakti Peetha circuit
├── char-dham.html          Char Dham circuit
├── temple-detail.html      Dynamic temple detail (?id=...)
├── festivals.html          Festival calendar with countdown
├── aarti.html / chalisa.html / mantras.html   Knowledge libraries
├── blogs.html / blog-detail.html              Blog section
├── yatra-planner.html      AI-style itinerary generator
├── about.html / contact.html
├── admin.html              Add / Edit / Delete panel
├── css/style.css           Full design system
└── js/
    ├── data.js             Seed content
    ├── store.js            localStorage-backed CRUD data layer
    ├── components.js       Shared header/footer + card renderers
    └── admin.js            Admin panel logic
```
