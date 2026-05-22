# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Erik Nguita's personal CV site, served at https://erik7z.github.io via GitHub Pages from the `master` branch of `erik7z/erik7z.github.io`. Single static page — no build system, no JS, no tests, no package manager.

## Files that matter

- `/Users/erik7z/www/e7z/_github/_other/erik7z.github.io/index.html` — the entire page (intro + contact table).
- `/Users/erik7z/www/e7z/_github/_other/erik7z.github.io/style.css` — all styling, including the `@media (max-width: 360px)` mobile rules.
- `/Users/erik7z/www/e7z/_github/_other/erik7z.github.io/eriknguita.jpg` — profile photo referenced by `index.html`.
- `/Users/erik7z/www/e7z/_github/_other/erik7z.github.io/docs/nguita_erik_backend_developer.pdf` — the downloadable CV linked from the page via a raw `github.com/.../raw/master/docs/...` URL. When replacing the PDF, keep the same filename so the link stays valid.

## Workflow

- Preview locally by opening `index.html` directly in a browser, or `python3 -m http.server` from the repo root.
- Deployment is implicit: a push to `master` is the deploy. There is no CI.
- Per global rules (`/Users/erik7z/.claude/rules/git-and-commits.md`), never push directly to `master` — use `feature/*` or `fix/*` → PR → `master`.

## Things to know before editing

- The favicon link points to `akartynnik.png`, which does not exist in the repo (leftover from a template). Don't treat the resulting 404 as a regression introduced by your change.
- `index.html` uses an inline `<table>` for the contact block — that's intentional layout, not legacy markup to refactor.
