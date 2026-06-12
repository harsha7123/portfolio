# HarshaOS — Portfolio

A macOS-desktop themed portfolio for Sri Harsha Chedalla. Single self-contained `index.html` (real project screenshots are embedded, so it works offline and on any host).

## Deploy to Vercel

**Option A — drag & drop**
1. Go to vercel.com → Add New → Project
2. Drag this whole folder in, or upload `index.html` + `vercel.json`
3. Deploy. Done.

**Option B — CLI**
```bash
npm i -g vercel
vercel        # preview
vercel --prod # production
```

**Option C — GitHub**
Push this folder to a repo, then Import it in Vercel.

## Before you ship — 2 things

1. **Resume** — drop your real `resume.pdf` next to `index.html` (the Resume.pdf icon and Contact download both point to `/resume.pdf`).
2. **Contact form (optional)** — to capture messages in a Google Sheet instead of opening the visitor's mail app:
   - Create a Sheet → Extensions → Apps Script
   - Add a `doPost(e)` that appends `e.parameter.name / email / type / message`
   - Deploy → Web app → access "Anyone"
   - Paste the web-app URL into `GOOGLE_SCRIPT_URL` near the top of the `<script>` in `index.html`
   - Until you do, the form gracefully falls back to opening the visitor's email app.

## Update a project screenshot later
Screenshots are embedded as base64 in the `IMG` object inside `index.html`. Replace a value with a new `data:image/jpeg;base64,...` string (keep them ~600px wide, quality ~72 to stay small).
