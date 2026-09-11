# Structure Lab AU

Live shareable site: **https://v2-prog.github.io/**

Custom domain target: **https://earthacer.in/** (after Hostinger DNS or File Manager upload).

Source repo: https://github.com/v2-prog/structure-lab

## Make earthacer.in serve this site

DNS currently still points at Hostinger parking (`cosmos.dns-parking.com` / `nova.dns-parking.com`). Pick one method.

### Fastest — upload into Hostinger (keep current DNS)

1. Hostinger hPanel → **Files** → **File Manager** → open `public_html`
2. Delete the default parked `index.html`
3. Upload the site files from this repo (`index.html`, `404.html`, `favicon.svg`, `og.jpg`, `site.webmanifest`, and the `assets` folder)
4. Wait a minute and open https://earthacer.in

### Or point the domain at GitHub Pages

This repo already contains a `CNAME` file for `earthacer.in`.

In hPanel → Domains → earthacer.in → **DNS / DNS Zone Editor**:

| Type | Name | Points to |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `v2-prog.github.io` |

Remove the old Hostinger A records (`191.101.104.37`, `212.1.212.231`) and the `www` CNAME to `cdn.hstgr.net`. Leave MX records alone if you use Hostinger email.

Then open https://github.com/v2-prog/v2-prog.github.io/settings/pages and tick **Enforce HTTPS** once GitHub verifies the domain.
