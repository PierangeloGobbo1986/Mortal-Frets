# ☠ MORTAL FRETS — The Fretboard Slayer

Retro arcade-style guitar fretboard trainer inspired by Mortal Kombat. 12 game modes across Identification, Construction and Ear Training. Global leaderboard powered by Firebase. Installable as a home screen app on iPhone via Safari.

🎮 **[Play Now](https://PierangeloGobbo1986.github.io/Mortal-Frets/)**

---

## Game Modes

All modes: 10 questions per round · Score = errors (fewer = better) · Tiebreaker: time

### Identification — see the question on the fretboard, press the correct button

| Mode | What you see | Feedback |
|---|---|---|
| **Note ID** | Dot on fretboard (frets 0–12, all strings) | Wrong button plays that note |
| **Interval ID** | R (root, red) + interval dot within ±3 frets / ±2 strings | Wrong button plays that interval |
| **Chord ID** | Real voicing — triads / Drop 2 / Drop 3 / Drop 2+4 · fretboard darkened outside box | Wrong button plays root-position arpeggio · Correct: chord name + inversion shown 2s |
| **Scale ID** | Full scale in 5-fret box, R = Root · fretboard darkened outside box | Wrong button plays nothing · Correct: scale plays, root + name shown 2s |

### Construction — target illuminated, build it on the fretboard, press SUBMIT

| Mode | Pre-placed | What you do |
|---|---|---|
| **Note Construction** | — | Place ALL occurrences (frets 0–12, all strings) |
| **Interval Construction** | R (red) | Click interval note — auto-checks immediately |
| **Chord Construction** | One chord tone (amber, role R/3/5/7) · box stays dark throughout | Place remaining notes, one per string |
| **Scale Construction** | R in box | Fill all scale positions |

### Ear Training — fretboard hidden, 🔊 speaker button

| Mode | What you hear | Notes |
|---|---|---|
| **Ear Note** | Single note, always C4–B4 | Identify the note |
| **Ear Interval** | Root → interval (melodic) | Identify the interval |
| **Ear Chord** | Drop 2/3/2+4 voicing, central position | Identify the chord |
| **Ear Scale** | Scale ascending root→octave | Identify the scale |

In all ear modes: tap 🔊 to replay · wrong button plays the sound of what you pressed.

---

## Rules

- **Variety:** same type appears at most twice per round; exact same question never repeats
- **Mercy ☠:** activates after 2 wrong answers — hold to reveal full solution on fretboard; correct answer button lights gold. Release to retry.
- **Box selection:** Chord and Scale modes — fixed 5-fret box or 💀 KHAOS (random each question). Fretboard outside box is always darkened.
- **Active Chords / Scales:** deselect types in lobby to skip them; show ✕ in-game
- **Leaderboard:** ALL or SAME CONFIG (your active chord/scale selection only)
- **Notation:** toggle A-B-C / Do-Re-Mi at any time

---

## Scoring

| Errors | Result |
|---|---|
| 0 | ⚡ FLAWLESS VICTORY |
| 1–2 | EXCELLENT FIGHTER |
| 3–5 | SKILLED WARRIOR |
| 6–10 | FIGHT HARDER |
| 11–19 | FINISH HIM |
| 20+ | FATALITY |

---

## Music Theory Coverage

**Notes:** all 12 chromatic, frets 0–12, all 6 strings (standard tuning E A D G B e)

**Intervals:** m2 · M2 · m3 · M3 · P4 · TT · P5 · m6 · M6 · m7 · M7 · P8

**Chords:** Maj · min · Aug · Dim · Maj7 · Dom7 · min7 · ø7 · °7

**Scales:** Major · Natural Minor · Harmonic Minor · Melodic Minor · Whole-Half Dim · Half-Whole Dim

**Voicings:** triads on all 4 adjacent 3-string groups · Drop 2, Drop 3, Drop 2+4 on all adjacent 4-string groups · all inversions

---

## Install as iPhone App

1. Open Safari and go to `https://PierangeloGobbo1986.github.io/Mortal-Frets/`
2. Tap the **Share** button (rectangle with arrow)
3. Tap **"Add to Home Screen"**
4. Name appears as **"Mortal Frets"** — tap **Add**

The app opens full-screen with no browser chrome.

---

## Deploy on GitHub Pages

1. Upload `index.html` (the game file)
2. Upload `icon.png` (the app icon) to the same root folder
3. GitHub Settings → Pages → branch main → / (root)

---

## Firebase Setup

Uses Firebase Realtime Database REST API — no SDK.

1. [console.firebase.google.com](https://console.firebase.google.com) → new project → Realtime Database
2. Replace `FB_CONFIG` near the top of `<script>` with your project values
3. Set rules:

```json
{
  "rules": {
    "leaderboards": {
      "$mode": { ".read": true, ".write": true }
    }
  }
}
```

---

## Tech

Pure HTML/CSS/JS · Web Audio API · SVG fretboard · Firebase REST API · Press Start 2P + Rajdhani · CRT scanlines · iOS silent switch bypass via MediaStream API · PWA-ready (Apple Touch Icon)

---

## License

Copyright © 2026 Pierangelo Gobbo. All rights reserved.
Unauthorized copying, modification or distribution is strictly prohibited.
