# Closed-Loop — 30-Day Habit Tracker

A single-page, self-contained habit tracker for six daily targets: Exercise, Language learning, Repository & CV work, Sleep, Diet, and Water.

Ticks are saved automatically to your browser's local storage, with a live streak counter per habit and an overall progress bar. Optional cloud sync via a private GitHub Gist keeps it in sync across browsers/devices.

## Preview
[![Watch the demo](./preview.png)]([./preview.mp4](https://github.com/Mir-robotics/closed-loop-tracker-with-git/blob/main/preview.MP4))

## Usage

Just open `index.html` in a browser — no build step, no dependencies to install. **Don't just double-click the file** (some browsers block local storage for `file://` pages) — either use GitHub Pages (below) or run a quick local server:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Cloud sync across devices (optional)

By default, ticks only save to the one browser you're using (`localStorage`). To make them follow you across devices:

1. Go to **[github.com/settings/tokens](https://github.com/settings/tokens)** → *Generate new token (classic)*.
2. Give it the **`gist`** scope only (nothing else needed) and generate it.
3. Copy the token, open the tracker, paste it into the **☁ Cloud sync** box at the top, and click **Connect**.
4. The app creates a private Gist to hold your data and will read/write it automatically from then on — on any device where you connect the same way.

⚠️ The token is stored in that browser's `localStorage` and sent only to `api.github.com`. Use a token scoped to `gist` only, and revoke it anytime from the same GitHub settings page if needed.

## Enabling GitHub Pages

1. Push this repo to GitHub (steps below).
2. On GitHub, go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save — your tracker will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Project structure

```
.
├── index.html   # the tracker itself
└── README.md
```

