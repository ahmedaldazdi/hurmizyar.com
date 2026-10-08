# hurmizyar.com

Static holding page for **Hurmizyar OÜ** — an Estonian software company building
products with a focus on Kurdish culture and language, and practical SaaS tools
for companies in Kurdistan and Europe.

## Products

- **Viatrum** — https://viatrum.eu — logistics and operations platform for wind turbine repair work.
- **Peyvistan** — https://peyvistan.app — Kurdish-language learning app.

## Files

The site is static with no build step:

- `index.html`, `404.html`, `styles.css`, `favicon.svg`
- `fonts/` — Inter, self-hosted (SIL Open Font License, `fonts/OFL.txt`), so
  visitors' browsers never contact Google Fonts
- `robots.txt`, `sitemap.xml`
- `vercel.json` — clean URLs, security headers (including a strict
  Content-Security-Policy: no scripts, no third-party resources) and long caching
  for the font. Adding an external script, font or image means widening that policy.

The page follows the visitor's light or dark setting.

## Deploying

Hosted on Vercel (team "ahmedaldazdi's projects", project `hurmizyar-com`), linked
to this repository: every push to `main` deploys to production.

The domain's DNS stays at Wix, which also holds the Zoho Mail records (MX, SPF,
verification TXT). Keep those when changing DNS. The web records are:

| Type  | Host  | Value                                  |
| ----- | ----- | -------------------------------------- |
| A     | `@`   | `216.150.1.1`                          |
| A     | `@`   | `216.150.16.1`                         |
| CNAME | `www` | `05b91171b67666fb.vercel-dns-016.com`  |

These are the values Vercel recommended on 2026-10-08. The older generic values
(`A 76.76.21.21`, `CNAME cname.vercel-dns.com`) also work.

`www.hurmizyar.com` redirects to `hurmizyar.com` (set in the Vercel project's domains).
