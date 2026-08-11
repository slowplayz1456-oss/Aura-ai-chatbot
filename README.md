# Aura AI Chat

A sleek, voice-enabled AI chat interface with support for text, image, and code generation, live weather, and multilingual voice commands — built as a single, self-contained HTML file.

**Created by:** Mr. Dhyan Panchal
**Domain:** [Aura-ai-chatbot.com](https://aura-ai-chatbot.com)
**© 2026**

---

## Features

- 💬 Chat with **Claude (Anthropic)** or **Gemini (Google)** — switch providers anytime
- 🎙️ Voice input (speech-to-text) and voice replies (text-to-speech), with 5+ selectable voice personalities
- 🌍 Multilingual voice support: English, Hindi (हिंदी), Gujarati (ગુજરાતી)
- 🌦️ Live local weather pill (auto GPS or manual location)
- 🖼️ AI image generation (via Gemini) — falls back to a local generative-art placeholder if no key is set
- 💻 Code generation with syntax-highlighted, runnable snippets
- 🌐 Live web search toggle for news, scores, and current events
- 🧠 **Companion mode** — an always-on assistant persona you can put to sleep/wake with voice commands ("Aura, go to sleep" / "Aura, wake up," and Hindi/Gujarati equivalents)
- 🗣️ Voice shortcuts to open common web apps (e.g., "Aura, open WhatsApp")
- 🌓 Light/dark theme toggle
- 🔍 Built-in "System check" panel to confirm your setup is working
- 📱 Fully responsive — works on desktop, iPhone, iPad, and Android

No backend server is required — it's a single HTML file that talks directly to the Claude/Gemini APIs from your browser.

---

## Installation

Aura AI Chat needs no build tools, servers, or dependencies. Choose whichever method fits you:

### Option 1 — Just open it locally
1. Download `aura-ai-chatbot.html`.
2. Double-click it (or right-click → Open With → your browser).
3. That's it — it runs entirely client-side.

> Note: some browsers restrict microphone/location access on files opened via `file://`. For full functionality (voice input, weather), use Option 2 or 3 instead.

### Option 2 — Run a local dev server
```bash
# Python 3
python3 -m http.server 8000

# then open:
http://localhost:8000/aura-ai-chatbot.html
```

### Option 3 — Deploy it live (recommended)
Upload the single HTML file to any static host:

- **Netlify** / **Vercel** / **Cloudflare Pages** — drag-and-drop the file, get a live HTTPS URL in seconds, free tier
- **GitHub Pages** — push it to a repo and enable Pages in settings

To use your own domain (e.g. `aura-ai-chatbot.com`):
1. Buy the domain from any registrar (Namecheap, Cloudflare, GoDaddy, etc.)
2. Add it as a **custom domain** in your host's dashboard
3. Point your registrar's DNS/nameservers at the host as instructed
4. HTTPS is issued automatically by most hosts (Netlify, Vercel, Cloudflare Pages)

---

## How to Use Aura AI

### 1. Add an API key (for real AI responses)
Without a key, Aura runs in **demo mode** with canned replies. To get real, generated responses:

1. Click the **API settings** button in the sidebar.
2. Choose a **Provider**: Anthropic (Claude) or Google (Gemini).
3. Pick a **model** (e.g. Claude Sonnet 5, Claude Opus 4.8, Gemini 2.5 Pro).
4. Paste your API key.

Your key is stored **only in your browser** (`localStorage`) and sent directly from your browser to the provider's API — it never touches any other server.

> **Image generation** always uses a Gemini key, even if your chat provider is set to Claude, since Claude's API can't generate images. Without a Gemini key, "Generate an image" falls back to a local abstract-art placeholder so you can still try the feature.

Get API keys here:
- Anthropic (Claude): [console.anthropic.com](https://console.anthropic.com)
- Google (Gemini): [aistudio.google.com](https://aistudio.google.com)

### 2. Start chatting
- Type a message in the input bar and press **Enter** or tap Send.
- Tap one of the **suggestion cards** on the home screen for quick prompts (e.g., "Explain quantum computing," "Write a short poem").
- Use the **+ menu** next to the input bar to toggle **Web search**, or trigger **Generate an image** / **Generate code**.

### 3. Use voice
- Tap the **mic icon** or press **Ctrl+M** to start speaking.
  - On Chrome/Edge (desktop & Android): live transcription as you speak.
  - On iPhone/iPad/Safari (no native speech recognition support): Aura records your voice and transcribes it via Gemini — requires a Gemini API key.
- Go to **Voice settings** to:
  - Choose your voice language (English / Hindi / Gujarati)
  - Pick a voice personality (Aria, Sol, Nova, Pixel, Glitch, Aura)
  - Adjust rate, pitch, and volume
  - Set your location for local weather (auto GPS or type a city manually)

### 4. Companion mode
Companion mode is **on by default** — Aura acts as an always-available companion persona.
- Say **"Aura, go to sleep"** (or Hindi/Gujarati equivalents) to power it down.
- Say **"Aura, wake up"** to bring it back.
- Say **"Aura, open WhatsApp"** (or other common web apps) to launch them in a new tab.
- Toggle Companion mode on/off anytime in Voice settings.

### 5. Check your setup
Open **System check** from the sidebar to verify your API key, microphone, and location permissions are working correctly.

### 6. Switch themes
Use the **theme toggle** in the sidebar footer to switch between light and dark mode.

---

## Privacy

- API keys and settings are stored locally in your browser only.
- Chat requests go directly from your browser to Anthropic's or Google's API — no intermediary server sees your conversations.
- Location (for weather) is only used if you enable it, and can be set manually instead of via GPS.

---

## Credits

Aura AI Chat was designed and built by **Mr. Dhyan Panchal**.
