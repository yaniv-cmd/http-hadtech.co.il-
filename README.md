# HadTech website (hadtech.co.il)

Static bilingual (EN/HE) site. Just static files, host anywhere.

## Files
- index.html      main page (self-contained: CSS + JS inline, SVG graphics)
- og-image.png    social / search preview image (1200x630)
- CNAME           custom domain for GitHub Pages (hadtech.co.il)
- robots.txt      allows all crawlers + AI bots, points to sitemap
- sitemap.xml     search-engine sitemap
- llms.txt        summary for AI / LLM crawlers (root convention)
- content.md      full text (EN + HE) for indexing
- 404.html        redirect to home

## Host on GitHub Pages (recommended)
1. Create a repo and upload all these files to the root of the default branch.
2. Settings > Pages > Build and deployment: Source = "Deploy from a branch",
   Branch = main, folder = / (root). Save.
3. The CNAME file sets the custom domain to hadtech.co.il automatically.
4. Add the DNS records below at your DNS provider (Domain The Net / dtnt.info).

## DNS records for hadtech.co.il (add at Domain The Net)
Apex domain (host "@") -> four A records to GitHub Pages:
  A   @   185.199.108.153
  A   @   185.199.109.153
  A   @   185.199.110.153
  A   @   185.199.111.153
(optional IPv6)
  AAAA @  2606:50c0:8000::153
  AAAA @  2606:50c0:8001::153
  AAAA @  2606:50c0:8002::153
  AAAA @  2606:50c0:8003::153
www subdomain -> CNAME to your GitHub Pages host:
  CNAME  www   <your-github-username>.github.io.

After DNS propagates, enable "Enforce HTTPS" in Settings > Pages.

## Notes to update before launch
- LinkedIn URL in index.html (currently https://www.linkedin.com/in/yaniv-hadar) - set your real profile.
- Email yaniv@hadtech.co.il - make sure this mailbox exists, or change it.
