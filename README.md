# Rush

A single-tasking timer disguised as a squad game. Name one objective, set the clock, deploy a soldier. Finish in time and they rank up. Let the clock win and they die.

Plain HTML, no build step.

- `public/index.html` is the whole app.
- `public/img/` holds the sprites: `<species>_1.webp` to `<species>_5.webp` (ranks) and `<species>_fallen.webp`.
- Progress is saved in the browser (localStorage), per device.

## Deploy (Cloudflare)

Cloudflare dashboard: Workers & Pages → Create → Import a repository → pick this repo.
Leave the build command empty; the deploy command is `npx wrangler deploy`.
Add a custom domain under the Worker's Settings → Domains & Routes (e.g. `rush.adders.party`).
Every push to `main` redeploys.
