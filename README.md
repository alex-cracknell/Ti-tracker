# Titration Tracker

A small phone app for tracking blood pressure, pulse, weight and (optionally) symptoms, side effects, sleep and stress while starting ADHD medication.

- **All data stays on the device.** It's stored in the phone's browser storage (IndexedDB). Nothing is sent to any server.
- **Optional backup.** "Back up now" opens the phone's share sheet, so the backup file can go straight to Google Drive, Dropbox, OneDrive, iCloud/Files or email. "Restore from backup" loads it back, on the same or a new phone.
- **Works offline** once installed to the home screen.
- **Free to host.** It's just static files, so anyone can use the same link and each person's data stays on their own phone.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Lets phones install it to the home screen |
| `sw.js` | Makes it work offline |
| `icon-*.png`, `apple-touch-icon.png` | Home-screen icons |

## Install on a phone
- **iPhone (Safari):** open the link, tap **Share → Add to Home Screen**.
- **Android (Chrome):** open the link, tap **⋮ → Install app** (or Add to Home screen).

## Updating the app
Edit `index.html`, then in `sw.js` change `VERSION = "tt-v1"` to `"tt-v2"` (and so on) and re-upload. Phones pick up the new version the next time the app is opened with a connection. Users' data is not affected.

## Things to know
- **Back up regularly.** Clearing browser data, uninstalling the browser, or losing the phone deletes the records. The app reminds you every 14 days.
- iPhones can clear website storage for sites that aren't used for several weeks. Installing to the home screen avoids this, and the app also asks the browser for persistent storage.
- Each browser has its own copy: data in Safari isn't visible in Chrome on the same phone. Use backup/restore to move it.
- The app doesn't send reminder notifications (that would need a server). It shows what's due each time you open it.

## Medical note
This is a personal record, not medical advice. Alert levels default to the NICE home blood pressure threshold of 135/85 and a resting pulse of 100; change them in Settings to whatever your prescriber specifies. ASRS v1.1 questions are © World Health Organization; weekly use is a tracking adaptation of the screener (which originally asks about the past 6 months).

If you share this publicly, add your own note that it's not a medical device and that users should follow their prescriber's guidance.
