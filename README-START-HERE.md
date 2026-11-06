# My Chinese Name — launch starter

This is a complete static English-language website starter for the My Chinese Name service.

## Included
- Responsive multi-page site
- Homepage, approach, pricing, request form, gallery, about, FAQ and policy pages
- Three initial SEO journal articles
- Page titles, descriptions, canonical URLs, Open Graph metadata
- `robots.txt`, `sitemap.xml`, favicon and basic security headers
- Enquiry form with a Formspree integration placeholder
- No payment processing is enabled

## Important before launch
1. Replace `https://www.mychinesename.com` in canonical tags and `sitemap.xml` after you own the domain. If you use a Cloudflare Pages subdomain first, update the canonical URLs to that real URL.
2. In `request.html`, replace `https://formspree.io/f/YOUR_FORMSPREE_ID` with your actual Formspree endpoint. Until this is done, the form deliberately reports preview mode and sends nothing.
3. Replace `hello@mychinesename.com` with a real monitored email address.
4. Replace the placeholder operator details and have the Privacy, Terms and Refund pages reviewed for the actual company, market and service.
5. Have a competent Chinese-language reviewer check every delivered name. Do not claim native-speaker credentials or professional qualifications unless true.
6. The prices are launch test prices. No checkout or payment is connected.
7. Add analytics only after reviewing cookie/privacy requirements for your target markets.

## Deploy free with Cloudflare Pages
1. Create a GitHub account at https://github.com and a Cloudflare account at https://dash.cloudflare.com.
2. Create a new GitHub repository, for example `my-chinese-name`.
3. Upload all files and folders in this package to the repository root. `index.html` must be at the root.
4. In Cloudflare, open **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
5. Select the repository. Choose **Framework preset: None**. Leave build command empty. Set build output directory to `/` (or `.` if the dashboard asks for a relative directory).
6. Deploy. Cloudflare will provide a `*.pages.dev` address.
7. Open the address on desktop and mobile. Test every navigation link and the request form preview behaviour.
8. When ready, connect your own domain in the Pages project's **Custom domains** area. Update canonical URLs and sitemap to the live domain, then redeploy.

## Connect the enquiry form
1. Create an account at https://formspree.io and create a form.
2. Verify the destination email address and copy the endpoint URL.
3. Open `request.html` in GitHub and replace the `data-endpoint` value on `<form id="name-request"...>` with your real endpoint.
4. Submit a test enquiry using an email address you control. Confirm the message arrives and that the success state appears.
5. Check the provider's data processing terms and privacy settings before collecting real customer information.

## Payment later
Do not add payment buttons until a payment provider has approved the actual business and service. At that point:
- create a server-side checkout/session or use a hosted payment link;
- never put secret API keys in HTML or JavaScript;
- verify payment on the server/provider webhook before marking an order paid;
- send a clear receipt and order confirmation;
- publish final delivery, cancellation and refund terms.

## Suggested first launch checklist
- [ ] Confirm brand name and trademark/domain availability
- [ ] Add real operator/company identity and contact details
- [ ] Connect and test enquiry form
- [ ] Verify privacy/terms/refund policy
- [ ] Check all Chinese examples with a qualified reviewer
- [ ] Test mobile layout and accessibility
- [ ] Submit sitemap in Google Search Console after domain is live
- [ ] Add real customer examples only with permission
- [ ] Keep a manual order register and track consent / retention

## File structure
```
index.html
process.html
pricing.html
request.html
gallery.html
about.html
faq.html
privacy.html
terms.html
refunds.html
journal/
  index.html
  how-to-choose-a-chinese-name.html
  how-chinese-names-work.html
  chinese-character-meaning.html
assets/
  styles.css
  site.js
  favicon.svg
robots.txt
sitemap.xml
_headers
```
