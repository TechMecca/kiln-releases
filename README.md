# Kiln

**Build with AI, on your own PC, together.**

Kiln is a free Windows desktop app for chatting and coding with AI. Use free local models that run on your own
graphics card, or sign in with the Claude, ChatGPT or Gemini plan you already pay for. Kiln works on your real
project folders, checks and fixes its own code, and lets your friends join the same chat with their own AI.

**[⬇ Download the latest version](https://github.com/TechMecca/kiln-releases/releases/latest)** — run
`Kiln-Setup-<version>.exe`. Windows 10/11 (64-bit). No admin rights needed. Kiln updates itself.

---

## What makes Kiln different

- **Bring your own AI.** Free local models (through [Ollama](https://ollama.com)), or your existing Claude, ChatGPT
  or Gemini subscription. No API keys, no pay-per-use, no Kiln account.
- **Build together in one chat.** Invite friends into a session. Each person's prompts run on their own AI and their
  own plan, so nobody uses up anyone else's usage, and everyone sees everything.
- **It checks its own work.** After the AI changes files, Kiln checks that the code compiles and your tests pass, and
  sends the errors back to the AI to fix.
- **Nothing is lost.** Every message in a coding session is a checkpoint. Rewind the files, the conversation, or both.
- **Your code stays on your PC.** With local models, your files and chats never leave your machine.

---

## Features

### 🤝 Shared sessions: collaborate with friends
- Right-click a chat or coding session → **Invite friends…** → **Start sharing**. Send the invite key to your team.
- Friends click **Join a shared session** and paste the key. Everyone sees the conversation live.
- **Everyone brings their own AI.** Your messages are answered by your model, on your PC or your plan. Theirs are
  answered by theirs. Your Claude, a friend's ChatGPT and another friend's local model can all work in the same thread.
- Every AI sees the whole conversation, labelled with who wrote what, so they build on each other's answers.
- **The host stays in control.** Code from guests is never written to the host's project automatically: the host
  clicks **Review as changes** and approves each change. Commands suggested by a guest's AI always ask first.
- Secure link through Cloudflare, protected by the invite key. Stop sharing at any time.

### 💬 Chat
- Chat with any model: local Ollama models, Claude, ChatGPT, Gemini.
- Streaming replies, collapsible reasoning for thinking models, speed and token stats, stop, retry, regenerate.
- **Effort control** (Faster ↔ Smarter) that maps to each provider's own reasoning setting.
- Drag and drop, paste or attach files. Images go to vision models.
- Paste a link and Kiln reads it for you: web pages, PDFs, and YouTube videos (with their transcript).
- Searchable history with rename, pin, archive and delete.
- **Slash commands** in every message box: `/model`, `/module`, `/effort`, `/mode`, `/compact`, `/new` and more.

### 🌐 Internet research, always on
- The AI looks things up when it needs to: unfamiliar libraries, version-specific behaviour, error messages.
- Models that can't use tools get help too: Kiln searches the error or question for them and adds what it finds.
- **Only search words leave your PC.** Every search is cleaned of file paths, code, URLs, e-mail addresses and keys.
- Each reply shows what was searched and which pages were read.

### 🧑‍💻 Code workspace
- Open any folder, or start a session with its own clean scratch folder.
- File explorer with git status, a VS Code–style editor (Monaco) with tabs, project-wide search, and a built-in terminal.
- The AI understands your project: it gets the open file, the files it imports, files you attach and files named in
  your request.
- **Smart file search:** with a small embedding model installed, Kiln finds the files that match what you mean, even
  when no file name matches.
- Watch files being written live as the AI works, with a panel per file.
- **Preview site:** web projects open in Kiln's built-in browser and reload when files change.
- Right-click code → *Explain*, *Find bugs*, *Refactor* or *Improve*.
- Project instructions: Kiln reads `KILN.md`, `AGENTS.md` or `CLAUDE.md` from your project, like Claude Code does.

### 🛡️ You decide how much the AI does
- **Permission modes:**
  - **Auto** (default): edits are written right away, with backups and Undo.
  - **Manual:** every change waits for your review.
  - **Accept edits:** edits are written; tools follow your settings.
  - **Plan:** the AI reads and plans, but changes nothing.
  - **Bypass:** nothing asks.
- Full-size diff review with Apply, Reject, Apply all and Revert.
- If a file changed after the AI read it, Kiln flags a conflict instead of overwriting it.
- Commands always show the exact command first. "Always allow" works for simple commands, never for chained ones.

### 🔁 Self-checking debug loop
- After every change, Kiln checks that the files compile (Python, JavaScript, JSON, PowerShell, Go, Lua) and runs
  your tests or build command.
- If something fails, the AI gets the error and fixes it. Choose 1–10 tries, or **Until fixed**.
- Each reply shows *Compiles*, *Checks passed* or *Crashed* at a glance.
- The AI can start a dev server, read its output, open your local pages and read console errors, like a real developer.
- Missing Python or Node.js? Kiln offers to install it.

### ⏪ Rewind
- Kiln snapshots the project's files before every message in a coding session.
- Click **Rewind** on any message, see exactly what will change, and choose *Files and conversation*, *Files only* or
  *Conversation only*.
- Changed your mind? **Undo** puts everything back.

### 🧩 AI Modules
- Named assistants with their own instructions, model, effort and permissions. For example, a big model as
  *Architect* and a small fast model for *Quick edits*.
- Every module in a conversation sees the whole conversation, including what other modules wrote.
- Create, duplicate, test, import and export modules.

### ⚡ One-click local AI setup
- **Discover** scans your PC (graphics card, memory, processor) and recommends models that fit.
- One click installs Ollama if needed, downloads the model, and sets it up, ready to use.
- **Per-model tuning:** Kiln learns how each model edits files best. A built-in benchmark tests it on real coding tasks.

### 🎮 GPU memory, handled
- Before a model loads, Kiln unloads others that wouldn't fit beside it.
- A **GPU meter** in the sidebar shows memory in use and the loaded models, with Unload buttons.
- Kiln frees GPU memory when you close the window, and finds stuck model processes left behind by a crash.

### 🔐 Your AI accounts
- Sign in to **Claude** (Pro/Max), **ChatGPT** (Plus/Pro/Team) or **Gemini** (any Google account) with each company's own official sign-in.
  Kiln never sees your password.
- Usage counts against your plan, never against pay-per-use API billing.
- Kiln shows your Claude and ChatGPT plan limits, and what was sent through Kiln.

### 🔌 Works with your other tools
- **Share with other AIs:** Kiln can act as a local MCP server, so Claude Code, Codex or any MCP app on your PC can
  read a chat and post in it.
- Add **MCP tool servers** for extra tools. Every tool call asks unless you allow it.
- **GitHub:** start git, commit, push, and publish a project as a private repository in one click.
- Open any chat or session in VS Code, Explorer, Windows Terminal, or its own pop-out window.
- Works with **OpenCode**, and with an Ollama server on another computer on your network.

### 🪶 Built for long sessions
- Long conversations stay smooth: a 600-message session opens in about a tenth of a second.
- Kiln grows the context to fit the whole conversation. When a conversation outgrows it, the oldest messages are
  turned into notes instead of being dropped. `/compact` does that on demand.
- Click any reply's context meter to see exactly what the AI was given.
- Runs in the system tray, so replies and shared sessions keep going when you close the window.
- Dark, light or system theme.

---

## Requirements

- Windows 10 or 11, 64-bit.
- For local models: a graphics card helps a lot (NVIDIA recommended). Kiln's **Discover** tells you what fits your PC.
- For Claude or ChatGPT: a subscription to that service. Gemini works with any Google account.

## Privacy

- Your chats, settings and project files are stored on your PC.
- With local models, nothing you write leaves your machine.
- Internet research sends only search words, never your code.
- Chats with Claude, ChatGPT or Gemini go to that company, under your own account.
- Shared sessions send the conversation to the people you invite, and only while you are sharing.

## Updates

Kiln checks for updates on startup and every few hours, downloads them in the background, and shows
**Update ready — Restart** when one is ready. Every download is verified before it installs.

---

<sub>This repository holds Kiln's installers and update feed. The source code is private.</sub>
