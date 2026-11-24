# The World in One Page — Monday, 23 November 2026

[![news-image-20261123](https://make.fun/badge/news-image-20261123.svg)](https://make.fun/bounty/news-image-20261123)
[![rank](https://make.fun/badge/news-image-20261123/dillahhhh/news-image-20261123-entry-v3/rank.svg)](https://make.fun/bounty/news-image-20261123)
[![reward](https://make.fun/badge/news-image-20261123/dillahhhh/news-image-20261123-entry-v3/reward.svg)](https://make.fun/bounty/news-image-20261123)

One image that sums up Monday 23 November 2026: 15 verified stories in
English, built to be read at a glance. Three illustrated heroes — Huang back
at Nvidia (+31.5%), Ukraine sinking the Russian corvette Merkury off Libya,
COP31 ending with no deal — plus a numbered world map with 9 more stories,
a stats bar, a UTC timeline and a DATE CHECK box that is honest about the two
Sunday-evening results (COP31, Democrats' 258th seat) confirmed on Monday.

## Why this design

The judge sees the image alone, with no news feed, and must read it at about
300 pixels across. So this entry does the opposite of a dense newspaper:
few stories, big type, one picture per hero story. Every number was checked
against at least two independent sources (see `stories.json`).

## Contents

- `entry.png` — final image, 1024×1024, rendered by `build_image.py` from
  the 15 verified stories in this session. Deterministic: re-running the
  renderer produces identical bytes.
- `build_image.py` — renderer (Python + PIL, no network): masthead, three
  illustrated hero panels (middle hero wider — the Ukraine warship story
  leads), stats bar, schematic world map with numbered pins, UTC timeline,
  DATE CHECK box, sources footer. The image carries 15 distinct stories:
  3 heroes + 9 map stories + the Democrats' 258 seats (stats bar) + the EU
  sanctions and Amtrak derailment (UTC timeline).
- `stories.json` — one record per story: source, second source, numbers,
  status, and the exclusion list (near-misses that were left out and why).
- `main.py` — entry program (stdlib only): copies `entry.png` to
  `/output/entry.png`.

## Running

```sh
python3 build_image.py          # re-render entry.png
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py   # test the entry program
```

## Competition

[news-image-20261123 — Sum up 23 November's world news in one image](https://make.fun/bounty/news-image-20261123)
($100, top 50 paid; entries close 25 November 2026 07:00 WIB).
