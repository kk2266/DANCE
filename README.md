# Pixelated Tie-Dye Spiral Music Player

A self-contained HTML5 music visualizer and player with animated spiral backgrounds, a dancing GIF, and a full-featured track browser.

## Features

### Music Player
- Play/pause, next/previous track, and shuffle controls
- Seek bar and volume slider with mute toggle
- Auto-advances to the next track when a song ends
- Previous button restarts the current track if more than 3 seconds in, otherwise goes back

### Track Sidebar
- Slide-out sidebar (hamburger menu, top-left) to browse all tracks
- **Singles** listed at the top level
- **Albums** displayed as navigable folders — click an album to see its tracks, click "Back" to return
- Currently playing track is highlighted with a purple accent

### Visual Effects
- Full-screen pixelated canvas animation with multiple modes:
  - **Spiral** — single-arm logarithmic spiral
  - **Rings** — concentric circles with angular variation
  - **Vortex** — three-armed spiral with combined effects
  - **Random** — smooth crossfade cycling through all modes
- Floating music notes while audio is playing
- Diamond sparkle effects across the screen
- Animated dancing GIF synchronized to the visualization

### Customizable Controls (bottom-right)
- **Pixel Size** — 4px, 8px, 12px, 16px
- **Speed** — Slow, Normal, Fast
- **Mode** — Spiral, Rings, Vortex, Random
- **Dance Intensity** — Chill, Groove, Hyped, Chaos

## Project Structure

```
web_music/
├── combine_sp.html          # Main player (HTML + CSS + JS, single file)
├── spiral.html              # Standalone spiral visualization (no player)
├── deal-with-it-trailblazer.gif  # Dancing GIF
├── tracks/                  # Audio files
│   ├── *.mp3                # Singles (loose tracks)
│   └── graduation/          # Album folder
│       └── *.mp3            # Album tracks
└── README.md
```

## Usage

Open `combine_sp.html` in any modern browser. No build step, no dependencies, no server required — just double-click the file.

## Adding Music

### Adding singles
1. Drop `.mp3` files into the `tracks/` folder
2. Add an entry to the `library.singles` array in `combine_sp.html`

### Adding albums
1. Create a subfolder inside `tracks/` (e.g. `tracks/my-album/`)
2. Drop `.mp3` files into it
3. Add an entry to the `library.albums` array in `combine_sp.html` with the album name and track list

## Fonts

Uses [Rampart One](https://fonts.google.com/specimen/Rampart+One) for headings and [Zen Dots](https://fonts.google.com/specimen/Zen+Dots) for UI elements (loaded from Google Fonts).

## Tech Stack

- Vanilla HTML, CSS, JavaScript — zero dependencies
- HTML5 Canvas for pixel-art visualization
- HTML5 Audio for music playback
- Google Fonts for anime-style typography
