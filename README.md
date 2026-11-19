# Come With Me

A trip guide that keeps itself current.

Most planners generate an itinerary once and then go quiet. A trip keeps moving
after you build it — weather turns, opening hours change, cancellation windows
lapse, bookings get swapped. This is a working prototype of the alternative:
build the guide, then keep it true until you fly home.

Built around one real nine-day trip: Vancouver to Toronto, Montreal, Quebec City
and Niagara — two adults and a fourteen-year-old.

## Live site

https://amnsmn.github.io/Come_with_me/

## The five screens

| Page | What it is |
|---|---|
| `index.html` | Landing page — the argument, and links to everything below |
| `build.html` | Input flow: dates, stops, travellers, bookings, and the brief |
| `share.html` | Read-only share view where friends suggest, vote and offer rides |
| `changes.html` | The watch feed — what changed since you planned, with diffs |
| `guide.html` | The guide with applied changes rewritten in place, plus revert |
| `today.html` | The day-of mobile view: what's now, what changed overnight |

Every page is a single self-contained HTML file. No build step, no dependencies,
no framework. Fonts come from Google Fonts; everything else is inline.

## Enabling GitHub Pages

1. Push these files to the `main` branch.
2. In the repo, go to **Settings -> Pages**.
3. Under **Source**, choose **Deploy from a branch**.
4. Set branch to **main** and folder to **/ (root)**, then **Save**.
5. Wait about a minute, then open the live URL above.

`.nojekyll` is included so Pages serves the files verbatim rather than running
them through Jekyll.

## Status

Real: all five screens, fully interactive — the flows, the state, the decisions,
the reverts. Every change shown came from an actual planning session.

Simulated: reading uploaded confirmations, and the live weather / hours / price
feeds. The values are real but fixed, not polling.

Next: wiring places, hours and weather APIs behind every suggestion, so nothing
is invented and every price carries a date.

---

Prototype built 2026-11-19.
