# SleekSlateStudio Website

A storefront website that showcases your Etsy listings and sends buyers to Etsy to check out.
Built with Jekyll so GitHub Pages builds and hosts it for free — no coding required for day-to-day updates.

## 1. Put this on GitHub (no command line needed)

1. Go to github.com and create a **new repository**.
   - Name it exactly `YOURUSERNAME.github.io` (replace YOURUSERNAME with your actual GitHub username) — this gives you a free live site at `https://YOURUSERNAME.github.io`.
   - Keep it Public.
2. Open the new repo, click **"Add file" → "Upload files"**.
3. Drag in every file and folder from this project (keep the folder structure — e.g. `_layouts`, `_includes`, `_data`, `shop`, `assets` all need to go in as-is).
4. Click **Commit changes**.
5. Go to **Settings → Pages** in the repo. Under "Build and deployment", set Source to **"Deploy from a branch"**, branch `main`, folder `/ (root)`. Save.
6. Wait 1–2 minutes, then visit `https://YOURUSERNAME.github.io` — your site is live.

## 2. Add a new product (takes 1 minute)

Open `_data/products.yml` in GitHub (click the file, then the pencil "Edit" icon), copy an existing block, and paste it at the bottom with your new item's details:

```yaml
- title: "Your Listing Title"
  category: "Formula 1"          # must match an existing category, or type a brand-new one
  price: "7.99"
  original_price: "15.98"        # optional — leave off if there's no sale
  url: "https://www.etsy.com/listing/XXXXXXXXX/your-listing-slug"
  image: "/assets/img/placeholder.svg"   # swap for a real photo URL — see step 3
```

Commit the change — the live site updates automatically within a minute or two.
**A brand-new category name automatically gets its own homepage tile**, but you'll also want to
copy one of the files in `/shop/` (e.g. `formula-1.html`) and change its `category` filter to match,
so there's a dedicated page for it too.

## 3. Add real product photos

Right now every listing uses a placeholder image so the site isn't blocked on missing photos.
To swap one in:
1. Open the listing on Etsy, right-click the main photo, choose **"Copy image address"**.
2. Paste that link into the `image:` field for that product in `_data/products.yml`.

(Or upload photos into `assets/img/products/` in GitHub and reference them as `/assets/img/products/filename.jpg`.)

## 4. Files at a glance

- `_config.yml` — site title, tagline, your Etsy shop link
- `_data/products.yml` — every product listing lives here
- `index.html` — homepage
- `shop/*.html` — one page per category, plus `all.html` for everything
- `assets/css/style.css` — all styling, using your brand palette
- `assets/img/logo.png`, `banner.png` — your uploaded logo and banner

## 5. Next steps worth doing

- Swap placeholder images for real Etsy photos (step 3 above).
- Once live, submit the site to **Google Search Console** so Google starts indexing it.
- If you buy a custom domain later, add it in Settings → Pages → Custom domain, and update `url:` in `_config.yml`.
