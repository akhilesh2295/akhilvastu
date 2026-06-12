# AkkhilVastu

Website for **AkkhilVastu** — a Vastu Shastra consultancy led by **Shaormila Gandhi** (Pune, India). The consultancy offers Vastu guidance for new-home construction, flat-purchase decisions, remediation, career/business growth, and remote consultations for clients in Maharashtra and the USA.

## Tech

- Single static page: [`index.html`](index.html)
- Tailwind CSS via CDN + Google Fonts (Cormorant Garamond + Poppins)
- No build step — open `index.html` in a browser, or host as-is.
- Fully responsive (mobile hamburger nav, stacked layouts).

## Contact wiring

"Book Now" / "Sample report" buttons open **WhatsApp** with a prefilled message; the footer also has an **email** link. Both are driven by two constants near the bottom of `index.html`:

```js
var WA_NUMBER = "919999999999";           // WhatsApp number, international format, no '+'
var EMAIL     = "akhilesh2295@gmail.com"; // contact email
```

Update those two lines with the real number/email — every CTA picks them up automatically. Instagram handle is set in the footer link (`https://instagram.com/akkhilvastu`).

## Placeholders to replace

- Consultant photos (`placehold.co` → real photos of Shaormila)
- Stats numbers (years / consultations) — currently illustrative
- Testimonials — currently sample text, swap with real client quotes
- Confirm consultant name spelling, WhatsApp number, email, Instagram handle

## Deploy (GitHub Pages + custom domain)

1. Push to GitHub. In **Settings → Pages**, set source to branch `main`, folder `/ (root)`.
2. The [`CNAME`](CNAME) file points the site at the custom domain — edit it to your real domain.
3. At your DNS provider, add the GitHub Pages records:
   - `A` records for the apex domain → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - or a `CNAME` for `www` → `<your-username>.github.io`
4. Enable **Enforce HTTPS** once the certificate is issued.
