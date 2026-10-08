# BG Biocommerce website

Static company website for BG Biocommerce (biotechnology R&D). No build step: the site is plain HTML, CSS and JavaScript in `docs/`.

- `docs/index.html`: the site (English by default, with a BG language switch)
- `docs/fonts/`: self-hosted fonts (Unbounded, Onest, IBM Plex Mono; SIL Open Font License), so no visitor data goes to Google
- `design/concept-v1.html`: the original design concept

## Publish with GitHub Pages

1. Make sure Pages is available: either make this repository **public**, or use a paid GitHub plan (GitHub Pro), which allows Pages from private repositories.
2. In the repository go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Source: Deploy from a branch**, then select the branch that holds the site and the **`/docs`** folder. Save.
4. After a minute the site is live at `https://mzhekov.github.io/bgbiocommerce/`.

## Connect your domain

1. In **Settings → Pages → Custom domain**, enter your domain (for example `www.bgbiocommerce.com`) and save. GitHub adds a `CNAME` file to `docs/`.
2. At your domain registrar, add DNS records:
   - `www` → **CNAME** → `mzhekov.github.io`
   - the bare domain (`@`) → four **A** records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
3. When the domain check passes, tick **Enforce HTTPS**.

## Before going live

- Company details (BG Biocommerce Ltd., UIC 204871800, VAT BG204871800, Plovdiv) and the privacy notice are in the `#privacy` section of `docs/index.html`.
- Contact form: enquiries are delivered by Web3Forms to the email the access key was created with. The key (`FORM_ACCESS_KEY` in `docs/index.html`) is public by design; manage it at https://web3forms.com.
