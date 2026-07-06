# 🔍 Secret Sweep
## JS disclosure scanner

**Secret Sweep** is a client-side static analysis tool built entirely in vanilla HTML, CSS, and JavaScript. It allows security analysts, developers, and CTF players to scan JavaScript source bundles, chunks, or configuration files for exposed secrets, API keys, and hardcoded cryptographic configurations before deeper inspection.

## 🚀 Key Features

* **Pattern Matching:** Detects specific signature formats for popular services (AWS, Google OAuth, Slack, Stripe, Twilio, Firebase, etc.).
* **Entropy Analysis:** Uses a implementation of **Shannon Entropy** to dynamically flag randomized, high-entropy string literals that might be undocumented passwords, hashes, or encryption keys.
* **Crypto Signal Maps:** Identifies references to underlying algorithms, cryptographic libraries (`CryptoJS`, `Web Crypto API`, `JSEncrypt`), and targets weak hashes (like `MD5` or `SHA1`).
* **100% Client-Side Privacy:** Everything handles locally via the browser's `FileReader` API. No server-side storage, no tracking, no data leakage.

## 🛠 Usage

1. Open the live link or download the `index.html` file locally.
2. Paste raw JavaScript code into the prompt or drag-and-drop `.js`, `.map`, or `.json` files directly into the window interface.
3. Click **Scan for secrets** to review classified indicators by severity levels (`Critical`, `High`, `Medium`, `Info`).
