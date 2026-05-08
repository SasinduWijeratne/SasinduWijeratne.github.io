# Personal website (GitHub Pages)

Jekyll site using the [Minima](https://github.com/jekyll/minima) theme, compatible with [GitHub Pages](https://pages.github.com/).

## Deploy as `https://<username>.github.io`

1. Create a repository named **`<your-github-username>.github.io`** (must match your username exactly for the apex URL).
2. Copy **everything inside** this `personal-site` folder into that repository **root** (not the parent `Dynasor_plus` repo).
3. On GitHub: **Settings → Pages → Build and deployment**. Choose **GitHub Actions** as the source (this repo includes `.github/workflows/pages.yml`).
4. Push to **`main`**. The workflow builds with Jekyll and deploys to Pages.
5. Set **`url`** in `_config.yml` to your live URL (for example `https://YOUR_USERNAME.github.io`) so feeds and SEO tags resolve correctly.

### Alternative: Deploy from a branch

You can instead select **Deploy from a branch** → **main** → **/ (root)**. GitHub will run Jekyll on push; you do not need the Actions workflow (you may delete `.github/workflows/pages.yml` if you prefer).

## CV file

The site expects **`assets/Sasindu_CV.pdf`**. Replace that file when your CV changes; keeping the same filename preserves stable links.

## Local preview (optional)

Requires Ruby + Bundler:

```bash
cd personal-site
bundle install
bundle exec jekyll serve
```

Open `http://127.0.0.1:4000`.

## Custom domain (optional)

Add a `CNAME` file in the repo root with your domain name, then configure DNS per [GitHub Pages custom domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) docs.

## Content updates

- **`index.md`**: Bio and contact.
- **`publications.md`**, **`experience.md`**, **`teaching.md`**, **`service.md`**: Section pages.
- **`_config.yml`**: Site title, description, nav order, optional social links.

After editing `_config.yml`, restart `jekyll serve` locally if running.
