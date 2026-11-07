# Hireko AI Recruiter — Cursor Plugin

Official Cursor plugin for **Hireko AI Recruiter**: candidate interview analytics, automated AI interview link generation, candidate match scorecards, and multi-tenant talent search.

---

## Capabilities

- 📊 **Candidate Pipeline & Analytics**: Fetch candidate counts, status breakdowns (completed vs. pending), and interview outcomes directly within Cursor chat.
- 🔗 **AI Interview Generation**: Create personalized interview links for candidates across all supported job funnels.
- 🎯 **Candidate Search & Scoring**: Retrieve semantic match scores and evaluation details for candidates evaluated by Hireko AI.
- 🔐 **Zero-Config Multi-Tenant Auth**: Direct local auth proxy (`bundle.mjs`) with seamless browser login. Recruiters simply enter their tenant credentials securely.

---

## Installation in Cursor

### 1. From the Cursor Marketplace (Recommended)
Open Cursor **Settings > Plugins** (or Customize), search for **Hireko AI Recruiter**, and click **"Install"**.

### 2. Direct Install in Cursor Chat
In Cursor Chat, type:
```text
/add-plugin jishnusaireddy/hireko-cursor-plugin
```

### 3. Manual Local Installation (Offline)
Copy this repository into:
- Windows: `%USERPROFILE%\.cursor\plugins\local\hireko-cursor-plugin\`
- Mac / Linux: `~/.cursor/plugins/local/hireko-cursor-plugin/`
Then restart Cursor.

---

## Starter Prompts

Once installed, try asking Cursor:
- *"Show candidate interview counts and pass rates for my team"*
- *"Create a candidate interview link for Senior Backend Engineer"*
- *"Search candidates for Java Spring Boot and Microservices"*

---

## Engine & Architecture
- **Engine**: Local Stdio MCP Router (`node ${CURSOR_PLUGIN_ROOT}/bundle.mjs serve`)
- **Downstream Tools**: 10 Recruiter Facade business tools
- **Authentication**: Multi-tenant AWS Cognito via browser device flow
