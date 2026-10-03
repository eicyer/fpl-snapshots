# fpl-snapshots

Raw Snapshots of the public [Fantasy Premier League](https://fantasy.premierleague.com) API, taken at least once a day from the 2026/27 season onwards.

The API only ever shows the current state, so prices, ownership, injury news and chance-of-playing flags are lost unless someone records them. This repo keeps them.

## Layout

```text
raw/<UTC timestamp>/
  bootstrap-static.json.gz   players, teams, Gameweeks, chips, game settings
  fixtures.json.gz           every fixture with difficulty and results
  event-status.json.gz       whether the current Gameweek's points are final
  set-piece-notes.json.gz    penalty and free-kick takers
  event-<gw>-live.json.gz    live points for the current Gameweek
```

Each file is the API response exactly as served, gzipped. Snapshots are never edited after they are committed.

## Source

Taken automatically by [soccer-agent](https://github.com/eicyer/soccer-agent). The data belongs to the Premier League; this repo is an unofficial archive and is not affiliated with or endorsed by the Premier League or Fantasy Premier League.
