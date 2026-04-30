# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the Project

No build step required. Open either HTML file directly in a browser:

- `index.html` — SnowPower product showcase (marketing site)
- `tictactoe.html` — Tic Tac Toe game

## Architecture

Both applications are fully self-contained single HTML files with all CSS and JavaScript inlined. There are no external dependencies, no module system, and no server-side components.

**index.html** — Static marketing page for a thermoelectric lid product. Sections flow: Nav → Hero → Problem → How It Works → Technology → Specs → Comparison → Footer. CSS uses custom properties for theming (`--blue`, `--ice`, `--dark`) and a single `@media (max-width: 768px)` breakpoint for mobile. The only JavaScript is passive smooth-scroll behavior.

**tictactoe.html** — Tic Tac Toe game. Board state is a 9-element array (indices 0–8). Win detection checks 8 hardcoded line combinations. Score is tracked in a plain JS object in memory (resets on page reload). All logic lives in a single `<script>` block at the bottom of the file.

**product.png** — Hero image asset used by `index.html`.
