[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/c6mnxczqw8-beep/makefun-sitegen-20261124/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/c6mnxczqw8-beep/makefun-sitegen-20261124/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
A fast, dependency-free drop-in replacement for makefun-site 1.0.0.

`solve.js` exports `run(input)`, returning the exact output tree (every page,
index/tag page, `build-report.txt` and static file, byte for byte) that
makefun-site's `build` returns for the same site. `main.ts` is the harness
driver: it reads `/input/cases.json`, answers each case with `run`, and writes
`/output/answers.json`.

Speed comes from a single-pass front-matter scanner, hand-rolled Markdown
block/inline scanning with bulk plain-text runs, a per-case slug cache,
cached per-page cards, and an array-based template renderer — with no
regular expressions or object churn in the hot loops.
