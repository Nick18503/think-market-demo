# Think Market Bids

The Think Market sealed-bid platform, built from the Showroom in the ThinkTLS
repository (`demos/src/variants/showroom`). The backend is the
`showroom-ai-proxy` Cloudflare Worker (D1 + KV); email goes out through Resend.

- `/` — the admin console, behind sign-in. Start a round, upload the bid
  sheet, set reserves, open bidding with **Give the link**, lock, compute and
  approve the results letters.
- `?join=<round>` — the bidder sign-up page. A bidder signs in with their
  name, the one-time access code the seller gave them, and their email.
- `?bid=<token>` — one bidder's private bidding sheet.

This folder is generated: rebuild it with
`npx vite-node demos/scripts/build-share.mjs` from the ThinkTLS repo root and
publish the contents of `demos/share/`.
