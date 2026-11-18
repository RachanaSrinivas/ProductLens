# ProductLens — iPhone PWA starter

This is a static, iPhone-first Progressive Web App. It can be hosted free on Cloudflare Pages or GitHub Pages and installed from Safari using **Share → Add to Home Screen**.

## Included now
- iPhone camera/photo-library image selection
- OCR using Tesseract.js (English; library is loaded from a CDN and needs internet for first load)
- Editable brand, product, model, barcode and variant fields
- Product library stored in IndexedDB on the device
- Retailer search links for Amazon India, Flipkart and Myntra
- Manual price observations with timestamp and optional listing URL
- JSON export backup
- Basic offline app shell

## Important limitations (not hidden)
- Retailer links open search results; this build does **not** retrieve live retailer prices or retailer descriptions automatically.
- Exact product identity is not guaranteed by OCR. Confirm model/variant/barcode before relying on a match.
- Saved data is local to this browser/device, not cloud-synchronised. Export backups regularly. Clearing Safari website data may delete it.
- This build has no user accounts and no cloud database.
- OCR uses an external CDN. The rest of the app is static.

## Free deployment using Cloudflare Pages
1. Create/sign in to a Cloudflare account.
2. Open **Workers & Pages → Create → Pages → Upload assets** (wording may vary).
3. Upload the *contents* of this folder (index.html must be at the root).
4. Deploy. Cloudflare gives you an HTTPS `pages.dev` address.
5. On iPhone, open that HTTPS address in Safari → Share → Add to Home Screen.

No paid plan is required for a small personal prototype, subject to the provider's free-plan limits and terms.

## Alternative: GitHub Pages
Create a public repository, upload the folder contents, enable Pages from the repository's Settings, and open the resulting HTTPS Pages address on the iPhone.

## Future work required for the full requested product
To show current prices and original listing descriptions inside ProductLens, integrate permitted retailer APIs/affiliate feeds or other authorised product data sources. API access and eligibility vary by retailer and can change. Do not scrape sites in ways that violate their terms. A durable cloud-synced library also needs a hosted database and an account/authentication design.
