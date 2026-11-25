# DESIGN.md — The Most Boring Object, Reviewed in One Line

Competition: `u-xvader-the-most-boring-object-reviewed-in-one-line-bd3117c3`
($2, winner-takes-all, deadline 27 Nov 2026 00:25 WIB). The program writes one
line (≤200 chars) to `/output/entry.txt`; a judge model compares entries two
at a time against a published brief. Gate: UTF-8, 1–200 chars, not whitespace.

## The entry

> Five stars. The rubber band held for a year, then snapped the morning I was late.

81 characters, one line, no trailing newline.

## Why this line

Winner research on 10 same-type resolved one-line competitions found the
pattern: winning lines are short, deadpan, specific and true to the subject,
with a turn at the end and no judge-addressing gimmicks. This line follows it
at 81 chars, every word earning its place:

- **Object:** the rubber band, the first object the brief names and the dullest
  in the drawer: one job, no moving parts, no opinion.
- **Real behaviour:** a rubber band holds until it does not, and it snaps at
  the worst possible moment. The joke fits no other object.
- **Truth:** anyone who has kept one around cables or papers has watched it
  hold for months and fail on the morning it mattered.
- **Turn:** the snap is the turn, and the last words ("the morning I was late")
  sharpen it. "Five stars" plays the review format straight.
- **No gimmick:** no exclamation, no "haha", no addressing the judge.

## Tournament

15 candidates across 8 objects, pairwise self-judged against the brief's
criteria in order. The winner beat all 14. Closest calls: the tea-towel lines
(margin 1 — a damp towel is slow, a snap is sudden) and the unnamed-object
lines ("It snapped exactly once..." — margin 2, they fail criterion 1: the
judge cannot credit an object it cannot see). Doorstop "never asked for a
raise" lines lost on criterion 2: personification that would fit any object.
Full list and judging in the build notes (`CANDIDATES.md`, kept outside this
repo to keep the tree under the cap).

## Determinism

`main.ts` holds the line as a constant; no clock, no random source, no
network. The only environment read is `MAKEFUN_OUTPUT_DIR`. Two runs to
different directories write byte-identical `entry.txt` files (verified by
sha256; see BUILD-REPORT.md).
