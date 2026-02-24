# bradpalmerofficial.com

Personal brand site for Brad Palmer — AI, Ads, Luxury Concierge & Coaching.

## Structure

```
bradpalmerofficial/
├── index.html          ← Single-page site (all CSS/JS inline)
├── assets/
│   └── headshot.jpg    ← Hero photo (500x500, optimized)
├── netlify.toml        ← Netlify deploy config
└── README.md
```

## Deploy to Netlify via GitHub

### 1. Push to GitHub

```bash
cd bradpalmerofficial
git init
git add .
git commit -m "Initial site launch"
gh repo create bradpalmerofficial --public --source=. --push
```

Or manually:
```bash
git remote add origin git@github.com:YOUR_USERNAME/bradpalmerofficial.git
git branch -M main
git push -u origin main
```

### 2. Connect Netlify

1. Go to [app.netlify.com](https://app.netlify.com)
2. **Add new site → Import an existing project → GitHub**
3. Select the `bradpalmerofficial` repo
4. Build settings:
   - **Build command:** *(leave blank — static site)*
   - **Publish directory:** `.`
5. Click **Deploy site**

### 3. Custom Domain

1. In Netlify → **Domain management → Add custom domain**
2. Enter `bradpalmerofficial.com`
3. Update your DNS:
   - If using Netlify DNS: point nameservers to Netlify
   - If using external DNS: add a `CNAME` record pointing to your Netlify subdomain (e.g. `amazing-site-abc123.netlify.app`)
4. Netlify auto-provisions HTTPS via Let's Encrypt

## Working in Claude Code

Once the repo is on GitHub, open it with Claude Code:

```bash
claude
# then in Claude Code:
# > open the bradpalmerofficial repo
```

### Things to customize next

| What | Where in `index.html` |
|---|---|
| Booking link | Search `calendly.com/bradpalmer` — replace with your actual link |
| InstaProfit Kit link | Search `href="#"` on the 03 card — replace with purchase URL |
| Email address | Search `hello@bradpalmerofficial.com` — update if different |
| Metric numbers | Search the `ticker` section — update stats to real figures |
| Photo | Replace `assets/headshot.jpg` |

### Future improvements to consider

- Add `favicon.ico` and Open Graph meta tags for social sharing
- Add Google Analytics or Plausible snippet
- Split CSS into `css/style.css` and JS into `js/main.js` if the file gets larger
- Add a `/instaprofit` landing page for the digital product
- Add schema.org structured data for SEO
