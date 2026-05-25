# animii

> **// find your crew. watch together.**

Animii is a Tinder-style social app built exclusively for the anime community. Swipe to find friends or romance, match based on watch history, and kick off watch parties — all wrapped in a slick dark broadcast aesthetic.

---

## What Was Built

This project went from zero to a fully interactive prototype in a single session. Here's everything that was designed and built:

### Concept & Branding
- Brainstormed the core product direction: a social/dating app specifically for anime fans
- Landed on a dual-purpose goal — both friendship and romance, with watch parties as the killer differentiator
- Named the app **Animii** — original, ownable, and not already in the App Store
- Chose the **Neo Broadcast** visual identity: dark backgrounds, cyan + orange accents, monospace typography, broadcast signal aesthetic
- Tagline: `// find your crew. watch together.`

### App Screens

**Onboarding Splash**
- Animated logo with floating particle effects
- "Start Your Arc" CTA framing the experience as a personal anime journey

**Swipe / Discovery Screen**
- Tinder-style profile card stack with drag-to-swipe (mouse + touch)
- Three-action row: **Pass**, **Like**, and **Watch Together** — the center button signals this app is about more than just matching
- Mode switcher at the top: **Friends / Romance / Watch Party**
- LIVE badge for users actively watching right now
- Episode-labeled cards (EP.01, EP.04, etc.) framing every interaction as part of your arc
- Swipe hint overlays (NOPE / LIKE / WATCH?) appear as you drag

**Matches Inbox**
- Matched profiles populate with preview messages
- Unread indicators and timestamps
- LIVE border highlight for online matches

**Profile Screen**
- Personal stats: shows watched, matches, watch parties
- Genre tags, currently watching list, and a **Hot Take** section as a built-in icebreaker
- Edit Avatar button opening the full character creator

### Avatar Creator
A full in-app anime character builder with live preview:

| Category | Options |
|---|---|
| Skin Tone | 9 tones — Porcelain to Deep |
| Hair Style | 16 styles — Spiky, Long Straight, Wavy, Afro, Bob, Pixie, Ponytail, Twin Tails, Side Swept, Mohawk, Undercut, Curly, Braids, Bun, Buzz, Middle Part |
| Hair Color | 18 colors — Black, Auburn, Red, Blonde, Platinum, Pink, Blue, Purple, Cyan, and more |
| Eye Shape | 5 styles — Standard, Sharp, Soft (Ghibli), Narrow, Half-Lidded |
| Eye Color | 16 colors — Brown, Blue, Cyan, Green, Purple, Red, Amber, Gold, Pink, and more |
| Accessories | 9 options — None, Round Glasses, Square Glasses, Visor, Eyepatch, Scar, Headband, Cat Ears, Demon Horns |

All built with custom SVG — no external avatar libraries. Each selection instantly updates the live preview. Saving the avatar replaces the profile hero.

### Spotify Anthem Feature
- Each user profile has an **Anime Anthem** — a song they choose via Spotify
- When a match happens, the anthem plays automatically on the match modal (the user just tapped, satisfying browser autoplay requirements)
- 10-second preview with animated equalizer bars, song title + artist, countdown timer, and a smooth progress bar
- Music fades out gracefully at the end or on modal close
- Architecture is ready for real Spotify API integration — just swap in the `preview_url` from the Web API

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript (single file) |
| Fonts | JetBrains Mono, Inter (Google Fonts) |
| Avatars | Custom SVG — hand-authored paths, radial gradients |
| Music | HTML5 Audio API, Spotify preview URL architecture |
| Hosting | Static — open `index.html` directly in any browser |

No frameworks. No build tools. No dependencies. Pure web platform.

---

## Running the App

```bash
git clone https://github.com/jbflores95/animii.git
cd animii
open index.html   # Mac
start index.html  # Windows
```

Or just double-click `index.html`. It runs entirely in the browser.

---

## Roadmap

Features identified during this session for future development:

- [ ] Real Spotify / Apple Music API integration for anthem playback
- [ ] AniList / MyAnimeList watchlist sync for compatibility matching
- [ ] Con meetup planner — find attendees at upcoming anime conventions
- [ ] Debate Arena — hot takes wall where matches argue about anime
- [ ] Watch Party lobby — sync video playback with matched users
- [ ] React Native mobile app (iOS + Android)
- [ ] Supabase backend — user accounts, matching algorithm, real-time chat
- [ ] Push notifications for new matches and watch party invites

---

## Design System

**Colors**
```
Background   #08090f
Surface      #10121c
Card         #14172a
Border       #1e2340
Cyan         #00d4ff   — connection, live, primary actions
Orange       #ff6b35   — energy, hot takes, debate
Pink         #ff4fa3   — likes, hearts
```

**Typography**
- Display / UI labels: `JetBrains Mono`
- Body / descriptions: `Inter`

**Voice**
All UI copy uses broadcast and code syntax — `// comments`, `EP.01` episode labels, `▶` play indicators. Every interaction is framed as part of the user's personal anime arc.

---

## License

MIT — build on it, fork it, make it yours.

---

*Built in one session. Powered by caffeine and too much anime.*
