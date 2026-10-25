# Raam Group Customer Portal — Phase 1 UI demo

A no-build, dependency-free HTML/CSS/JavaScript frontend prototype. It includes eight views (dashboard + seven modules), a demo authentication/onboarding journey, multi-vehicle switching, AMC and booking walkthroughs, rule-based illustrative chat, referral and support placeholders, and responsive navigation.

## Start locally

**Option A:** Double-click `index.html` to open it in your browser. All core UI demos run locally.

**Option B (recommended):** Run from inside this folder:

```bash
python -m http.server 8000
```

Open http://localhost:8000 in your browser. Python 3 required only for Option B.

## Preview login

- Enter any valid email address (e.g. `demo@example.com`) or a 10–15 digit mobile number.
- Enter any password of 8 or more characters. This is **not real authentication**.
- For sign-up, use the clearly displayed example email code `123456`. No email is actually sent.
- Demo sign-up asks for a 10+ character complex password. It validates the format in the browser but **does not store the password**.
- PAN is optional and neither stored nor transmitted.
- User name and email can persist in browser `sessionStorage` during this browser tab session; do not enter real private information.
- Example vehicles are fictional, and workshop and benefits data are placeholders.

## Features

- Responsive sidebar / mobile navigation and profile menu
- Login, registration, email-code UI, password setup, password-reset UI, profile onboarding
- Welcome dashboard, linked example vehicles, booking/AMC summaries, navigation shortcuts
- Vehicle details and benefit eligibility placeholder views with multi-vehicle switching
- AMC Basic and Plus comparison, review, payment-unavailable screen, explicitly demo-only completion
- Vehicle ownership and service chronology, configurable stage UI examples
- Private in-page Advisor UI and educational sample feed
- 6-step service booking wizard with marked illustrative outlet/services/slots and no real booking or payment
- Referral wallet, example sharing, rewards placeholder
- Support hub, AI demo chat, voice integration explainer, human escalation UI placeholder
- Empty states, form validation, error notifications, responsive layouts

## Important limitations

This is a **frontend-only demonstration**. Real email verification, login, passwords, user authorisation, personal data storage, purchase/renewal, live service stages, advisor messaging, payment, service booking, referral rewards and voice/AI assistance require backends/integrations. The demo intentionally avoids implying real transactions succeeded. Do not deploy as a secure customer portal or use real PAN or customer information.

### Integrations to add for production

1. Identity platform with server-side sessions, secure account recovery, throttling and real verified OTP email.
2. Customer, vehicle and entitlement database with ownership checks and protected PAN fields if genuinely required.
3. Dealer/workshop management systems for purchase entitlements, service records and live vehicle progress.
4. Outlet / service catalogues, schedule and capacity API, booking locks and confirmed reservation IDs.
5. Official AMC plans, terms, eligibility rules, contract lifecycle and renewals.
6. Payment gateway with server-side webhooks, signature verification, reconciliation, refunds, and no card handling by the frontend.
7. Referral rewards and immutable points ledger.
8. Published content management, support ticketing, authenticated AI retrieval, speech services and human transfer.
9. Accessibility, privacy, security and payment-flow testing before launch.

## Brand reference

The palette approximates the supplied Raam Group EPIC casebook: deep maroon `#300B10`, secondary maroon `#46151C`, dark ink `#241C1E`, accent red `#C8101E`, and white `#FFFFFF`. The extracted sample colours remain provisional until exact brand hex values/fonts are provided. No external image assets are required. DM Sans and Manrope are retrieved from Google Fonts when internet is available, with local system-font fallbacks.

## Project structure

- `index.html` — entry point
- `styles.css` — responsive design system
- `app.js` — frontend state, rendering and demo interactions
