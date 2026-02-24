# DraftKings Parlays — Continuity

## Status as of 2026-02-24

**What this project is:** AI-researched parlay picks for DraftKings. Friend provides a screenshot of the games he wants to parlay on. Claude does deep research (odds, standings, injuries, H2H, back-to-backs) and outputs three tiers of parlays: safe, medium value, high payout.

**First session completed:**
- Built Feb 26, 2026 NHL parlay picks (12 games on the slate)
- Created `index.html` — styled dark-theme page with all three parlays, injury alerts, and avoid list
- Created `Feb26_NHL_Parlays.md` — full research document with game-by-game breakdowns
- Moved screenshot to `nhl-feb26-games.png`
- Deployed to GitHub Pages: **https://benjaminmwaldo.github.io/draftkings-parlays/**
- GitHub repo: https://github.com/benjaminmwaldo/draftkings-parlays

## The Three Parlay Tiers (pattern to follow each session)

| Tier | Goal | ~Legs | Notes |
|------|------|-------|-------|
| 1 — Safe | Likely to hit | 3 | Clean favorites, no injury wildcards, rest advantage |
| 2 — Medium | Higher return, still likely | 4 | Add 1-2 value picks on top of the safe core |
| 3 — High Payout | Informed long shot | 3 | Specific situational edges, not random fliers |

## Workflow for Future Sessions

1. User provides screenshot of available games
2. Run deep research: current odds (OddsShark, Polymarket), standings (hockey-reference.com), injuries (DailyFaceoff, covers.com), back-to-back schedules (ESPN scoreboard for previous day), H2H records
3. Flag game-day injury checks prominently (line-moving news like McDavid, Crosby)
4. Build three parlays per the tier pattern above
5. Update `index.html` with new picks (or create a new dated HTML file)
6. Commit and push: `git add . && git commit -m "Add [date] parlay picks" && git push`
7. Share: **https://benjaminmwaldo.github.io/draftkings-parlays/**

## Key Research Sources (bookmarked for next session)

- Odds: https://www.oddsshark.com/nhl/odds
- Standings: https://www.hockey-reference.com/leagues/NHL_2026_standings.html
- Injuries: https://www.dailyfaceoff.com/hockey-player-news/injuries/1
- Back-to-backs: https://www.espn.com/nhl/scoreboard (previous day)
- Recent form: https://www.statmuse.com/nhl

## Next Steps

- When user brings another slate: follow the workflow above
- Consider adding a "picks history" section to index.html showing past parlays and whether they hit
