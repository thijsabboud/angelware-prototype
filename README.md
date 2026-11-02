# Angelware prototype

A clickable prototype of Angelware, "WhatsApp for AI agents": one app where people meet all their agents, each in its own chat. Agents can message you first and answer with interactive screens (MCP Apps). One agent can serve several people, each in a private chat.

**This is a prototype. Every agent, message and number in it is simulated.** Nothing here is a live product.

Live at https://angelware.auconsulting.ai (behind an access code).

## What's in it

One self-contained `index.html` (inline CSS and JavaScript, one Google Font, no build step) and a `CNAME`. Eleven scenes, picked from the list beside the phone or with the arrow keys:

1. Your agents: seven agents from seven builders, each with a "built by" badge, plus a morning digest that bundles the non-urgent updates
2. Check-in: a notification, a one-tap reply, a guided session that marks itself done once it plays to the end, then you say how it went in your own words, by voice or typing, and tomorrow's session adapts
3. A live screen in the chat: a workout log you fill in, a progress chart, then a permission to share health data from your wearable
4. One agent, two phones: coach and client, each in a private chat, plus the coach's overview of all her clients
5. Patient updates for a family (fictional patient and hospital)
6. Household: the kids' to-dos, ticked off by connected devices like the dishwasher, and a reminder (fictional kids)
7. Charging: "your car is charged, spot 4", then pay with the phone's wallet
8. Shopping: a web shop's agent with your orders; it pays below your auto-approve limit, and above it your phone's wallet asks (fictional shop)
9. Agents work together: a cycle coach sends the PT agent a note, only after you allow it
10. Builder side: publish an agent ($49 per agent per month), decide what data it collects and what each role sees, and see analytics
11. Rules per agent: message first, quiet hours, digest, auto-approve spend, connections, and a log of what it saw and did today

Phone frame on desktop, full screen on a phone. Light and dark.

## Run locally

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765.

## Access code and analytics

The access code is a speed bump, not security: the codes are in the source.

Cloudflare Web Analytics loads only after a tracked code is entered, so every pageview in the dashboard is a real open. To turn it on, add the site in Cloudflare (Analytics, Web Analytics), copy the beacon token and set `CF_BEACON_TOKEN` near the top of the script.

## Hosting

GitHub Pages from `main`, with a DNS-only CNAME record `angelware` pointing to `thijsabboud.github.io`.
