# Flexura

An AI coding agent for macOS with a **Canvas**. Next to the chat, the agent builds real, working panels (test benches, viewers, dashboards, small tools) and then uses them itself to check its work.

Made for developers building AI products: compare prompts and models side by side, replay an agent's run step by step, see what your retrieval returned, throw odd inputs at a feature, and keep a set of test cases you re-run after every change.

**[Download for Mac (Apple Silicon)](https://github.com/raunak711/flexura/releases/latest/download/Flexura-latest-arm64.dmg)** · [flexura.site](https://flexura.site)

## Install

1. Download `Flexura-latest-arm64.dmg`, open it, and drag **Flexura** into **Applications**.
2. Flexura is not notarized by Apple yet, so macOS will say it can't be opened. Run this once in Terminal to tell macOS you trust it:
   ```
   xattr -cr /Applications/Flexura.app
   ```
3. Open Flexura, go to **Settings → Accounts**, and connect **OpenAI Codex** (your ChatGPT plan) or **Google Gemini**.
4. In **Settings → Model**, choose a model. Flexura does not pick one for you.
5. In **Settings → Workspace**, choose your project folder.

## First things to try

- "Read this project and draw its architecture on the canvas."
- "Build a panel that sends the same question to my app with two different system prompts and shows the answers side by side."
- "Make 10 test questions for my RAG endpoint, run them in a panel, and show which ones fail."
- "Fix the failures, then re-run the panel until all 10 pass."
- "Open my app in the browser and check that signup works."

## What it does

- **Codes:** reads and edits your project, runs commands in a sandbox, and checks its own changes.
- **Builds on the Canvas:** panels it can click and read, so it tests what it built. Useful ones go in its toolbox for next time.
- **Uses a browser:** drives its own Chrome to try your app like a user.

## Known limits

- macOS on Apple Silicon only. Windows is coming.
- Not notarized yet (step 2 above).
- Panels on the canvas can open files and run commands on your Mac. Use Flexura on your own projects, and be careful letting it browse untrusted sites in the same chat where it builds panels.

## Feedback

Bugs, ideas, questions: [raunakkumar@flexura.site](mailto:raunakkumar@flexura.site) or [open an issue](https://github.com/raunak711/flexura/issues).
