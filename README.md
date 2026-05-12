# ⌨️ Spacebar Clicker

An addictive browser-based idle/incremental clicker game where you press the spacebar to earn points, hire quirky helpers, and build an unstoppable clicking empire.

<p align="center">
  <a href="https://spacebarclicker.win/" target="_blank"><img src="https://img.shields.io/badge/🎮_PLAY_NOW-spacebarclicker.win-483d21?style=for-the-badge&labelColor=f9fbb2" alt="Play Spacebar Clicker" /></a>
</p>

---

## 🎮 About The Game

**Spacebar Clicker** is a zero-dependency, single-page idle game that runs entirely in your browser. Originally created by [CrociDB](https://bruno.croci.me/), the game challenges you to press the spacebar (or tap on mobile) to earn points, then spend those points on increasingly powerful auto-clickers.

### Gameplay Loop

1. **Click** — Press the spacebar or tap the on-screen button to earn points
2. **Buy Upgrades** — Spend points on 10 tiers of auto-clickers, from Monkeys to Alien Tech Machines
3. **Scale Up** — Watch your points-per-second skyrocket as upgrades compound
4. **Enjoy the Rain** — As your empire grows, spacebar icons rain down the screen in an ever-intensifying visual reward

### Upgrade Tiers

| Tier | Helper | Base Rate |
|------|--------|-----------|
| 1 | 🐒 Monkey | 1 every 5 sec |
| 2 | 👩 Boomer Mom | 3/sec |
| 3 | 📱 Gen Z Kid | 20/sec |
| 4 | ⌨️ Keyboard Upgrade | 2× manual clicks |
| 5 | 😤 Angry Influencer | 150/sec |
| 6 | 🎮 MOBA Gamer | 600/sec |
| 7 | 🤖 Homemade Robot | 3,500/sec |
| 8 | 🔫 Laser Machine Gun | 25,000/sec |
| 9 | ☢️ Nuclear Blast Gun | 100,000/sec |
| 10 | 👽 Alien Tech Machine | 1,000,000/sec |

### Tech Stack

- **HTML5** — Single-file architecture, no build tools required
- **Vanilla CSS** — Inline styles with CSS custom properties
- **Vanilla JavaScript** — Game engine with particle system, procedural audio via `jsfxr`, and localStorage persistence
- **Zero Dependencies** — No frameworks, no CDNs for core functionality

---

## 🛠️ Fixes & Improvements

This fork includes a comprehensive code and SEO audit with **20+ fixes** applied without breaking any game functionality or visual design.

### 🔴 Critical Fixes

| Fix | What Changed | Why It Matters |
|-----|-------------|----------------|
| Added `<!DOCTYPE html>` | Was missing entirely | Browser was running in **Quirks Mode**, causing layout inconsistencies |
| Fixed `color: 483D21` → `color: #483d21` | Missing `#` prefix on hex color | Score popup particles were **invisible** — now properly styled |
| Initialized `this.canclick = true` | Property was never set in `init()` | **First spacebar press was silently ignored** — now works immediately |
| Removed fake `aggregateRating` | Had hardcoded 4.8★ / 1,250 reviews | Google can **penalize unverifiable structured data** |
| Fixed `javascript:` href | Changed to `onclick` handler | Deprecated pattern; game object wasn't globally accessible anyway |

### 🟠 Major Fixes

| Fix | What Changed |
|-----|-------------|
| Removed `console.dir()` from production | Debug logging in `loadGame()` was dumping save data to console on every visit |
| Game object now globally accessible | Changed anonymous class instantiation to `var game = new class{...}` so reset link works |
| Added Open Graph meta tags | Social shares on Discord, Twitter, WhatsApp now show rich previews instead of blank cards |
| Added Twitter Card meta tags | Proper `summary_large_image` card with title, description, and image |
| Expanded thin content sections | How to Play, Upgrades, and FAQ sections went from ~50 words to ~400 words of useful content |
| Fixed semantic HTML | Changed `<article>` wrapper to `<div>` — content sections aren't re-shareable articles |

### 🟡 Minor Fixes

| Fix | What Changed |
|-----|-------------|
| Fixed viewport meta | Removed `user-scalable=no` → users can now pinch-to-zoom (WCAG 1.4.4 compliance) |
| Fixed heading hierarchy | Item template changed from `<h2>` to `<h3>` — proper document outline |
| Added `rel="noopener noreferrer"` | All external `target="_blank"` links now secure against tab-napping |
| Improved footer alt text | Generic "Spacebar Clicker" alt text → descriptive platform names (GitHub, YouTube, etc.) |
| Added `<noscript>` fallback | Users with JS disabled now see a helpful message instead of a blank page |
| Removed deprecated `keywords` meta | Google has ignored this since 2009 |

### 📁 New Files Created

| File | Purpose |
|------|---------|
| `robots.txt` | Crawl directives + sitemap reference for search engines |
| `README.md` | This file — project documentation |

### 📁 Files Updated

| File | Changes |
|------|---------|
| `site.webmanifest` | Fixed empty `name`/`short_name` fields, updated theme colors to match site palette, added `start_url` and `description` |
| `sitemap.xml` | Updated `lastmod` to current date, changed `changefreq` from `daily` to `monthly` (accurate for a static page) |

---

## 📂 Project Structure

```
spacebarclicker/
├── index.html              # Complete game (HTML + CSS + JS in one file)
├── robots.txt              # Search engine crawl directives
├── sitemap.xml             # XML sitemap for SEO
├── site.webmanifest        # PWA manifest for "Add to Home Screen"
├── favicon.ico             # Browser tab icon
├── favicon-16x16.png       # Small favicon
├── favicon-32x32.png       # Standard favicon
├── apple-touch-icon.png    # iOS home screen icon
├── android-chrome-192x192.png  # Android icon (small)
├── android-chrome-512x512.png  # Android icon (large) + OG image
└── README.md               # This file
```

---

## 🚀 Running Locally

No build step needed. Just open the file:

```bash
# Option 1: Direct file open
open index.html

# Option 2: Simple HTTP server (recommended for full functionality)
npx serve .
```

---

## 📜 Credits

- **Original Game** by [CrociDB](https://bruno.croci.me/) — [GitHub Repo](https://github.com/lightend/spacebar-clicker)
- **Audio Engine** — [jsfxr](https://sfxr.me/) procedural sound synthesis
- **Code & SEO Audit** — Comprehensive fixes applied May 2026

---

<p align="center">
  <a href="https://spacebarclicker.win/" target="_blank"><strong>👉 Play Spacebar Clicker Now at spacebarclicker.win 👈</strong></a>
</p>
