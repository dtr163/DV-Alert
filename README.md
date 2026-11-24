# DV Alert — Android app source

This repository builds a debug APK automatically in GitHub Actions.

## Build it from a tablet (no PC required)

1. Create a GitHub repository named `DV-Alert`.
2. Upload the **contents** of this ZIP to the repository root (not the ZIP file itself).
3. Commit the files to the `main` branch.
4. Open the repository → **Actions**.
5. If GitHub asks to enable workflows, choose **I understand my workflows, go ahead and enable them**.
6. Open the workflow **Build DV Alert APK** and wait until the run finishes with a green check.
7. Open the completed run, scroll to **Artifacts**, and download `DV-Alert-debug-APK`.
8. Extract the downloaded artifact ZIP and tap `app-debug.apk` to install it.
9. If Android blocks installation, allow Chrome or Files to **Install unknown apps** for this installation.

## App behavior

- WorkManager checks the official U.S. Department of State Diversity Visa page about every 12 hours when internet is available.
- It looks for a DV-2028 mention together with registration-related wording and sends a local notification once a matching notice is detected.
- The app has a manual check button and a shortcut to the official entry portal.

## Important limitations

- Periodic background work is approximate; Android may delay it because of battery optimization, Doze, or network availability.
- The page wording or structure can change. This keyword monitor may miss an announcement or generate a false alert. Always verify dates and instructions on official government pages.
- This is not an official U.S. government app and does not submit an entry.
- No personal information is collected or transmitted by the app.
- Registration portal: https://dvprogram.state.gov/
- Official program page: https://travel.state.gov/content/travel/en/US-visas/immigrate/diversity-visa-program-entry.html
