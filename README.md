# Pop Joy — landing page

Marketing site for **Pop Joy**, a block-popping match-3 mobile game.

A single self-contained `index.html` — no build step, no dependencies. Open it directly, or serve the folder:

```bash
python3 -m http.server 4174
```

## What's in it

- **Playable hero demo** — a real 6×6 match-3 board in the phone mock: flood-fill group detection, gravity, refill from the top.
- **Self-playing demo board** in *How to play*, which performs the mechanic on a loop (and pauses when scrolled off-screen).
- **Game-native scroll motion** — rows of block sprites drop and settle like a board refill; the mascot peeks from behind a section edge.

## Assets

`assets/sprites/` holds 14 transparent PNGs (mascot poses, wordmark, tiles, boosters) cut from the game's own asset sheet. `assets/screen-*.jpg` are real in-app screenshots.

The page degrades gracefully if screenshots are missing: each `<img>` removes itself on error, and the gallery hides entirely when empty.

## Notes

- `scoreFor()` in `index.html` is deliberately plain (linear + flat streak bonus) — the scoring curve is still to be designed.
- Store links in the download section are placeholders.
