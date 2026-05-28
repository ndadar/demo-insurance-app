# InsureCo Customer Portal - Demo App

An interactive, single-file customer dashboard mockup for **InsureCo**. This application serves as a high-fidelity demo environment built specifically to test digital adoption platforms, automated testing frameworks, and interactive walk-throughs.

---

## 🌐 Live Environment

You can access and interact with the deployed version of this demo app instantly here:
👉 **[Live Demo URL](https://effervescent-cajeta-47012e.netlify.app/)**

*Note: This environment runs entirely on the client-side, meaning any actions you take (like filling out forms or adding cards) will interact seamlessly in real-time but will reset back to default upon a page refresh.*

---

## 🚀 Key Features

- **My Policies View:** View active coverage plans, premium summaries, covered vehicles (Tesla Model 3, Toyota RAV4), and agent details.
- **Interactive Claims Center:** A functional multi-step insurance claim filing workflow (Incident Info ➔ Photo Upload ➔ Success Confirmation).
- **Billing Management:** Interactive dashboard featuring real-time state changes for Autopay toggling, simulated quick card additions, and step-by-step checkout modals.
- **Document Hub:** Categorized file viewer featuring instant client-side search functionality and mock downloads.
- **Embedded Support Agent Chat:** Simulated live-chat widget with automated smart replies based on user selections.

---

## 🍴 Customization & Forking

This portal was designed to be highly extensible. If you want to use it as a sandbox or build your own tailored feature variants, feel free to customize it:

1. Click the **Fork** button in the top right corner of this page to generate an isolated copy under your own GitHub account.
2. Clone your forked repository down to your computer.
3. Open `index.html` in your favorite IDE (like VS Code).
4. Locate the `const POLICY` or `const BILLING` JavaScript objects near the top of the script block to manipulate user names, vehicle types, or premium costs instantly.
5. Deploy your customized version back to Netlify or GitHub Pages as you see fit!

---

## 🛠️ Architecture & Tech Stack

To ensure effortless portability and rapid deployments, this application is completely **self-contained** in a single file (`index.html`). It works out-of-the-box using CDN dependencies—no development environment orchestration, server management, or `npm install` executions required.

- **Frontend Core:** React 18 (via Unpkg CDN)
- **Compilation Engine:** Babel Standalone (runs JSX directly inside the browser)
- **Styling Utility:** Tailwind CSS Play CDN
- **Data Persistence:** Mock states hardcoded client-side (runs smoothly over standard `file://` protocols)

---

## 🎯 Digital Adoption & Testing Optimization (Whatfix)

This application is structurally engineered with hardcoded semantic hooks to make targeting effortless for digital adoption layers (e.g., **Whatfix Smart Tips, Beacons, and Flows**) and automation layers (Cypress, Playwright, Selenium):

1. **Page Tagging:** The `<body>` element includes a `data-wf-page="dashboard"` selector to easily determine global application context.
2. **Section Structuring:** Core dashboard regions carry explicit tracking boundaries via descriptive wrappers (e.g., `data-wf-section="sidebar"`, `data-wf-section="claim-form"`).
3. **Explicit Interactive IDs:** Key actionable elements utilize persistent, readable element selectors instead of dynamic random classes:
   - `#download-pdf-btn` (Download Policy PDF trigger)
   - `#file-new-claim-btn` (Initial claim launcher)
   - `#autopay-toggle-btn` (Live Autopay switcher switch)
   - `#upload-document-btn` (Document vault uploader)
   - `#support-chat-toggle` (Chat assistance bubble)

---

## 💻 Local Quickstart

If you don't want to use the public live link and prefer working locally instead:

### Option 1: Double-Click (Simplest)
1. Clone or download this repository onto your workstation.
2. Double-click the `index.html` file to launch it directly inside any modern web browser.

### Option 2: Local Static Server
If you prefer running it inside a local development port (e.g., `http://localhost:3000`), navigate to your workspace directory inside your terminal and spin up a lightweight server:

```bash
# Using Python 3.x
python -m http.server 3000

# Using Node.js (npx)
npx serve .
