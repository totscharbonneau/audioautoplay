# Setting up GitHub Pages for this project

This folder contains a simple webpage (`index.html`) that plays `audio.mp3`
(converted from the original `AUD-20260630-WA0009.opus`) when opened. The goal
is to host it on GitHub Pages so a printed QR code can link straight to it.

## Steps

1. Create a new repository on GitHub (e.g. `audioplay`).
   - Must be **public** for GitHub Pages to work on a free account.
2. From this folder, initialize git and push:
   ```bash
   git init
   git add index.html audio.mp3
   git commit -m "Add audio player page"
   git branch -M main
   git remote add origin https://github.com/<your-username>/audioplay.git
   git push -u origin main
   ```
3. On GitHub, go to the repo's **Settings → Pages**.
   - Under "Source", select the `main` branch and `/ (root)` folder.
   - Save.
4. Wait 1-2 minutes. Your site will be live at:
   ```
   https://<your-username>.github.io/audioplay/
   ```
5. Open that URL on your phone to confirm the play button / autoplay works.
6. Generate a QR code pointing to that URL (e.g. via a QR code generator) and
   print it.

## Notes

- Any future push to `main` updates the live site automatically within about
  a minute.
- Mobile browsers (iOS Safari, Chrome) block autoplay-with-sound on a fresh
  page load with no prior user interaction — that's why the page shows a
  "Tap to play" button as a fallback if autoplay is blocked.
