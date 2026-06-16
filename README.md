# elcerrito-apex-redirect

Single-purpose GitHub Pages site that 301-redirects `https://elcerritorestaurante.com` -> `https://www.elcerritorestaurante.com`.

## Why this exists

Cloudflare Pages requires DNS authority for apex domains. This is impossible when
Wix locks nameservers on Wix-registered domains. GitHub Pages provides free apex
SSL via Let's Encrypt and stable anycast IPs for apex A records.

## DNS records (at Wix DNS panel)

Apex `elcerritorestaurante.com` -> 4 A records:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153

`www.elcerritorestaurante.com` CNAME -> `elcerrito.pages.dev` (handled by CF Pages)

## Real site

The actual website is at https://github.com/alejandro067/elcerrito.
