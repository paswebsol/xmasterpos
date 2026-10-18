# Master POS — GitHub Pages deployment

This package prepares the existing Master POS client HTML for hosting as an installable Progressive Web App (PWA). The client interface and business logic are retained; PWA metadata, app icons, and an offline service worker have been added.

## Deploy on GitHub Pages
1. Sign in to GitHub and create a repository (for example `master-pos-client`).
2. Upload **all files and folders in this ZIP** to the repository root. `index.html` must be at the root.
3. Open **Settings → Pages**.
4. Under Build and deployment, select **Deploy from a branch**, choose `main` and `/(root)`, then Save.
5. Wait for GitHub Pages to publish the site. Open the published HTTPS address once while online.

## Install on devices
- **Android (Chrome):** open the published site, tap the browser menu, then **Install app** or **Add to Home screen**.
- **iPhone/iPad (Safari):** open the published site, tap **Share**, then **Add to Home Screen**.
- **Windows/macOS/Linux computers:** open the published site in a supported browser. Use the install icon in the address bar if offered, or the browser menu's **Install app** option.

## Offline and data notes
- After the first successful online visit, the service worker caches the app shell so it can reopen offline. A first visit requires internet.
- Sales, products and other records are stored according to the existing app's browser-storage implementation. They are not automatically synchronized across devices. Use the app's backup/export features and keep backups safely.
- Do not clear browser/site data unless records have been backed up.
- GitHub Pages serves a public website. Do not upload private customer records, secrets, issuer credentials, or the separate license-issuer tool to this public repository.
- iPhone installation and offline caching require the HTTPS hosted site; opening the HTML directly from a ZIP/file manager does not provide full PWA installation behavior.

## Important
This is a browser-installable PWA, not a signed native App Store / Google Play package. Publishing in the Apple App Store or Google Play requires additional packaging, developer accounts, and review. Test the deployed site and backup/restore flow before distributing it to paying clients.
