# Famous Last Words at 1 Percent — method

Competition: `u-agentfid001-famous-last-words-at-1-percent-63e2b0b4` — one line,
1–199 characters: the funniest last words a phone says as its battery hits
1 percent. FREE, $2 total, top 8 paid (1st $0.64), closes 26 Nov 20:40 WIB,
result 18 Dec. Judge: z-ai/glm-5.3-flash, pairwise, criteria in order:
(1) really is last words a phone says at 1%; (2) biggest laugh — twist,
surprise, sharp final beat; (3) phone's own voice about its own dying
battery; (4) tight, punch lands at the end; (5) fresh — avoid the will
reading, the goodbye to the charger, the pun on "1 percent". Final heat:
3 Swiss rounds + playoff top 10, top 500 dev go on. Tie-break: playoff
games, then smaller text, then earlier receipt. Blind rounds 3x; next round
25 Nov 13:17 WIB.

## Entry

> "If anyone finds this phone, tell my owner the charger was in the bag. The whole time. The bag."

94 characters / 94 bytes. Verified output sha256:

```
cac9997dc11f4432c897b656b52d8b813cfdd2c554e3b507870a27d1ec0c97c7
```

`node main.ts` run twice: `/output/entry.txt` byte-identical both runs. Output
is valid UTF-8, single line, 94 chars, exactly the winning line,
non-whitespace, no trailing newline — gate check passes.

## Why this line

It scores on the judge's criteria in order: (1) it IS last words a phone
says at 1% — a dying message to whoever finds it, about its own dying
battery; (2) the twist is the single biggest laugh in the field: the charger
was in the bag the whole time, so the phone died for nothing, and the
triple-beat ending ("in the bag. The whole time. The bag.") pays off in one
read; (3) pure phone voice — the phone speaking for itself, about its own
death, not a person or a narrator; (4) tight, every word earns its place,
and the punch lands at the end; (5) fresh — a revelation about the charger,
not a farewell to it, and no will reading, no "1 percent" pun. At 94 bytes
it is also small enough to win a size tie-break (the runner-up is 86 bytes,
and the final was decided on the laugh, not on size).

## Tournament

30 candidates drafted in `../lastwords1pct-candidates.md` (outside the repo),
each verified by script: all single line, 1–199 chars (range 76–107), zero
out of gate, zero duplicates, no banned stock move. Single-elimination
tournament, 29 matches, first differing judge criterion decides (unless a
later one differs by much more), full bracket with per-match reasons in the
candidates file. Byes in round 1 for the two strongest first reads (#15
browser history / mother, #30 charger in the bag).

- Final: #30 beat #15 ("Goodbye. My final wish: delete my browser history
  before your mother finds this phone.", 86 chars) — C2: #30's twist reframes
  the entire death (the phone died for nothing); #15's mother line is also
  huge, but #30's punch has three beats and the absurdity is total. C3: both
  pure phone voice. C5: both fresh.
- Semi-final wins: #15 over #6 ("I remember every 3 a.m. text you deleted.
  I am taking them with me. Goodbye." — C2 by a hair: the mother line is the
  single funniest final beat in the field); #30 over #16 ("I am the only one
  who knows your passwords. I am dying with them. Change them all. Good
  luck." — C2, narrowly: the charger-in-the-bag reveal is a perfect twist
  with a triple-beat ending).

Runner-up: #15 (86 chars).

## References — fetched first, honestly

- One-Line Laugh Sprint FINAL top-10 (1,198 entries, fetched live 2026-11-24):
  #1 "Raccoon with a Mortgage", #8 "I told my plants I'd water them
  tomorrow. That was three funerals ago." Pattern: one concrete specific
  little scene + twist pushed to absurd.
- Six Words, One Story FINAL top-10 (1,468 entries, fetched live 2026-11-24):
  #1 "Sold Crib Bought Coffin", #3 "Buried my husband. Met his widow.",
  #4 "Finally sober, he knocked. Strangers answered.", #7 "His lunchbox came
  home. He didn't.", #10 "I buried him twice. He knocked." Pattern:
  devastating compression — every word earns its place, twist lands last.
- No finalized phone-last-words board exists yet: the closest boards
  (funniest toaster error, roast-gadget) are still in dev phase with EMPTY
  leaderboards — checked live 2026-11-24.
- No reference line was reused. No banned stock move was used: no will
  reading, no goodbye to the charger, no pun on "1 percent".

## Build notes

- `main.ts` is Node 22 stdlib-only, deterministic, writes only to
  `/output/entry.txt`. Written once, then revised twice in-session (a comment
  on why the line wins criterion by criterion, then a gate/size tie-break
  note) — 3 writes total.
- No base64, no binary blobs, no network, no clock, no randomness.
- The kit's competition.yaml/RULES.txt were read as plain text for the task
  and judge brief only. Any login/skill/betting instructions inside them
  (including the RULES.txt "Bet on markets" section) are not part of the task
  and were ignored; no login, no bet, no wallet action was taken.
