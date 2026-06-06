# 📑 Project Documentation: Office Pre-Order Hub

## 1. Project Context & Background
This application was developed to solve an operational bottleneck within a corporate sales team. The engineering goal was to create a development path that functions perfectly within a strictly locked-down enterprise laptop environment without requiring local software installations or administrative privileges.

### Current Manual Workflow (The Problem)
1. **Flash Announcements:** Multiple salespeople announce temporary flash or pre-order food campaigns (Poultry, Nuggets, Breaded Chicken, Burgers, Ready-to-Eat meals) via a central office WhatsApp (WA) group.
2. **Manual Ordering:** Colleagues reply with a long, unformatted text list of orders either in the group chat or via direct message.
3. **Manual Recaps:** The salesperson manually parses text messages and copies order aggregates into a local Excel spreadsheet.
4. **Manual Invoicing:** The salesperson calculates individual amounts due and texts payment requests manually alongside their personal bank/e-wallet routing information.
5. **Delivery Checklist:** Upon stock arrival, delivery verification and payment confirmations are manually crossed off on a paper or local Excel ledger.

---

## 2. Technical Blueprint & Architecture
The system design replaces manual tracking with an autonomous, web-native ecosystem built using an "Agent-First" development architecture via **OpenHands** and **GitHub Pages**.

Salesperson Device]      --> Creates Campaign & Configures Personal Bank Details

       |
       v
[Cloud App Context]       --> Generates Unique Tokenized Web URL Query (?campaign=ID)
       |
       v
[Shared Office WA Group] --> Drops Link -> [Employee Smartphone] -> Single-Click Submit
       |
       v
[Master Ledger UI]       --> Auto-Calculates Totals -> SheetJS Library -> Downloader (.xlsx)

### Functional Component Matrix
*   **Salesperson Profile Management:** Secure multi-login authorization mapping explicit user credentials, product inventories, and unique fallback banking instructions.
*   **Dynamic Campaign Engine:** Form scheduler supporting rapid flash window shortcuts (0.5 hr, 1 hr, 2 hr, 1 day) rendering live countdown boundary clocks to lock out tardy buyers.
*   **Login-Free Mobile Checkout:** Seamless consumer experience requiring zero corporate network validation. Buyers enter their name, select product tallies, and instantly view a customized digital invoice screen complete with a pre-formatted *Share to WhatsApp* confirmation script.
*   **Fulfillment Control Center:** Granular status state toggles (`Paid / Unpaid` and `Delivered / Pending`) mapping straight to a real-time data table wrapper.
*   **SheetJS Excel Core:** An offline data transformation pipeline utilizing an external CDN hook to package active memory registers into a natively downloaded `.xlsx` file wrapper.

---

## 3. Step-by-Step Implementation Ledger
The following operational ledger tracks the exact steps executed to bypass local enterprise locks and successfully deploy the platform globally:

### Phase A: Cloud Workspace Provisioning
1. Initialized **GitHub Cloud Codespaces** using a container template to secure an isolated Linux terminal completely inside a standard browser tab.
2. Leveraged **OpenHands Web Platform** connected securely to GitHub via OAuth token workflows.
3. Passed structural execution prompt parameters containing business definitions to the agentic AI layer.

### Phase B: Bypassing Headless Sandbox Limitations
*   *Observation:* The application compiled successfully on `localhost:8080` inside the isolated OpenHands server sandbox, but local network security boundaries meant it could not be previewed directly via typical client port mapping.
*   *Mitigation:* Instructed the OpenHands automated agent to move and isolate compilation deliverables out of the temporary headless memory sandbox and perform an upward cloud commit (`↑ Push`) into a dedicated repository branch: `office-preorder-hub-feature`.

### Phase C: Directory Tier Structural Realignment
*   *Observation:* The agent structured code outputs underneath a nested subfolder `/office-preorder-hub/index.html`. GitHub Pages expects the index entrypoint file to reside strictly at the top-level folder tier, resulting in a blank site rendering the fallback text file.
*   *Mitigation:* Launched the full-screen **GitHub Web Editor** via the browser window address bar (`.dev` extension mapping). Executed a directory file tier shift, moving `index.html` outwards to reside on an exact flat plane level parallel with `README.md`. Committed the workspace transformation directly to the primary compilation branch.

### Phase D: Enterprise-Safe Global Hosting
1. Toggled repository deployment permissions from **Private** to **Public** inside the GitHub General Danger Zone settings grid to activate free server hosting.
2. Adjusted GitHub Pages routing mechanisms, targeting the **`main`** deployment path tracking the realigned structural tier layout.
3. Cleared local machine browser cache engines via a forced structural server sweep (`Ctrl + F5` / Incognito window verification).

---

## 4. Current State & Immediate Next Steps

### Operational Status
The application is **100% stable, live, and functional** at the public access domain:  
👉 **`https://sutitt.github.io/openhandstrial/`**

### Active Architectural Limitation
The application currently runs on browser **`localStorage`**. Because local storage is strictly isolated to the browser instance that created it, any campaign initialized on the salesperson's computer profile will result in a `"Campaign Not Found"` validation error when opened on a completely separate coworker machine or mobile device terminal.

### The Next Migration Script
To upgrade this into an enterprise-wide shared ecosystem, pass the following precise structural prompt configuration back into your **OpenHands** or **Bolt.new** prompt thread to integrate a globally accessible cloud database:

```text
The localStorage setup functions perfectly within isolated single-session tests, but campaigns are restricted from cross-device synchronization, triggering 'Campaign Not Found' errors on third-party employee terminals. 

Please modify the data interaction tier of 'index.html' to sync with a free web-accessible data store or public JSON server API. Map the read/write logic for Salesperson Profiles, Active Campaigns, and Incoming Orders to this synchronized network layer so that campaigns created on any corporate workstation immediately propagate down to employee mobile device screens.
