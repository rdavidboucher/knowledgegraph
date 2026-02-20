# Philosophical Connections

477 nodes · 442 edges · 19 thinkers

## Deploy to Render.com

1. Push this directory to a GitHub repo (public or private)
2. Go to https://dashboard.render.com → New → Static Site
3. Connect your GitHub repo
4. Settings:
   - **Build Command**: leave blank (or `echo done`)
   - **Publish Directory**: `.`
5. Click Deploy

That's it. Render will serve `index.html` and the `data/` folder automatically.

## Local Development

Do not open `index.html` directly in a browser — the `fetch()` calls will
fail due to CORS restrictions on the `file://` protocol.

Instead, run a local server:

```bash
cd phil_site
python3 -m http.server 8000
# then open http://localhost:8000
```

## File Structure

```
phil_site/
├── index.html          # Full application
├── render.yaml         # Render.com config
├── README.md
└── data/
    ├── nodes.json      # 477 philosophy nodes
    └── edges.json      # 442 edges (5 types)
```

## Graph Controls

| Control | What it does |
|---|---|
| Edge type toggles | Show/hide contradicts, converges, extends, mirrors, undermines |
| Highlight author | Dim all nodes except one thinker |
| Min edge weight | Only show strong (2+) or very strong (3) edges |
| Reset view | Re-center the graph |
| Click node | Open detail panel with full text + connections |
| Click connection | Jump to that node |
| Authors legend | Color key for all 19 thinkers |
| Scroll/pinch | Zoom |
| Drag canvas | Pan |
| Drag node | Reposition |
