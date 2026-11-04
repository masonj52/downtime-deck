# Downtime Deck

A phone-first flashcard app for spare minutes, built to replace idle scrolling.

**Open it:** https://masonj52.github.io/downtime-deck/

## How it works

- Pick one theme each time you open it. You only see cards from that theme until you switch.
- Choose 2, 5 or 10 minutes (3, 6 or 10 cards). Every session ends.
- Tap an answer or "Show answer", then mark it:
  - **Got it** (or swipe right): comes back after 1, 3, 7, 16, then 35 days.
  - **Again** (or swipe left): skips the rest of this session and opens your next one.
- Progress is stored in your phone's browser (localStorage). No account, no server.

## Themes

Circuits & E&M · C & Memory · Digital Logic · Probability · Markets · Business · Culture Map

## Editing cards

All cards live in the `CARDS` array in `index.html`. Each card has a `t` (theme key), a `q` (prompt), and either
`opts` + `a` (multiple choice, `a` is the correct option text) or `ans` (reveal answer), plus `ex` (explanation paragraphs).
Keep each card's `id` stable so saved progress still matches.
