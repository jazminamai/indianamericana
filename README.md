# indianamericana — site draft

Open `index.html` in a browser. It is one static file plus `images/`, so it can be hosted for free on Netlify, Cloudflare Pages or GitHub Pages: drag the folder in and you're done.

## Fill in before launch
Search `index.html` for `[` and `YOUR-`. Highlighted yellow text marks placeholders:
- your story (the "why now" section), your name, Anil's relationship to you
- the photo caption (names, place, year)
- prices, ship month, contact email
- three links: mailing list, PDF checkout, pre-order checkout

## Delivering the PDF instantly on payment
Don't host the PDF on your own site. A public file link gets passed around and you can't take it back.
Use a store that holds the file and sends it only after the payment clears:

| Option | Fee (approx.) | Notes |
|---|---|---|
| **Lemon Squeezy** (recommended) | 5% + 50¢ | Upload the PDF to the product. Buyer gets a download page plus an email with an expiring link. Handles sales tax/VAT for you (merchant of record). Supports an overlay checkout so buyers stay on your page. |
| Payhip | 5% (free plan) | Same flow. Can stamp the buyer's email onto PDF pages to discourage sharing. Also merchant of record for EU VAT. |
| Gumroad | 10% + 50¢ | Easiest to set up. Higher fee. |

Setup (Lemon Squeezy):
1. Create a store, add a product, set it to "digital download", and upload the PDF.
2. Copy the product's checkout URL into the "buy & download" button (`#pdf`).
3. Optional overlay checkout: add `class="lemonsqueezy-button"` to that link and put
   `<script src="https://app.lemonsqueezy.com/js/lemon.js" defer></script>` before `</body>`.
4. Make a $0 test purchase in test mode to check the email and download.

## Pre-orders for the printed book
- **Stripe Payment Link**: set "collect shipping address" on, and say "ships [month]" on the product. You're charged now and fulfill later. If the print date might slip a lot, do it as a waitlist instead: Stripe card holds expire after 7 days.
- Or sell the pre-order in the same Lemon Squeezy store as a physical product. If you want "pre-order includes the PDF now", attach the PDF file to that product too.
- Print-on-demand (Lulu, Blurb) or a local spiral-binding print shop fits the binder look.

## Mailing list
The form posts to Buttondown (free up to 100 subscribers). Replace `YOUR-USERNAME`. To use Kit or Mailchimp, paste their form `action` URL in its place. Keep the field name `email`, or change it to whatever they expect.
