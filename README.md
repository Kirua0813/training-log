# Training Log

A private, single-file web app to track daily training, nutrition, body weight and sleep. It runs entirely in your browser, installs on an iPhone home screen like a native app, and has five dark red-and-black visual styles.

**Live app:** `https://YOUR-USERNAME.github.io/training-log/`

## Features

- **Daily entry:** trained (yes/no), date, calories, creatine, protein, fat, carbs, weight after workout and sleep.
- **Smart defaults:** the date moves to the next day automatically, and an empty weight repeats the previous day's weight. Duplicate dates are blocked.
- **Summary and per-metric tabs:** week, month, year or all-time statistics with charts for weight, calories, creatine, protein, fat, carbs, training days and sleep.
- **Daily goals:** set targets for calories, macros, creatine, sleep, weight and workouts per week. The app shows days on goal and draws a dashed goal line on charts.
- **Data tab:** full history with delete, plus copy and import backup (tab, semicolon or comma separated).
- **5 styles:** Berserk, Neon, Glitch, Terminal and Blackout, plus a custom background image with a darkness slider.

## Install on iPhone

1. Open the live app link in **Safari**.
2. Tap **Share**, then **Add to Home Screen**, then **Add**.
3. Open the app from the new icon.

## Your data and privacy

- All entries, goals and settings are stored in your browser's local storage on **your device only**. Nothing is sent to a server and there is no account.
- Data is separate per browser and per address (Safari and the Home Screen app do not share it). Use **Data → COPY DATA** now and then to keep a backup, and **IMPORT** to restore it.
- Goals and settings are not part of the copied backup.
- Clearing website data in your browser deletes your entries.

## Importing from a spreadsheet

Paste rows into **Data → IMPORT** in this column order:

`Date, Trained?, Calories, Creatine, Weight, Sleep, Protein, Fat, Carbs`

Dates can be `YYYY-MM-DD`, `DD/MM/YYYY` or spreadsheet serial numbers. "Yes", "Sim" and "No", "Não" are accepted.

## Goal rules

Calories, macros and creatine count as met within 10% of the goal. Sleep counts when at or above the goal. Weight counts within 0.5 kg of the target.

## Project structure

| File | Purpose |
| --- | --- |
| `index.html` | The whole app (HTML, CSS and JavaScript in one file) |
| `manifest.webmanifest` | Home screen app metadata |
| `sw.js` | Service worker (network first, offline fallback) |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | App icons |
| `LICENSE` | MIT license for the code |

## Deploy your own copy

1. Fork or create a public repository and add these files to the `main` branch.
2. Open **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
3. Your app is published at `https://YOUR-USERNAME.github.io/REPO-NAME/`.

## Tech notes

No build step and no dependencies. Fonts (Cinzel, IM Fell English, Orbitron, Rajdhani, Share Tech Mono) load from Google Fonts on first use, with system fallbacks.

## License and credits

The source code is released under the [MIT License](LICENSE).

The default background wallpaper embedded in `index.html` is third-party artwork. It is **not** covered by the MIT license and remains the property of its owner. If you reuse or redistribute this project, replace it with an image you have the rights to use. You can pick your own image in the app under the settings button.
