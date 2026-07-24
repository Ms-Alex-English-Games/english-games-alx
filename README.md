# Ms Alex's English Games

A single-page website showcasing English & CLIL Wordwall games for primary students (Years 1–6), organized into categories: Book Literature Club, Vocabulary & Topics, Grammar, Reading & Comprehension, Speaking & Exam Prep, CLIL Science & Nature, Greek Culture & History, Seasonal & Holidays, and Character & Community.

**Live site:** _add your GitHub Pages link here once it's live, e.g. `https://yourusername.github.io/repository-name/`_

## What's inside

- `index.html` — the entire site (HTML, CSS, and JavaScript all in one file, no build tools needed)

Each game links out to its original page on [Wordwall](https://wordwall.net), opening in a new tab so students stay on the site afterward.

## How it works

- **Search bar** filters games live by title, year group, or game type.
- **Category chips** jump down to each section.
- **Click tracking**: every "Play" button click sends an event to Google Analytics (game title, category, and year group), so you can see which games are actually being used.

## Updating the games list

All game data lives near the bottom of `index.html`, inside a JavaScript list called `GAMES`. Each game is one line, shaped like this:

{t:"Game Title", u:"https://wordwall.net/...", c:"category-id", k:"Game type", y:"Y5"},

- `t` — the title shown on the card
- `u` — the Wordwall link
- `c` — which category it belongs to (must match one of the ids in the `CATEGORIES` list just above it: `bookclub`, `vocab`, `grammar`, `reading`, `speaking`, `science`, `greek`, `seasonal`, `character`)
- `k` — the Wordwall game type (e.g. "Quiz", "Matching pairs") — shown as a small label on the card
- `y` — year group, if relevant (e.g. `"Y5"`, `"B1"`, or `""` if not specified)

To add a new game, copy an existing line, edit the details, and paste it into the list. To remove a game, delete its line. No other changes are needed — the page builds itself from this list automatically.

## Google Analytics

The site is connected to Google Analytics (Measurement ID G-JZ3R1Q6DKT). To view stats:

1. Go to analytics.google.com
2. Check Reports → Realtime to confirm clicks are being recorded
3. Check Reports → Engagement → Events, look for the play_game event, for a breakdown of which games are played and how often (data can take 24–48 hours to appear in standard reports)

## Hosting

This site is hosted for free with GitHub Pages. To update the live site after editing index.html:

1. Open index.html in this repository on GitHub
2. Click the pencil icon (Edit this file)
3. Paste in your updated content
4. Commit the changes
5. Wait a minute or two for GitHub Pages to redeploy, then refresh the live link
