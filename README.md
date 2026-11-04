# Payment page

A standalone payment page with its own control panel. It has no connection to any other site.

- `index.html` – the payment page and its control panel (open `/#admin`)
- `content.json` – every text, colour, package and payment detail
- `assets/uploads/` – logo and package images uploaded from the panel
- `404.html` – sends unknown addresses back to the payment page

## Set up
1. Upload these files to a new **public** repository and turn on **Settings → Pages → Deploy from a branch → main / (root)**.
2. Create a fine-grained token for **this repository only** with **Contents: Read and write**. Use a different token from any other site.
3. Open `/#admin`, connect the device, then add your payment methods under **Payment methods**.

## Security
- No login file is stored in this repository. Each device keeps its own copy of the token, encrypted with your panel password.
- The panel signs out after 30 minutes idle and slows down repeated wrong passwords.
- The page never handles card or bank details. Payments happen in UPI apps or on Razorpay, Stripe or PayPal.
- Keep GitHub two-factor login on, and check the commit history if a payer reports a wrong payee.
