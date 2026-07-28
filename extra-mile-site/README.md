# Extra Mile — landing page

A single self-contained page (`index.html`) for Extra Mile: build-first, bill-later software
for small businesses. No build step, no dependencies, no external requests — open the file or
drop it on any static host (Netlify, Vercel, Cloudflare Pages, S3, GitHub Pages).

## Design

Identity is **"The Ledger"** — the page is laid out as an itemized statement, because the whole
offer is about what shows up on the invoice and when.

| Token | Light | Dark | Used for |
| --- | --- | --- | --- |
| `--ground` | `#EDEEE9` | `#121413` | page ground (bone-grey / asphalt) |
| `--ink` | `#16181A` | `#ECEEE9` | body + display type, hard rules |
| `--accent` | `#C63F16` | `#FF6A3D` | hi-vis orange: numbers, the promise, primary CTA |
| `--paid` | `#1E6B4A` | `#4FBF8B` | the "$0.00 / free" state |
| `--invert-*` | dark slab | paper slab | the closing block, which flips the page over |

Type is a two-role pairing: a grotesque system stack for the voice (tight tracking, weight 800
display) and a monospace stack for every label, number and structural marker — the ledger voice.
Numbers are `tabular-nums` throughout. Both themes are defined at token level and respond to
`prefers-color-scheme` and a `data-theme` attribute on `<html>`.

Motion is deliberately limited to two things: the hero statement total counting down to `$0.00`
on load, and a scroll reveal on the ledger blocks. Both are disabled under
`prefers-reduced-motion`.

## Things to replace before this goes live

Search `index.html` for these:

- `hello@extramile.example` — contact email (appears 3×, including the CTA `mailto:` links)
- `+10000000000` / `+1 (000) 000-0000` — phone number
- `from $490` — the monthly price in the "Once it's working" tier
- `data-from="8400"` — the number the hero total counts down from (what a build like this
  normally costs up front); pick one that matches your real quotes
- "two to three weeks" — the build window, in step 3, the comparison card, and the FAQ

Everything else is real copy, not placeholder. There are deliberately **no testimonials, client
logos, or result numbers** on the page — add those only once you have real ones, or the
pay-on-results promise is the only proof you're offering and it should stay that way.

## Structure

1. Hero + statement of account (`$0.00 due today`)
2. Terms strip — $0 up front / 30-day proof window / one number
3. `01` The problem — how everyone else charges
4. `02` How it works — the four steps
5. `03` What we build — six offers, each tied to the metric it's judged on
6. `04` What it costs — free, free, then flat monthly
7. `05` The fit — good fit / bad fit
8. `06` Questions
9. Close — book a 30-minute look
