# SolveX – Ask. Learn. Solve.

A bilingual (Khmer / English) learning site. No build step, no account, no paid AI. Everything is plain HTML, CSS and JavaScript.

## Easiest: put it online in 2 minutes (Netlify Drop)
1. Unzip this folder.
2. Open https://app.netlify.com/drop and drag the **whole folder** onto the page.
3. Open the link it gives you. On a phone, use the browser menu → **Add to Home screen**.

Voice, camera and offline mode need **https**, which Netlify provides.

## Other free hosts
- **GitHub Pages:** create a repo, upload all files, then Settings → Pages → deploy from the main branch.
- **Cloudflare Pages / Vercel:** import the repo; build command empty, output directory `/`.

## Test on your computer
Run `python3 -m http.server 8000` in this folder, then open http://localhost:8000 (localhost counts as secure, so camera, voice and offline work).

## Files
- `index.html` – page shell · `style.css` – design · `app.js` – all features
- `sw.js` – offline cache (change `solvex-v2` to `solvex-v3` after you edit files) · `manifest.webmanifest` – install info · `icon*` – app icons

## Notes
- Data (notes, history, settings) stays in the browser’s local storage. Clearing browser data erases it.
- **Photo reading (Khmer + English):** the “Read text from photo” button uses the free Tesseract.js engine. It downloads the engine and Khmer language data from a CDN the first time (internet needed once, a few MB), then works offline. It reads printed text best. Handwriting and math symbols can be misread, so always check and edit the text before tapping Solve. It only reads text; it does not understand pictures or diagrams.
- Voice input depends on the browser (Chrome on Android works best); Khmer recognition may not be available everywhere.
- Created by KONG ICHHUNPHEARITH
