# Ben's Album — World Cup 2026 Sticker Tracker

A fun, mobile-first single-page web app for tracking a World Cup 2026 sticker
collection. Built as a single `index.html` file with no build step.

## Features

- **Collect view** — hero progress ring, live stats, and a "Continue" shortcut to your next unfinished section.
- **Teams view** — searchable, filterable grid of all 48 national teams (flags + per-team progress).
- **Detail view** — drill into any team or special section to tap stickers as collected.
- **Stats view** — completion %, teams/sections done, and milestone tracking.
- **Confetti & toasts** when you complete a section or hit a milestone.
- **Cross-device sync** via Supabase, with automatic local-storage fallback.
- Optimized for both mobile (bottom tab bar, safe-area aware) and desktop (full-width top nav).

## Setup

Open `index.html` in any browser — it runs as-is.

To enable cross-device sync, set your Supabase values near the top of the
`<script>` block in `index.html`:

```js
const SUPABASE_URL = 'https://YOUR-PROJECT.supabase.co';
const SUPABASE_ANON_KEY = 'your-anon-key';
const TABLE = 'owned_stickers';
```

The table needs a single text `id` column (primary key). Without these values,
the app saves your collection locally on the device.
