CADENCE — ANDROID INSTALLABLE WEB APP

WHAT THIS PACKAGE DOES
This wraps your original Cadence HTML app as a Progressive Web App (PWA). It adds:
- an app name, icon and standalone display mode;
- a service worker that caches the app shell;
- caching of external scripts/fonts after they have loaded successfully online;
- an installable HTTPS web app that can be added to your Android home screen.

IMPORTANT
A PWA cannot be properly installed by opening index.html directly from Downloads. It must be served from HTTPS (or localhost). The app's existing task data is stored in browser local storage. Keep using the same installed app/browser profile to retain that data. Clearing Chrome site data can erase it.

EASIEST PUBLISHING ROUTE: GITHUB PAGES
1. On a computer, sign in to GitHub and create a new repository. You can call it cadence-app.
2. Upload all the CONTENTS of this folder (index.html, manifest.webmanifest, sw.js, icons folder). Do not upload only the ZIP.
3. In the repository, open Settings > Pages.
4. Under Build and deployment, choose Deploy from a branch; select the main branch and / (root), then Save.
5. Wait for GitHub Pages to publish. The address will look like https://YOUR-USERNAME.github.io/cadence-app/.
6. Open that HTTPS address on your Android phone in Chrome.
7. In Chrome, tap the three-dot menu and choose Install app (or Add to Home screen, depending on the Chrome version). Confirm.
8. Open Cadence from the new home-screen icon.

UPDATES
If you replace the app files later, increment CACHE_NAME in sw.js (for example cadence-pwa-v2) before uploading. This makes browsers fetch the new app shell.

OFFLINE BEHAVIOUR / LIMITATIONS
- The app shell is cached after the first successful online visit. Open the app once while online before relying on it offline.
- Tailwind, Lucide and Google Fonts are external resources. The service worker caches them when successfully fetched online; first-time offline use may therefore look less styled or have missing icons/fonts.
- The AI Magic Split code has no Gemini API key configured in the original file. Its built-in local fallback remains available; this package does not add a private API key.
- This is an installable web app, not a native APK.
