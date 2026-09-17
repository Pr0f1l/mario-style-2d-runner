# 🍄 Pixel Dash — Endless Platformer

A tiny 2D platformer, built with plain HTML5 Canvas and JavaScript — no frameworks, no build step, no external assets. Every level is procedurally generated, and every sound effect plus the background music is synthesized live with the Web Audio API.

**[▶ Play it live](#)** — replace this link with your GitHub Pages URL once deployed (see below).

## Features

- **Single-jump platforming** — run and jump only, no double-jump or wall-jump, keeping the controls simple and classic.
- **Procedural random maps** — a seeded generator lays out platforms, gaps, floating ledges, enemies, and coins fresh every level, so no two playthroughs are the same.
- **Fully synthesized sound** — jump, coin, stomp, hurt, win, and background music are all generated in real time with the Web Audio API. No `.mp3`/`.wav` files to manage.
- **Stomp-to-kill enemies**, coin collecting, a lives/health system, and a score counter.
- **Mobile-friendly** — on-screen touch controls appear automatically on touch devices.
- Pause, mute, and a "next random map" flow on level complete.

## Controls

| Action | Keys |
|---|---|
| Move | `←` `→` or `A` `D` |
| Jump (single jump only) | `Space` or `↑` or `W` |
| Pause | `P` |

## Project structure

```
.
├── index.html   # page structure + game logic (JavaScript)
├── style.css    # all visual styling
└── index.md     # this file
```

## Running it locally

Just open `index.html` in any modern browser — no server or build step required.

## Deploying to GitHub Pages

1. Push `index.html` and `style.css` to the root of your GitHub repository (this `index.md` is optional — keep it as your repo's documentation, or rename it to `README.md`).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and the `/ (root)` folder, then **Save**.
5. Your game will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

> **Note:** GitHub Pages will always serve `index.html` as the homepage even if `index.md` is also present, so there's no conflict between the two files.

## How the map generation works

Each level uses a seeded pseudo-random number generator (`mulberry32`). The generator walks forward through the level placing ground segments, occasional gaps, floating platforms, enemies, and coin arcs — with gap widths and platform heights capped to stay within the player's jump distance, so every generated map is always completable.

## License

Feel free to fork, modify, and use this project however you like.
