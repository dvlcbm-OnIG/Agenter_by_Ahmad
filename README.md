# 🚀 Agenter Created by [Ahmad](https://github.com/zxcoding123).
### Your AI Coding Command Center

**Manage multiple Codex sessions from one dashboard. Code smarter, switch less, and keep every AI agent under control.**

Agenter is a desktop dashboard that brings your Claude Code and Codex sessions into one place. Instead of constantly switching between terminals and VS Code windows, you can monitor, communicate with, and manage your coding agents through a single interface.

> **Important:** Agenter does not generate code itself, increase Codex intelligence, or provide additional AI usage. Codex does the actual coding; Agenter makes managing multiple sessions easier.

---

## ✨ 1. What Can Agenter Do?

- **Unified Dashboard:** Monitor multiple Codex sessions in one window.
- **Live Monitoring:** See what each agent is doing and whether it is running, waiting, or finished.
- **Centralized Communication:** Send additional instructions to your agents.
- **Session Management:** Start and stop sessions from Agenter.
- **Command Approvals:** Review and respond to supported permission requests.
- **Usage Monitoring:** Check your Codex usage and available reset times.
- **Desktop Notifications:** Know when an agent needs your attention.

## ⚖️ 2. With Agenter vs. Without Agenter

You can achieve similar coding productivity without Agenter, but you will need to manage everything manually.

| Without Agenter | With Agenter |
|---|---|
| Switch between terminal windows | One unified dashboard |
| Check each session individually | Monitor all sessions together |
| Look for agents waiting for approval | Centralized approval inbox |
| Open the correct terminal to reply | Reply through the dashboard |
| Manually track agent progress | Centralized activity feed |
| Check usage separately | Usage overview and alerts |
| Manually organize sessions | Centralized session management |

**The difference:** Agenter reduces the time and attention spent managing your agents, allowing you to focus more on planning, reviewing, and developing your project.

It does not make Codex execute code faster or improve its generated code quality.

---

## 🛠️ 3. Setup Guide (Windows 11 + Codex Free)

### Requirements

- Windows 10/11
- Node.js 18 or newer
- npm
- A Codex-supported ChatGPT account
- Internet connection for installation and normal Codex authentication

### Step 1 — Check Node.js

Open PowerShell or your VS Code terminal.

```powershell
node -v
npm -v
```

If both commands display version numbers, you're ready.

### Step 2 — Install Codex (skip if already installed)

```powershell
npm install -g @openai/codex
```

Verify:

```powershell
codex --version
```

### Step 3 — Sign in to Codex Free

Run:

```powershell
codex
```

Choose **Sign in with ChatGPT** and authenticate using your Free account.

You can use Codex through its CLI, VS Code extension, or desktop app.

### Step 4 — Install Agenter

Open PowerShell:

```powershell
npm install -g agenter-app
```

Install it globally, not through `npx`.

### Step 5 — Open Agenter

```powershell
agenter
```

The dashboard should open in its own window.

**For Codex-only users, no additional Agenter installation or Codex configuration is required.** Your Codex sessions should appear automatically.

If you also want Claude Code integration, run:

```powershell
agenter install
```

Then reload your VS Code windows to activate the Claude hooks.

### Step 6 — Start using multiple sessions

Open separate terminals in your project directory and start Codex:

```powershell
codex
```

Give each session a different responsibility.

Example:

- Terminal 1 — Backend development
- Terminal 2 — Frontend development
- Terminal 3 — Database design
- Terminal 4 — Testing and code review

Open Agenter to monitor the sessions together.

---

## 📊 4. Understanding Codex Free Usage Limits

Agenter can display your Codex usage, including applicable usage periods and reset times.

**Remember:** Codex usage is not simply a fixed monthly token balance. Limits depend on your plan and may include different usage windows.

When you reach a limit:

1. Stop assigning new tasks temporarily.
2. Check your usage and reset information.
3. Wait for the applicable allowance to refresh.
4. Save your current progress using Git.
5. Resume your work when access becomes available.

### How to switch to another ChatGPT account

If you have another legitimate ChatGPT account with its own Codex access, you can sign out and authenticate with that account.

For Codex CLI:

**Step 1 — Sign out**

```powershell
codex logout
```

**Step 2 — Sign in again**

```powershell
codex login
```

**Step 3 — Authenticate using your other ChatGPT account.**

Make sure the browser authentication flow uses the intended account. Sign out of the previous browser session or choose the correct account when prompted.

**Step 4 — Verify your authentication**

```powershell
codex login status
```

Your Codex CLI and VS Code extension share cached login credentials, so signing out of one can affect the other.

For the Codex desktop app, use its account/profile menu to sign out and sign in with the intended account.

**Important:** Switching accounts does not transfer usage or reset limits on your original account. Each account follows its own eligibility and usage restrictions. Do not use account switching to circumvent applicable service restrictions.

---

## 🧠 5. How to Vibe Code Efficiently with Agenter

Having multiple agents does not automatically mean faster development. You need to organize their responsibilities.

### A. Plan before coding

Before starting multiple agents, understand your project requirements.

Define:
- What you are building.
- Technologies you will use.
- Database structure.
- Frontend and backend responsibilities.
- Expected results.

Ask your primary Codex session to analyze the project and propose an implementation plan before making changes.

### B. Assign specific responsibilities

Avoid giving every agent the same instructions.

Example: Barangay Management System

| Agent | Responsibility |
|---|---|
| Agent 1 | Backend and API |
| Agent 2 | Frontend and UI |
| Agent 3 | Database and relationships |
| Agent 4 | Testing and debugging |

Give each agent clear boundaries.

For example, the frontend agent should follow the agreed API contract instead of independently changing backend endpoints.

### C. Give agents context

Use a clear prompt:

"Your responsibility is the backend development of this project. Review the existing folder structure and database schema first. Do not modify frontend files. Follow the existing architecture and explain your implementation before making major changes."

Good instructions reduce conflicts and unnecessary modifications.

### D. Monitor through Agenter

Use the dashboard to:

1. Check which agents are running.
2. Identify agents waiting for your response.
3. Review command approval requests.
4. Answer questions and provide additional instructions.
5. Stop unnecessary or conflicting tasks.

### E. Review everything

Never assume that generated code is automatically correct.

After implementation:

- Run the application.
- Test the API endpoints.
- Check database operations.
- Inspect frontend behavior.
- Review changes before committing.

Use Git to protect your progress:

```powershell
git add .
git commit -m "Complete backend implementation"
```

---

## 💡 6. Recommended Multi-Agent Workflow

A practical workflow for beginners:

1. **Architect:** Ask Codex to analyze the project and create an implementation plan.
2. **Database:** Design and verify the database schema.
3. **Backend:** Implement the API based on the agreed schema.
4. **Frontend:** Develop the UI based on the agreed API contract.
5. **Tester:** Review integration, identify bugs, and run tests.
6. **You:** Review the final output and approve important changes.

### Golden Rules

- Never run multiple agents without assigning responsibilities.
- Avoid having agents edit the same files simultaneously.
- Give agents access only to the information and files they need.
- Use Git checkpoints before major changes.
- Ask Codex to explain unfamiliar code.
- Review changes before accepting them.
- Prioritize correctness over the number of agents.

---

## 🔗 7. Useful Resources

- [Agenter on npm](https://www.npmjs.com/package/agenter-app)
- [OpenAI Codex Documentation](https://developers.openai.com/codex/)
- [Codex CLI Documentation](https://developers.openai.com/codex/cli/)
- [Codex Usage and Plan Information](https://help.openai.com/en/articles/11369540-using-codex-with-your-chatgpt-plan)

---

### Final Thoughts

**Agenter is your command center. Codex is your workforce. You are the architect.**

The goal isn't to run as many AI agents as possible. It's to organize them effectively, minimize wasted usage, prevent conflicting changes, and deliver working software.

Start with two agents, understand how they collaborate, and gradually expand your workflow as your projects become more complex.
