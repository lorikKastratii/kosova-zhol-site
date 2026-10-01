# kosova-zhol-site

Public marketing, privacy and support pages for the Kosova Zhol iOS app, served by GitHub Pages.

Kept separate from the game repo: App Review needs a privacy policy URL and a support URL that stay
reachable indefinitely, and that shouldn't require publishing the game's source.

## Pages

| Path         | Purpose          | Used in App Store Connect as |
| ------------ | ---------------- | ---------------------------- |
| `/`          | Landing page     | `marketingUrl` (optional)    |
| `/privacy/`  | Privacy policy   | `privacyPolicyUrl`           |
| `/support/`  | Support and FAQ  | `supportUrl`                 |

Each page is a directory containing `index.html`, so the trailing-slash URLs work without rewrite
rules. Do not rename these directories — the URLs are registered with Apple, and a 404 on the privacy
policy is grounds for removal after approval. The repo must stay public and Pages must stay on.

The site serves at `https://lorikkastratii.github.io/kosova-zhol-site/` from `main`, folder `/`.
`.nojekyll` makes GitHub serve the files as-is.

## Keeping it accurate

The privacy policy describes the real behaviour of the app and its game server, and must keep matching
the App Privacy answers in App Store Connect. Update it if any of these change:

- the game server's host (currently an ngrok tunnel to a developer machine, shared with Kosova Poker)
- adding an analytics, crash-reporting or advertising SDK (currently: none)
- storing anything beyond display name, chip balance, account id and token
- adding free-text chat, sign-in, or purchases
