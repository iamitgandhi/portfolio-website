# Personal Portfolio Website

A modern, high-performance portfolio website built with **Astro**, **Tailwind CSS**, and **Three.js WebGL**, deployed globally on **Cloudflare Pages**.

[![Live Preview](https://img.shields.io/badge/Live_Website-www.amitkumargandhi.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://www.amitkumargandhi.com/)
[![Astro](https://img.shields.io/badge/Astro_v7-BC52EE?style=for-the-badge&logo=astro&logoColor=white)](https://astro.build)
[![Cloudflare Pages](https://img.shields.io/badge/Deployed_on-Cloudflare_Pages-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)](https://pages.cloudflare.com/)

---

## 🌐 Website Preview

[![Portfolio Website Preview](./public/preview.png)](https://www.amitkumargandhi.com/)

👉 **Live URL:** [https://www.amitkumargandhi.com/](https://www.amitkumargandhi.com/)

---

## ⚡ Technical Features & Architecture

* **Astro Static Site Generation (SSG):** Built with Astro 7 for ultra-fast, zero-JS-by-default static HTML rendering with zero runtime server overhead.
* **Global Edge CDN Delivery:** Distributed worldwide across Cloudflare's edge network with custom cache and security headers via `public/_headers`.
* **Interactive 3D WebGL Shader:** Custom Three.js fragment shader with real-time cursor-following chromatic aberration and RGB displacement effects. Features screen-width viewport detection to dynamically load 3D libraries only on desktop devices (≥ 1024px) for peak mobile PageSpeed scores.
* **Reflow-Free Background Grid:** High-performance canvas grid background using document-relative scroll offset range caching instead of layout-thrashing DOM queries, maintaining `~0ms` Total Blocking Time (TBT).
* **Preloaded LCP Assets:** Optimized WebP hero image with `fetchpriority="high"` and `<link rel="preload">` in `<head>` for near-instant Largest Contentful Paint.
* **Analytics & Privacy:** Integrated Google Analytics (`gtag.js`) and asynchronous SecurePrivacy cookie consent manager.
* **Domain Email Infrastructure:** Native Cloudflare Email Routing for inbound mail with Brevo SMTP relay for authenticated outbound sending.

---

## 🛠️ Technology Stack & Badges

### Core Frameworks & Languages
![Astro](https://img.shields.io/badge/Astro_v7-BC52EE?style=for-the-badge&logo=astro&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_v3-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript_ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

### 3D Visuals & Animation
![Three.js](https://img.shields.io/badge/Three.js_WebGL-000000?style=for-the-badge&logo=three.js&logoColor=white)
![GSAP](https://img.shields.io/badge/GSAP_Animations-88CE02?style=for-the-badge&logo=greensock&logoColor=white)

### Cloud & Infrastructure
![Cloudflare Pages](https://img.shields.io/badge/Cloudflare_Pages-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Cloudflare DNS](https://img.shields.io/badge/Cloudflare_DNS-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Brevo](https://img.shields.io/badge/Brevo_SMTP-0B996F?style=for-the-badge&logo=brevo&logoColor=white)

---

## 📁 Repository Structure

```
├── public/                     # Static assets (images, favicon, resume PDF, headers)
│   ├── _headers                # Cloudflare Pages HTTP security & cache headers
│   ├── AmitG.webp              # Compressed, optimized profile WebP
│   ├── Amit Kumar Gandhi - Resume.pdf # Portfolio resume file
│   └── preview.png             # Website preview screenshot
├── src/
│   ├── components/             # UI and section components
│   │   ├── layout/             # Navbar and SiteFooter
│   │   ├── sections/           # Hero, About, Projects, Experience, Skills, Contact, etc.
│   │   └── ui/                 # Container, Section, SkillBadge, ResumeButton
│   ├── data/                   # Centralized site content definitions
│   │   ├── site.ts             # Primary configuration data object
│   │   └── types.ts            # TypeScript interfaces
│   ├── layouts/                # BaseLayout document wrapper & analytics head tags
│   ├── pages/                  # Page entry points (index.astro, 404.astro, robots.txt.ts)
│   └── styles/                 # Global CSS styles & Tailwind directives
├── astro.config.mjs            # Astro configuration
├── .npmrc                      # CI package management configuration
└── package.json                # Dependencies and build scripts
```

---

## 💻 Local Development Setup

### Prerequisites
* **Node.js:** `>= 20.0.0`
* **Package Manager:** `npm`

### Commands

```bash
# 1. Clone the repository
git clone https://github.com/iamitgandhi/portfolio-website.git
cd portfolio-website

# 2. Install dependencies
npm install

# 3. Start local development server
npm run dev

# 4. Check TypeScript & Astro diagnostics
npm run check

# 5. Build for production
npm run build

# 6. Preview production build locally
npm start
```

Local dev server runs on `http://localhost:4321`.

---

## ☁️ Cloudflare Pages Deployment

This website is automatically built and deployed via **Cloudflare Pages** connected to this repository:

1. **Framework Preset:** `Astro`
2. **Build Command:** `npm run build`
3. **Build Output Directory:** `dist`
4. **Environment Variables:**
   * `NODE_VERSION=22`
   * `SITE_URL=https://www.amitkumargandhi.com`

Continuous deployment triggers automatically on every push to the `main` branch.

---

## 📝 License

This project is open-source under the [MIT License](LICENSE).
