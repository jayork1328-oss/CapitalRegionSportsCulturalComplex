# CRSCC Publish Package — Deployment Checklist

This folder contains everything needed to publish the CRSCC landing page and documents.

## Files
- `CRSCC_landing_page_analytics_with_renderings.html` — main public page
- `CRSCC_Proposal.pdf`, `CRSCC_Impact_Report.pdf`, `CRSCC_One_Pager.pdf` — public documents
- `CRSCC_Renderings.zip` + individual PNG thumbnails
- `crscc-og-1200x630.png` — social share image (Open Graph)
- `favicon.png` + `favicon.ico` — site icons
- `robots.txt` and `sitemap.xml` — for SEO and indexing
- `Press_Release_CRSCC_Public_Proposal.pdf` — media-ready announcement
- `CRSCC_Social_Copy.txt` — ready-to-post social captions

## Steps (Any Host)
1. Upload the HTML file and all assets into the same folder on your host.
2. Update links inside the HTML if you host PDFs at a different path (search for `CRSCC_Proposal.pdf`, etc.).
3. Replace `G-XXXXXXX` in the HTML with your Google Analytics ID (or remove GA if not used).
4. Replace `your-domain.org` in `sitemap.xml` and `<meta>` tags with your real domain.
5. Upload `robots.txt` and `sitemap.xml` to your site root (e.g., `https://your-domain.org/robots.txt` and `/sitemap.xml`).
6. Submit your site in Google Search Console for indexing.

## Hosting Options (Choose One)
### A) Squarespace / Wix (Easiest)
- Create a site → add a new page → use a “Code/HTML” block → paste the **body** content of the HTML or upload the HTML as a custom page if supported.
- Upload PDFs and images to the site’s file manager; update the links in your page.

### B) WordPress (Flexible)
- Use your host’s file manager (or an SFTP client) to upload the HTML & assets to a directory (e.g., `/crscc/`). 
- Alternatively, create a page and paste the HTML into a “Custom HTML” block; upload PDFs/media to the Media Library and replace links.

### C) Netlify (Fast Static Hosting)
- Create a new site from a folder. Drag-and-drop this entire folder in the Netlify dashboard.
- Set a custom domain under “Domain management” (use your registrar’s DNS to point to Netlify).

### D) GitHub Pages (Free)
- Create a repo (`crscc-site`) → upload files → enable GitHub Pages in settings → choose main branch `/root`.
- Your site appears at `https://<username>.github.io/crscc-site/`. Point a custom domain if desired.

## DNS & Domain
- Register a memorable domain (e.g., `crscc.org`).
- In your registrar (Namecheap/GoDaddy/Cloudflare), set DNS per your host’s instructions (A/AAAA/CNAME records).
- Add the domain to your host (Squarespace/Wix/Netlify/WordPress) and verify.

## After Launch
- Test open‑graph previews (Facebook Sharing Debugger, Twitter Card Validator).
- Verify indexing in Google Search Console.
- Track visits in GA/Plausible and iterate content as media coverage grows.
