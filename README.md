# 🧠 AB Browser Agent (n8n + Claude + Airtop)

This project builds a browser automation workflow using **n8n**, designed to simulate a basic AI agent that can receive a prompt and act on it inside a browser — typing, clicking, loading pages — and updating via Slack.

It uses:

- 🧠 **Claude 3.5 Sonnet** via OpenRouter (for generating AI-driven instructions)
- 🌐 **Airtop** (for browser session control: start, type, click, end)
- 📩 **Slack integration** (to share a live view link of the agent working)
- 🧠 **n8n's native memory and agent nodes** to hold context and toolchains

---

## 🔧 What It Does

- Starts a remote browser session using Airtop
- Uses Claude AI to interpret the input prompt
- AI chooses what to load, type, or click
- Live session link is sent to Slack
- Ends session after completing the task

The workflow is modular and separated into agent thinking, browser tools, and communication.

---

## 📁 Files

- `AB_Browser_Agent.json`: full n8n workflow (**with credentials removed for safe sharing**)
- `screenshot.png`: visual layout of the system (optional)
- `README.md`: this file

---

## ⚠️ Credentials & Environment Variables

This workflow requires the following credentials **to be set manually in n8n**:

- `Airtop API`
- `OpenRouter API`
- `Slack OAuth2 API`

👉 **Note:** Credentials have been removed from the exported workflow JSON for security.  
You can either:
- Set them manually in the n8n Credentials section, or
- Use environment variables like `{{$env.OPENROUTER_API_KEY}}` if you're self-hosting

---

## 📸 Workflow Screenshot

> ![AB Browser Agent](./screenshot.png)

---

## 🙏 Credits

The structure and idea were inspired by **Nate Herk** on YouTube and his AI Browser Agent demonstrations.  
This version was built independently by observing his tutorials and adapting the logic into a working n8n system.

---

## 📌 Notes

- This setup uses **paid services**: Airtop and OpenRouter (Claude).
- While the visual flow is complete and executable, **Airtop restricts usage without a paid account**, and no generous free tier is currently available.
- This repo is shared for educational and experimental purposes only.

---

## ✍️ Author

Anil Bhargava  
[LinkedIn](https://www.linkedin.com/in/anilbhargava1331)
