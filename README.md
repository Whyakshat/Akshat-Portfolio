# Hey, I'm Akshat! 👋

Welcome to the repository of my personal portfolio website. I built this space to reflect who I am as a developer: someone who values clean code, robust backend engineering, and immersive, high-fidelity user experiences. 

I'm currently a third-year BCA (Full Stack Development) student at Bennett University, and this portfolio serves as a showcase of the production-grade full-stack applications I independently design, build, and deploy.

---

## 🎨 Design Philosophy & UX Highlights

I wanted to move away from generic, template-like portfolio designs. The aesthetic here is sleek, dark, and minimalist, but brought to life with dynamic micro-interactions and canvas-based animations that react to the user.

- **Ink-Drop Cursor Trail**: Instead of a basic cursor, I hand-coded a fixed-canvas trail. Moving the mouse spawns ink drops with random gravity, drift, and easing offsets that gracefully dissolve.
- **Scroll-Synchronized Video Backdrop**: In the hero section, the video playback position is bound directly to the viewport scroll. As you scroll down, the background vinyl rotates and transforms smoothly in real time.
- **Magnetic Navigation**: The navigation title uses a magnetic pull effect. When your cursor gets close, it smoothly shifts toward it.
- **Quantum Wave Contact Panel**: The contact form features a custom HTML5 canvas background rendering multiple sine waves with varying frequencies and amplitudes. Hovering near the waves creates a magnetic wave distortion.
- **Anti-DevTools & Scraping Guard**: Built-in safeguards (like F12/Right-Click interceptors, console debugger loops, and viewport dimension tracking) protect the source content and images from basic scraping.

---

## 🚀 Performance Optimization: 98% Size Reduction

Originally, the HTML file contained heavy base64-encoded inline images, making the page size over **4.05 MB**—resulting in slower initial page loads and poor SEO scores.

I optimized this by:
1. Extracting all base64-encoded strings, decoding them, and organizing them as compressed assets inside the [images/](images) directory.
2. Moving the background mp4 video into the [images/](images) directory.
3. Updating the markup to use relative pathing.
4. Cleaning up redundant and unused CSS styles from the stylesheet.

**The Result:** The main HTML payload was reduced to a mere **54 KB** (a **98.6% reduction**), allowing the website to load instantly even on slower mobile networks.

---

## 📂 File Structure

Here's how the optimized project workspace is structured:

```text
AKSHAT'S PORTFOLIO/
├── images/
│   ├── about-card.png           # Profile/Intro card graphic
│   ├── experience-bg.jpg        # Background for experience section
│   ├── fresh-plate-mockup.jpg   # Mockup image for Project 2
│   ├── hero-motion.mp4          # Scroll-synced hero video loop
│   ├── heyo-mockup.png          # Mockup image for Project 1
│   ├── projects-bg.jpg          # Background for projects section
│   └── skills-bg.jpg            # Background for skills section
├── index.html                   # Main entry point (highly optimized structure)
└── README.md                    # You are here!
```

---

## 🛠️ Tech Stack & Integrations

- **Frontend**: Semantic HTML5, Vanilla CSS3 (Custom Variables, Flexbox/Grid layouts), Vanilla ES6 JavaScript (Intersection Observer API, Canvas API).
- **Integrations**: Web3Forms REST API for secure, backend-free contact form submissions.
- **Fonts**: Inter (for clean body text), Bebas Neue (for bold headlines), Playfair Display (for elegant italic accents) via Google Fonts.

---

## 💻 Featured Projects Showcased

### 1. Heyo — Location-Based Social Networking PWA
*A real-time Progressive Web App connecting users semantically based on proximity.*
- **Backend & Database**: Node.js/Express, Prisma ORM with SQLite (PostgreSQL-ready).
- **Core Features**: OpenAI semantic discovery, split-polling real-time chat (saving 60% bandwidth), Leaflet.js map integration with location expiry.
- **Security**: JWT authentication, email verification via OTP, rate-limiting on authentication routes.

### 2. Fresh Plate & Co. — Meal Ordering Platform
*A full-stack meal-ordering web application featuring zero external UI frameworks.*
- **Backend & Database**: Node.js/Express with MongoDB/Mongoose.
- **Core Features**: Access levels (Admin/Customer), real-time order dashboard, resilient in-memory database fallback to handle DB outages, express-rate-limit protection.

---

## ⚙️ Getting Started

### Running Locally

Since the portfolio runs entirely on static files, you don't need complex build steps.

1. **Option A (Double Click)**:
   Simply open `index.html` in your favorite web browser.

2. **Option B (Recommended - Local Server)**:
   For the best video scroll sync performance, run a local development server.
   
   If you have Python installed:
   ```bash
   python3 -m http.server 8000
   ```
   If you use Node.js and have `npx` available:
   ```bash
   npx serve .
   ```
   Now, open `http://localhost:8000` (or `http://localhost:3000` for serve) in your browser.

---

## 🌐 Deployment Guide

### GitHub Pages (Simplest)
1. Push this folder to a new GitHub repository.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, select the `main` or `master` branch as the source and click **Save**.
4. Your site will be live at `https://<username>.github.io/<repo-name>/`.

### Netlify / Vercel
1. Create a Netlify or Vercel account and link your GitHub.
2. Select the repository containing this folder.
3. Keep the **Build Command** empty and set the **Publish Directory** to `.` (current directory).
4. Click **Deploy**.
