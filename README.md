# AI-SPOT — Interactive Elements

Self-contained, single-file HTML modules for the AI-SPOT platform
(Republic Polytechnic, School of Sports and Health). Each module is fully
standalone — all images and fonts are embedded, no build step, no external
runtime dependencies — and is meant to be embedded into aispot.hpilab.net.

## Structure
    aispot/
    ├── index.html        # hub / landing that links to each module
    ├── hero/index.html   # animated cinematic hero  (DONE)
    ├── monitor/index.html# injury risk monitoring   (coming soon)
    ├── coach/index.html  # pitch control analysis   (coming soon)
    └── evaluate/index.html# player value evaluation (coming soon)

## Deploy with GitHub Pages
1. Create a public repo named **aispot**.
2. Upload the contents of this folder so the paths match above
   (drag-and-drop the folders in the GitHub web UI, or use git).
3. Repo → Settings → Pages → Build and deployment → Source = "Deploy from a
   branch", Branch = **main**, folder = **/ (root)**. Save.
4. After ~1 minute the modules are live at:
       https://aaron-chen-angus.github.io/aispot/
       https://aaron-chen-angus.github.io/aispot/hero/
       https://aaron-chen-angus.github.io/aispot/monitor/
       https://aaron-chen-angus.github.io/aispot/coach/
       https://aaron-chen-angus.github.io/aispot/evaluate/
       https://aaron-chen-angus.github.io/aispot/video/

       
## Embed a module in the website (e.g. in KIMI)
    <iframe src="https://USERNAME.github.io/aispot/hero/"
            style="width:100%;aspect-ratio:16/9;border:0;display:block"
            loading="lazy" title="AI-SPOT Hero"></iframe>

## Custom domain (later)
To serve under aispot.hpilab.net directly from GitHub Pages: add a `CNAME`
file containing `aispot.hpilab.net` at the repo root, then point a DNS CNAME
record for that subdomain to `USERNAME.github.io`. (Or simply keep embedding
the github.io URLs via iframe inside the KIMI-built site.)
