# Blast Furnace Mass Balance — Vercel deploy

This is a static, single-page app (no build step, no dependencies) — the whole
tool lives in `index.html`. That makes it a zero-config Vercel deployment.

## Option A — Vercel CLI (fastest, no GitHub needed)

1. Unzip this folder somewhere on your laptop.
2. Install the CLI once: `npm install -g vercel`
3. From inside this folder, run:
   ```
   vercel
   ```
4. Answer the prompts (log in / create account on first use, accept the
   defaults — it will detect this as a static project). It gives you a live
   `https://...vercel.app` URL in under a minute.
5. To push updates later: `vercel --prod`

## Option B — GitHub + Vercel dashboard

1. Create a new GitHub repo and push this folder to it:
   ```
   git init
   git add .
   git commit -m "blast furnace mass balance tool"
   git branch -M main
   git remote add origin <your-repo-url>
   git push -u origin main
   ```
2. Go to vercel.com → **Add New Project** → import that repo.
3. Leave the framework preset as **Other** and click **Deploy** — no build
   command or output directory needed since it's plain HTML/CSS/JS.

## Option C — drag and drop

On vercel.com, some account tiers let you drag a folder straight onto the
"New Project" screen instead of connecting Git. Same result.

Once deployed you'll have a permanent URL you can open on any laptop/phone
in class instead of relying on a local file.
