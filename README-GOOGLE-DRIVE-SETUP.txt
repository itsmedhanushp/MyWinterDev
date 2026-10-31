WINTER ARC 2026 — FOUR APPS + GOOGLE DRIVE SYNC

UPLOAD THESE FILES TO THE ROOT OF YOUR GITHUB REPOSITORY:
- index.html                  Home page / launcher
- diet-tracker.html           App 1: Diet Tracker
- winter-arc-tracker.html     App 2: Daily Workout & Winter Arc Progress
- developer-edition.html      App 3: C#/.NET + DSA Developer Edition
- bible-journey.html          App 4: Bible Journey
- README-GOOGLE-DRIVE-SETUP.txt

GOOGLE CLOUD SETUP — ONE WEB OAUTH CLIENT ID FOR ALL FOUR APPS
1. Open https://console.cloud.google.com/ and create/select a project.
2. Enable Google Drive API.
3. Configure Google Auth Platform / OAuth consent screen.
4. Create OAuth Client ID -> Web application.
5. Under Authorized JavaScript origins, add your GitHub Pages origin, e.g.
   https://YOUR-GITHUB-USERNAME.github.io
   Add your custom domain origin too if you use one.
6. Copy the Web Client ID (ends in .apps.googleusercontent.com).
7. Open each published app using its HTTPS GitHub Pages URL, paste the same
   Client ID and click Connect Google Drive. Sign in with the same Google account.
8. Repeat on each device/browser. Each app keeps its own JSON backup in Drive.

IMPORTANT
- Local browser storage is used first. Connect each app to Drive on every device.
- After connection, changes auto-upload while the page remains open and the
  Google access token is valid. Use Sync now after reconnecting.
- Google access tokens are held in memory and expire; reconnect when asked.
- Sync uses timestamps (newest copy wins). Avoid simultaneous edits on two devices.
  Sync device A before switching to device B.
- Export JSON backups occasionally as an extra safety copy.
- Clearing browser site data can erase the local copy; use Restore from Drive
  to recover a previously uploaded backup.
- Bible chapter text is fetched online from bible-api.com in the public-domain
  King James Version (KJV). Internet is required to load chapter text.
- Bible reading target is approximately 2,200 words/day; the app adjusts the
  chapter count based on actual fetched chapter length. The 60-minute timer is
  a reading/reflection timer and is not a background alarm.
- Do not put a Google Client Secret or password in these HTML files. Only the
  public OAuth Client ID is entered in the apps.

TEST
1. On device A, connect all four apps and make a small test entry.
2. Wait for the Drive status to confirm the upload.
3. On device B, open each app, enter the same Client ID and connect.
4. Confirm the test data appears. Repeat for all four apps.
