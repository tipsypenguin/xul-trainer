# Xul Dungeon Trainer

A single-file HTML/Canvas tank practice tool for the **Xul** dungeon in *Fellowship*.

Top-down view. No install, no dependencies — open `index.html` in a browser.

## What is implemented

This trainer focuses on the hardest tank-facing parts of the fight:

- **True Sight** — click corner altars, 20s duration, cannot refresh while active
- **Tired Eyes** — stacks every 2s while True Sight is up; residual after it falls
- **Statue waves** — safe lanes, patterns, visibility tied to True Sight
- **Blood orbs** — spawn from last altar used, move toward the boss, heal on contact
- **Eradication** — telegraph beams that track targets, then instant resolve
- **Tormented Visions** — boss cast that requires True Sight
- **Portal** — click to teleport (20s cooldown)

Movement, boss chase, speed sliders, and a basic HUD are included for practice flow.

## What is *not* implemented

Not a full dungeon sim. Many real-fight systems are missing or simplified on purpose.  
Only the True Sight / wave / orb skillset is built out in detail.

## Controls

| Input | Action |
|--------|--------|
| WASD / Arrow keys | Move |
| Click altar | True Sight |
| Click portal | Teleport |
| Start / Restart | Begin or reset the fight |

## Character icons (optional)

Place these PNGs next to `xul_dungeon.html` (same folder works on GitHub Pages):

| File | Role |
|------|------|
| `tank.webp` | Player |
| `boss.webp` | Boss |
| `ally1.webp` / `ally2.webp` / `ally3.webp` | Party members |

If a file is missing, a colored circle is used instead.

## Tech notes

- One HTML file, Canvas + `requestAnimationFrame`
- Game-speed multiplier scales fight timers together
- **Most of this codebase was generated with AI** and then adjusted by hand

## License

Use and modify freely for personal practice.
