# walid-ichchou portfolio

Static site: `index.html` + `assets/`. No build step, no framework, no trackers.

## Edit
- All text lives in `index.html`. Projects are the `<article class="case">` blocks, experience is the `<ol class="log">` list.
- Shell commands are in the `cmds` / `files` objects in the `<script>` at the bottom.
- Swap the photo at `assets/walid.jpg` and the CV at `assets/cv-walid-ichchou.pdf`.

## Deploy (free) and point a .dev domain
1. The code lives in `waliddoesthis/portfolio`.
2. Host it on one of:
   - **Cloudflare Pages**: dash.cloudflare.com → Workers & Pages → Create → Pages → connect the repo. Build command: none. Output dir: `/`.
   - **Vercel**: vercel.com/new → import the repo → Framework "Other" → Deploy.
   - **GitHub Pages**: repo Settings → Pages → Deploy from branch `main` / root.
3. Buy the domain (about 10–15 USD/yr): `walidichchou.dev` or `ichchou.dev` at Cloudflare Registrar, Porkbun or Namecheap.
4. Connect it:
   - Cloudflare Pages: project → Custom domains → add the domain (DNS is automatic if bought at Cloudflare).
   - Vercel: project → Settings → Domains → add; then set the DNS records Vercel shows (A `76.76.21.21` for the apex, CNAME `cname.vercel-dns.com` for `www`).
   - GitHub Pages: add a `CNAME` file containing the domain, then A records to 185.199.108.153 / .109 / .110 / .111.
5. `.dev` is HTTPS-only (HSTS preloaded). All three hosts issue the certificate for you; the site will not load over plain http, which is expected.
