# 🛰️ shreeharia.github.io — Mission Control

Personal portfolio of **Shreehari Anbazhagan** — Data & Cloud Engineer, Backend Developer, Applied-AI builder.

**Live at:** https://shreeharia.github.io

A space sci-fi "mission control" interface with a game layer on top: visitors earn XP, unlock 12 achievements, rank up from **Cadet** to **Fleet Admiral**, and can discover hidden easter eggs. Built with zero frameworks and zero build tools — pure HTML, CSS and vanilla JavaScript in a single file.

## Features

- **Boot sequence** — a terminal-style OS boot on first visit (skippable, auto-skipped on repeat visits and for reduced-motion users)
- **Animated starfield** — canvas-based with parallax on mouse move, twinkling stars and occasional shooting stars
- **Mission HUD** — persistent XP bar, visitor rank, and an achievements log (progress saved in the browser)
- **12 achievements** — earned by exploring sections, opening project source code, making contact, and finding secrets
- **Easter eggs** — a satellite that occasionally drifts across the screen (catch it!), and a warp drive triggered by the Konami code `↑ ↑ ↓ ↓ ← → ← → B A` or by tapping the ◈ logo seven times
- **Telemetry counters** — animated career stats
- **Sci-fi 404 page** — served automatically by GitHub Pages for broken links
- Fully responsive, keyboard-accessible, `prefers-reduced-motion` respected, print-friendly

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire site — content, styles and scripts |
| `404.html` | "Lost in space" page for unknown URLs |
| `resume.pdf` | Downloadable CV — linked from the hero and Contact buttons |
| `og-image.png` | Social preview card (LinkedIn / WhatsApp / X link previews) |
| `README.md` | This file |

## Deploying to GitHub Pages

1. Create a **public** repository named exactly `ShreehariA.github.io` (your username + `.github.io`).
2. Upload `index.html`, `404.html`, `resume.pdf`, `og-image.png` and `README.md` to the repository root.
3. That's it — GitHub Pages activates automatically for repos with this name. The site goes live at **https://shreeharia.github.io** within a couple of minutes. (You can confirm under **Settings → Pages**, where "Deploy from a branch / main / root" should be selected.)

### Via the command line instead

```bash
git init
git add .
git commit -m "Launch mission control 🚀"
git branch -M main
git remote add origin https://github.com/ShreehariA/ShreehariA.github.io.git
git push -u origin main
```

### Updating the site

Edit `index.html`, commit and push (or re-upload through the GitHub web UI). Changes appear on the live site within a minute or two.

## Customizing

Everything lives in `index.html`:

- **Content** — each section is clearly marked with `<!-- ===== SECTION ===== -->` comments. Edit text directly; project cards and timeline entries are self-contained blocks you can copy-paste to add more.
- **Colors** — all theme colors are CSS variables in the `:root` block at the top (`--ion` is the cyan accent, `--amber` the highlight color).
- **Achievements & XP** — the `ACH` array in the script defines every achievement (icon, name, description, XP). `RANKS` defines the rank thresholds.
- **Boot lines** — the `LINES` array in the script.
- **Stats** — the telemetry numbers are `data-target` attributes in the hero section.

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Opening `index.html` directly in a browser also works.

## Optional next steps

- **Updating your CV** — overwrite `resume.pdf` with a newer version any time; the site's buttons keep working, no HTML change needed.
- **Custom domain** — add a `CNAME` file containing your domain and configure DNS (Settings → Pages → Custom domain).
- **Analytics** — add a privacy-friendly tracker such as GoatCounter or Plausible with one script tag.
