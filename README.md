# InsightFlowAI — AI Terms Site

Static site powering the AI Terms & Safety page used by the app.

## Structure

- `index.html` — redirects to `/ai-terms/`
- `ai-terms/index.html` — the terms content
- `vercel.json` — config for Vercel static hosting

## Quick Deploy (Vercel)

Prereqs: Node.js, Vercel CLI, a Vercel account with access to your domain.

```bash
cd ai-terms-site
vercel login
vercel --prod --name insightflow-ai-terms
```

Then in the Vercel dashboard:
- Connect your project to this repo for auto‑deploys
- Set Production Domain to your domain (e.g. `insightflowai.com`)
- Add DNS per Vercel’s instructions

## GitHub Remote

```bash
cd ai-terms-site
git init
git add .
git commit -m "chore(terms): initial site"
# Using GitHub CLI
gh repo create insightflow-ai-terms --public --source . --remote origin --push

# Or manually
git remote add origin git@github.com:<you>/insightflow-ai-terms.git
git branch -M main
git push -u origin main
```

## Customizing

- Update copy in `ai-terms/index.html`
- Adjust caching/headers in `vercel.json`
- If serving at the root of a subdomain, you can remove the `index.html` redirect and place the content at root

