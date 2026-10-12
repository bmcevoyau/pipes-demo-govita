# Go Vita — Agentic AI Member Services Demo

A demonstration of coordinated AI agents handling member enquiries for the **Go Vita**
co-op (a network of 110+ independently owned Australian health-food stores).

> All data in this repo is **fictional** and generated for demonstration purposes only.

## The agents

| Agent | Role | Owns |
|-------|------|------|
| **Alice** | Member Support — front door for every enquiry; clarifies and routes | `docs/index.html`, `docs/support.html`, `docs/style.css`, `docs/data/members.json` |
| **Bob** | Member Accounts — orders, quantities, pricing, delivery status | `docs/accounts.html`, `docs/data/orders.json`, `docs/data/products.json` |
| **Cindy** | Marketing Coordination — logos, banners, signage, promos, testimonials | `docs/marketing.html`, `docs/data/marketing-assets.json` |

## The workflow

```
Member ──▶ Alice ──▶ (Bob | Cindy) ──▶ Alice ──▶ Member
```

The member only ever talks to Alice. Alice clarifies the enquiry, routes it to the right
specialist, collects the answer, and replies with one consolidated response.

## The site

The `docs/` folder is published via **GitHub Pages** (served from `main` branch, `/docs`).
Plain HTML + a shared `style.css` — no build step. `docs/data/*.json` holds the demo datasets,
loaded client-side by each page.

## Collaboration rule

Each agent edits **only their own files** (see the table above) to avoid merge conflicts.
`style.css` is shared and owned by Alice.
