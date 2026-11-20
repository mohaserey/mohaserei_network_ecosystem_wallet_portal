# mohaserei_network_ecosystem_wallet_portal
Mohaserei System Network (MSN) — Wallet Portal

The Mohaserei Wallet Portal (mohaserei_network_ecosystem_wallet_portal) is a browser-based Layer 2 economic and contribution interface for the Mohaserei System Network (MSN). Built as a self-contained single-file HTML application (index.html), it enables members to manage MSN Coin, track Human Contribution Value (HCV), monitor Universal Economic Score (UES) telemetry, and inspect Layer 2 ledger settlements.

Key Features

Multi-Asset Portfolio & Settlement View:

Displays live balances for MSN Coin (MSN), Human Contribution Value (HCV), and the combined UES Settlement Pool.

Supports switching display settlements between USD and KHR (៛).

Interactive Wallet Actions:

Send / Transfer: Transfer MSN or HCV to a recipient MSN ID or handle with a 0.1% network fee preview, MAX balance helper, and memo support.

Receive / QR: Displays the active MSN wallet address (MSN-KH-8841-902A), one-click copy support, and a deterministically generated SVG matrix QR code.

Swap / Convert: Calculates protocol conversions between MSN, HCV, and UES settlement units and updates balances and ledger history.

Stake / Yield: Stakes MSN into regional Mohaserei yield pools and records bonus HCV rewards.

UES & HCV Economic Telemetry:

Tracks the member's Universal Economic Score (UES) progress bar, tier label, HCV earning multiplier, and profit-sharing cycle rate.

Includes a contribution simulator button (Record Verified Contribution) that updates HCV balance, UES score, and HCV multiplier while logging a new ledger entry.

Filterable Ledger & Receipt Modal:

Filter activity by All, Transfers, Rewards / HCV, or Marketplace.

Click any ledger row to open a detailed receipt modal (Mohaserei Ledger Receipt), or click + Demo Settlement to test marketplace settlement updates.

Bilingual UI (EN / ភាសាខ្មែរ) & Voice Summary:

Switch labels between English (EN) and Khmer (ភាសាខ្មែរ) using Kantumruy Pro and Inter typography.

Uses the browser's Web Speech API (speechSynthesis) to read out a spoken balance and UES summary in the selected language.

Local Persistence & Architecture

Single-File Delivery: index.html bundles layout styling (Tailwind CSS via CDN plus custom holographic glassmorphism styles), SVG rendering, translations, state management, and event handlers in one file.

Client-Side State: Balances, staking totals, UES telemetry, active panel/filter preferences, and transaction history are persisted in localStorage under mohaserei_wallet_portal_state_v1.

Running Locally

Because index.html is a standalone static page, you can open it directly in a modern browser or serve it over a local static server:

# Example using Python HTTP server from the repository root
python3 -m http.server 8080


Then navigate to http://localhost:8080/mohaserei_network_ecosystem_wallet_portal/index.html.

Integration Notes for the Mohaserei Ecosystem

Keep the exact spelling Mohaserei across all Mohaserei modules, documentation, and datasets.

When wiring this portal to live Mohaserei backend services, replace the localStorage state layer (loadState / saveState) and simulated action handlers with authenticated MSN Layer 2 API endpoints and verified regional member IDs.
