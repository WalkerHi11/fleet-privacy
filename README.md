# fleet-privacy

Static host for the privacy policies of the Dizzywalk game fleet. Served on Render (free static
tier) as a dependency-free static site — the publish directory is the repo root, no build step.

## Structure

- `index.html` — landing page linking every game's policy.
- `<game-slug>/privacy.html` — one self-contained policy per game.
- `render.yaml` — Render Blueprint (static site, publish path `.`).

## Live URLs

Base: `https://fleet-privacy.onrender.com/`

| Game | Path |
|---|---|
| Four Square: King of Court | `/four-square-king-of-court/privacy.html` |
| GRAFT: Build-a-Beast Arena | `/graft-build-a-beast-arena/privacy.html` |
| Pull Ya To Chat? | `/pull-ya-to-chat/privacy.html` |
| Black Budget: Spy Deck | `/black-budget-spy-deck/privacy.html` |
| Brink Blitz: Flick Football | `/brink-blitz-flick-football/privacy.html` |
| FRAMEFORGE: Duel of Reads | `/frameforge-duel-of-reads/privacy.html` |
| Empire Heat: Crime Tycoon | `/empire-heat-crime-tycoon/privacy.html` |
| NIGHTFORGE | `/nightforge/privacy.html` |
| Tee'd Off: Battle Golf | `/teed-off-battle-golf/privacy.html` |
| Trivia Munchers | `/trivia-munchers/privacy.html` |

Capeless (`capeless.onrender.com/privacy.html`) and WYRMJOUST (`wyrmjoust.onrender.com/privacy.html`)
are hosted from their own game repos and linked from `index.html`.

## Updating

Edit the HTML and push to `main`; Render auto-deploys. Owner tokens (`{{DEVELOPER_NAME}}`,
`{{OWNER_CONTACT_EMAIL}}`, `{{EFFECTIVE_DATE}}`) are substituted at publish time.
