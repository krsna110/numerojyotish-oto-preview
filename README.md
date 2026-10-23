# Mahaacharya Numerology OTO preview

## Pages

- `index.html` — webinar confirmation and ₹299 report offer (main entry point).
- `numerojyotish_oto_conversion.html` — legacy redirect to `index.html`.
- `sample-numerology-report.html` — fictional report sample (Life Path 3, Birth Number 7).
- `payment-confirmation.html` — post-checkout landing page with two WhatsApp contact buttons.

## Before publishing

1. Replace the sample webinar date/time and WhatsApp group link in the offer page.
2. Add the Razorpay Payment Link to the offer page. Configure the Payment Link callback URL to the deployed `payment-confirmation.html` and callback method `GET` in Razorpay. Razorpay documents that a callback URL redirects the customer after checkout; confirm paid status using Razorpay's payment data or webhook before marking an order fulfilled.
3. In `payment-confirmation.html`, replace `WHATSAPP_SALES` and `WHATSAPP_SUPPORT` with the two phone numbers in international format, digits only (for example, India `91` followed by the ten-digit number). Replace the fallback email address too.
4. The 15-minute countdown currently runs in the browser session as a visual preview only; checkout remains open when it ends. Do not describe this as a real offer expiry until you enforce the deadline through an expiring payment link or trusted server.
5. Replace fictional sample content with the exact deliverables and delivery terms you will provide. The sample is not a customer reading.

Razorpay reference: [Payment Links API](https://razorpay.com/docs/api/payments/payment-links/).
