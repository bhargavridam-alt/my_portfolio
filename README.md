# Ridam Bhargav — Personal Portfolio

A polished, high-contrast black-and-white editorial personal portfolio website engineered exclusively with semantic **HTML5** and **CSS3**.

Zero JavaScript, zero external libraries, zero frameworks, and zero build steps. Fast, accessible, responsive, and ready for instant deployment to GitHub Pages.

---

## ✦ Table of Contents
1. [Overview & Design Identity](#-overview--design-identity)
2. [Project Structure](#-project-structure)
3. [Previewing Locally](#-previewing-locally)
4. [Customizing Content & Placeholders](#-customizing-content--placeholders)
5. [Publishing to GitHub Pages](#-publishing-to-github-pages)
6. [Accessibility & Best Practices](#-accessibility--best-practices)

---

## ✦ Overview & Design Identity

- **Visual Direction**: Editorial monochrome with high-contrast typography, hairline borders, and generous whitespace.
- **Typography**: Paired editorial serif (*Playfair Display*) for commanding headings, modern geometric sans-serif (*Plus Jakarta Sans*) for body, and *JetBrains Mono* for technical metadata.
- **Micro-Interactions**: Subtle, restrained CSS-only hover transitions, card elevations, and grayscale-to-contrast image effects.
- **Accessibility**: Full WCAG AAA/AA color contrast compliance, dedicated keyboard skip link (`.skip-link`), visible `:focus-visible` outlines, descriptive image `alt` tags, and `@media (prefers-reduced-motion: reduce)` support.

---

## ✦ Project Structure

```text
portfolio/
├── index.html                  # Semantic HTML5 layout & portfolio structure
├── styles.css                  # Pure vanilla CSS design system & responsive styling
├── README.md                   # Setup, customization & deployment instructions
└── assets/
    └── images/
        ├── favicon.svg         # Monogram SVG favicon (RB)
        ├── portrait-hero.jpg   # Featured hero photo (Clock Tower)
        ├── achievement-bits.jpg# Achievements highlight photo (BITS Pilani)
        ├── highlight-campus.jpg# Campus promenade highlight photo
        ├── project-preview-1.svg # High-contrast Systems Architecture preview
        ├── project-preview-2.svg # Telemetry & Real-Time Analytics preview
        ├── project-preview-3.svg # Terminal & CLI workflow preview
        └── project-preview-4.svg # Campus community platform preview
```

---

## ✦ Previewing Locally

Because this site uses pure HTML and CSS with standard relative paths, you do not need any build tool (e.g., Vite, Webpack) or package manager (`npm`/`yarn`).

### Option 1: Direct Browser Launch
Double click `index.html` in your file manager or run:
```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

### Option 2: Local HTTP Server (Recommended)
Using Python's built-in HTTP server:
```bash
python3 -m http.server 8000
```
Then visit `http://localhost:8000` in your web browser.

---

## ✦ Customizing Content & Placeholders

All customizable areas in `index.html` are clearly marked with HTML comments (`<!-- PLACEHOLDER: ... -->`):

1. **Personal Information & Bio**:
   - In `index.html`, search for `Ridam Bhargav` or `Newton School of Technology` to update your introduction, degree specialization, or biography.
2. **Projects (`#projects`)**:
   - Update titles, descriptions, role badges (`Lead Developer`, etc.), and tags in each `<article class="project-card">`.
   - Update GitHub links and live demo links (`href="https://github.com/..."`).
   - Drop your own screenshot images into `assets/images/` and update the `src` attribute.
3. **Achievements & Milestones (`#achievements`)**:
   - Adjust dates, event names, and descriptions in `<article class="milestone-item">`.
4. **Skills Matrix (`#skills`)**:
   - Add, edit, or remove skills inside each `<li class="skill-item">` according to your strengths.
5. **Contact Links & Socials (`#contact`)**:
   - Update your direct email address (`mailto:your_email@example.com`).
   - Replace social links (`GitHub`, `LinkedIn`, `Twitter / X`, `LeetCode`) with your exact profile URLs.
6. **Resume / CV**:
   - Place your resume PDF in `assets/resume.pdf` and link it in the hero button (`href="assets/resume.pdf"`).

---

## ✦ Publishing to GitHub Pages

1. Initialize git and commit your files:
   ```bash
   git init
   git add .
   git commit -m "feat: initial commit of portfolio website"
   ```
2. Create a repository on GitHub (e.g., `portfolio` or `<your-username>.github.io`).
3. Connect your remote repository and push:
   ```bash
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
4. Enable GitHub Pages:
   - On GitHub, navigate to **Settings** &rarr; **Pages**.
   - Under **Build and deployment**, select **Source: Deploy from a branch**.
   - Set the branch to `main` and folder to `/(root)`.
   - Click **Save**. Your site will be live at `https://<your-username>.github.io/<repo-name>/` in ~1 minute!

---

## ✦ Accessibility & Verification Checklist

- [x] **Zero JavaScript**: Runs flawlessly in any browser with JS disabled.
- [x] **Pure Semantic HTML5**: Uses `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<aside>`, `<time>`, `<footer>`.
- [x] **Responsive Layouts**: Flexbox and CSS Grid adapt smoothly across Mobile (<580px), Tablet (581px–1024px), and Desktop (>1024px).
- [x] **Accessible Navigation**: Keyboard skip-to-content link, clear focus outlines, and pure CSS mobile drawer.
- [x] **Reduced Motion**: Disables all animations and transforms when `prefers-reduced-motion: reduce` is enabled in user settings.
- [x] **WCAG Contrast**: Strong contrast ratio with ivory white `#f5f5f7` on deep obsidian black `#0a0a0a`.
