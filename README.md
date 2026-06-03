# Privacy Policy — Do I Need This?
 
**Last updated: June 2026**
 
This privacy policy describes how Do I Need This? ("the extension", "we", "us") collects, uses, and shares information about you when you use our Chrome browser extension.
 
---
 
## Who we are
 
Do I Need This? is an independent Chrome extension that helps users pause and reflect before completing online purchases. The extension is not affiliated with Google, Amazon, or any retailer.
 
---
 
## What data we collect and why
 
### 1. Email address
**When:** If you choose to create an account and sign in.
**Why:** To sync your purchase history and settings across multiple devices.
**Stored:** On our Supabase-hosted database servers.
**Required:** No. You can use the extension without signing in. Signing in is optional and only needed for cross-device sync.
 
### 2. Authentication tokens
**When:** When you sign in via the email OTP (one-time code) flow.
**Why:** To keep you logged in across browser sessions without requiring you to sign in repeatedly.
**Stored:** Locally in your browser using `chrome.storage.local`. Tokens are refreshed automatically every 50 minutes and are never shared with third parties.
 
### 3. Purchase and cancellation records
**When:** Each time the checkout prompt appears and you click "Yes, I need it" or "No, go back."
**What we record:**
- The hostname of the retailer site (e.g. `amazon.com`) — not the full URL
- The cart total detected on the page, if one could be found
- The reason you typed, if you chose to enter one (optional)
- The date and time of the event
- Whether you proceeded with or cancelled the purchase
**Why:** To power the spending dashboard and give you insight into your purchasing habits.
**Stored locally:** In `chrome.storage.sync` on your device.
**Stored remotely:** In our Supabase database if you are signed in, linked to your user account.
 
### 4. Cart total (financial information)
**When:** When a checkout page is detected.
**Why:** To display your cart total in the prompt and record it alongside each purchase event.
**How:** The extension reads visible text from the checkout page DOM to find the order total. It does not read, transmit, or store credit card numbers, bank details, or any payment credentials. Payment processing is handled entirely by the retailer and is never seen by this extension.
 
### 5. Checkout page detection (web activity)
**When:** On every webpage you visit.
**Why:** The extension must monitor pages to detect when a checkout button is present so it can show the prompt at the right moment.
**What we do NOT do:** We do not log, transmit, or store a list of websites you visit. The content script runs silently on all pages and only becomes active when a checkout button is detected. Non-checkout pages are not recorded.
 
### 6. Click events (user activity)
**When:** On every webpage you visit.
**Why:** The extension listens for click events to intercept clicks on checkout buttons before they are processed.
**What we do NOT do:** We do not log general clicks, mouse movements, keystrokes, or browsing behaviour. Only clicks on identified checkout buttons trigger any action.
 
### 7. IP address (indirect)
**When:** When you sign in or when your purchase records sync to our database.
**Why:** Your IP address is transmitted as a standard part of any internet connection and is received by our Supabase database servers. We do not explicitly collect or store IP addresses, but they may appear in server access logs maintained by Supabase.
 
### 8. Payment status
**When:** On extension load and hourly thereafter.
**Why:** To determine whether you have an active paid subscription and unlock premium features accordingly.
**How:** The extension calls ExtensionPay's servers, which check your payment status against Stripe's records using your browser identity. We do not collect or store credit card numbers. Payment processing is handled by Stripe via ExtensionPay.
 
---
 
## What data we do NOT collect
 
- Full URLs or page titles of websites you visit
- Passwords or login credentials for any website
- Credit card numbers or banking information
- The content of your emails, messages, or communications
- Your physical location or GPS data
- Health information of any kind
- Information about other browser tabs or windows
---
 
## How we use your data
 
We use the data described above solely to:
 
1. Show you a personalised spending prompt at checkout
2. Power the spending dashboard in the extension
3. Sync your history and settings across your devices (if signed in)
4. Determine whether premium features should be unlocked
5. Improve the accuracy of checkout button detection across retail sites
We do not use your data for advertising, profiling, or sale to third parties.
 
---
 
## Who we share your data with
 
| Party | What is shared | Why |
|---|---|---|
| **Supabase** | Email address, purchase records, auth tokens | Database and authentication infrastructure |
| **ExtensionPay** | Browser identity (anonymous until payment) | Payment status verification |
| **Stripe** | Email address, payment details | Processing subscription payments |
 
We do not sell, rent, or share your data with advertisers, data brokers, or any other third parties beyond those listed above.
 
**Supabase privacy policy:** https://supabase.com/privacy
**Stripe privacy policy:** https://stripe.com/privacy
**ExtensionPay privacy policy:** https://extensionpay.com/privacy
 
---
 
## Data retention
 
- **Local data** (chrome.storage): Retained until you clear it using the "Clear all data" button in the dashboard, or until you uninstall the extension.
- **Account data** (Supabase): Retained while your account is active. You can request deletion at any time by contacting us (see below).
- **Payment data** (Stripe/ExtensionPay): Retained per Stripe's standard data retention policies.
---
 
## Your rights
 
You have the right to:
 
- **Access** the data we hold about you
- **Delete** your account and all associated data
- **Opt out** of cloud sync by using the extension without signing in
- **Clear** your local purchase history at any time via the dashboard
To exercise any of these rights, contact us at the email address below.
 
---
 
## Children's privacy
 
This extension is not directed at children under the age of 13. We do not knowingly collect personal information from children.
 
---
 
## Changes to this policy
 
If we make material changes to this policy, we will update the "Last updated" date at the top of this page. Continued use of the extension after changes are posted constitutes acceptance of the updated policy.
 
---
 
## Contact
 
If you have questions about this privacy policy or your data, please contact us at:
 
**doineedthis.support@gmail.com**
 
