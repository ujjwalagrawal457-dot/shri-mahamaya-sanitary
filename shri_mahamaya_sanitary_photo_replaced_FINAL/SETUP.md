# Shri Mahamaya Sanitary — Free Publishing Setup

This package is prepared for a free GitHub + Cloudflare Pages + Pages CMS workflow.

## What is already done

- Current website preserved.
- Shop photo replaced with the newly provided storefront photo.
- Shop name is **श्री महामाया सेनेटरी**.
- Content moved to `data/site.json` so it can be edited from Pages CMS.
- `media/shop.jpg` contains the storefront image.
- `.pages.yml` configures editable shop settings, categories, products/services and images.
- The website loads `data/site.json` when online.

## Your setup steps

### Step 1 — Create a GitHub account
Go to https://github.com/ and create/sign in to your account.

### Step 2 — Create a repository
Create a new repository, e.g. `shri-mahamaya-sanitary`.
Keep it private if you want; Cloudflare Pages supports private GitHub repositories.

### Step 3 — Upload this package
Upload **all files and folders** from this package into the repository root. Make sure `index.html` is at the root.

### Step 4 — Create Cloudflare account
Go to https://dash.cloudflare.com/ and create/sign in to a free account.

### Step 5 — Deploy
Cloudflare Dashboard → Workers & Pages → Create application → Pages → Connect to Git.
Select GitHub and the repository.

For this plain HTML site:
- Production branch: `main`
- Build command: leave blank (or `exit 0`)
- Build output directory: `.`

Deploy.

Cloudflare will give you a free `*.pages.dev` website address.

### Step 6 — Set up your editor
Go to https://app.pagescms.org/

Sign in with the same GitHub account.
Install/authorize the Pages CMS GitHub App for the repository.
Open your repository and select the `main` branch.
Pages CMS will read `.pages.yml`.

You will then be able to edit:
- Shop name and tagline
- Shop photos
- WhatsApp number
- Categories
- Products
- Services
- Product images
- Stock

Save changes in Pages CMS. The change is committed to GitHub, and Cloudflare Pages automatically redeploys the site.

## Important

The built-in `Edit shop` button in the website is retained from the existing prototype, but it stores changes only in that browser. For permanent public changes, use **Pages CMS**.

## Custom domain later

You can connect a purchased domain to Cloudflare Pages later. The free `pages.dev` address is enough to launch first.


CORRECTION APPLIED
- Shop image paths are relative (`media/shop.jpg`) so the image works in local preview and after Cloudflare deployment.
- Service enquiries now open the ordering/details page first; Name, Mobile Number and Village/Area are mandatory. Only after validation is the customer sent to WhatsApp.
