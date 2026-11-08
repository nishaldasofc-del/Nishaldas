# Nishal Das Portfolio

A single-file, no-build static site (HTML, CSS, JS) with GSAP, ScrollTrigger and Lenis loaded from CDNs.
Deploy to Vercel or Netlify by uploading this folder as-is.

## Files
- index.html: the whole site (the portrait and two project screenshots are embedded as data URIs)
- og-image.png: social share image (1200x630)
- robots.txt, vercel.json: crawler rules, security headers and caching
- images/: the embedded images as separate files, for reference or to swap in

## Deploy (Vercel)
1. Push this folder to a GitHub repo, or run `npx vercel` inside it.
2. Framework preset: Other. No build command, no output directory.

## Before you go live
1. Replace `https://your-domain.com` in the <head> (canonical, og:url, og:image, twitter:image) with your real domain.
2. Contact form: set `formEndpoint` in the CONTACT CONFIG block near the bottom of index.html (for example a Formspree URL).
   Without it the form opens the visitor's email app, using your email in the same block.
3. Add a sitemap.xml once you know the domain.

## Where to edit things (all near the bottom of index.html)
- PROJECT CONFIG: project names, descriptions, status, live/GitHub/demo links, screenshots (image key).
- TEMPLATES CONFIG: the 10 template cards. Sites are built from template-{n}-ngai.netlify.app. Override with url:.
- CONTACT CONFIG: email and social links. Empty values are hidden.
- project-images: screenshots as data URIs. To use files instead, set the img src to images/yourfile.webp.

## Notes
- The theme (light/dark) is saved in localStorage. Dark mode turns the portrait black and white; hover or touch to reveal colour.
- Press Ctrl/Cmd+K for the command menu.
- Respects prefers-reduced-motion: intro loader, scroll animations and 3D motion are turned off.
- Template previews load in an iframe. If a template site blocks framing, visitors can still use "Open site".
