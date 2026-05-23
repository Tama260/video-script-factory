# 🎬 Video Script Factory

> AI-powered video production system that transforms any topic into a complete, production-ready video package — script, storyboard, voiceover, and platform-optimized content — in under 60 seconds.

**Live Generator:** [tama260.github.io/video-script-factory/generator.html](https://tama260.github.io/video-script-factory/generator.html)

**Sample Production:** [tama260.github.io/video-script-factory](https://tama260.github.io/video-script-factory)

---

## What This System Does

Input one topic. Get a complete video production package in under 60 seconds:

- Full scene-by-scene script with voiceover text
- AI-generated storyboard images for each scene
- Platform-optimized descriptions and tags
- Hook, CTA, and viral elements checklist
- Published automatically to GitHub Pages with a public URL

---

## Supported Formats

| Format | Duration | Scenes |
|---|---|---|
| YouTube Short | 60 seconds | 6 scenes |
| TikTok | 30-60 seconds | 5 scenes |
| Instagram Reel | 30 seconds | 4 scenes |
| LinkedIn Video | 2-3 minutes | 8 scenes |
| YouTube Long Form | 8-10 minutes | 15 scenes |

---

## System Architecture

[HTTP Trigger / Web Form Input]
↓
[parse_request] — extract topic, format, audience, tone
↓
[generate_master_script] — Groq AI generates full production script
↓
[generate_storyboard_images] — Pollinations.ai generates scene visuals
↓
[build_html_dashboard] — assembles complete production package as HTML
↓
[publish_to_github_pages] — pushes to GitHub Pages via API
↓
[notify_telegram] — sends notification with preview image + public URL

---

## Tech Stack

| Category | Tools |
|---|---|
| Workflow Automation | Pipedream |
| AI Script Generation | Groq AI (LLaMA 3.3 70B) |
| Image Generation | Pollinations.ai |
| Frontend | Vanilla HTML/CSS/JS |
| Deployment | GitHub Pages, GitHub API |
| Notification | Telegram Bot API |

**Cost: $0/month** — 100% free tier infrastructure

---

## Key Features

- **One-click generation** via web form interface
- **AI storyboard** with matching visuals per scene
- **Multi-format support** — YouTube, TikTok, Instagram, LinkedIn
- **Public URL** for every production package
- **Hook optimization** — first 3 seconds crafted for maximum retention
- **Viral elements checklist** — built into every package

---

## Sample Output

**Topic:** The Future of AI Agents
**Format:** YouTube Short (60s)
**Scenes:** 6
**Words:** 180

**Hook:** Imagine waking up tomorrow and AI handles your entire workday

**Scene 1 (3s):** [Visual: Futuristic cityscape at dawn]
Voiceover: Imagine a world where AI does all the work

**Scene 2 (10s):** [Visual: Human and robot working side by side]
Voiceover: Welcome to the world of AI agents — machines that think, learn, and act on their own

**CTA:** Subscribe for weekly AI insights that keep you ahead of the curve

---

## How to Use

### Option 1 — Web Form
Visit the live generator, fill in your topic and format, click Generate.

### Option 2 — Direct API

GET https://[pipedream-webhook-url]?topic=Your+Topic&format=youtube_short&audience=tech+professionals

### Option 3 — Custom Parameters
```json
{
  "topic": "How to Build an AI Chatbot",
  "format": "tiktok",
  "audience": "beginners",
  "tone": "casual_fun",
  "language": "english"
}
```

---

## Environment Variables

GROQ_API_KEY                = gsk_xxxx
TELEGRAM_BOT_TOKEN          = xxxx:xxxx
TELEGRAM_CHAT_ID            = -100xxxxxxx
GITHUB_TOKEN                = ghp_xxxx
GITHUB_USERNAME             = Tama260

---

## Project Structure

- Pipedream Workflow (HTTP Trigger, on-demand)
- parse_request
- generate_master_script
- generate_storyboard_images
- build_html_dashboard
- publish_to_github_pages
- notify_telegram
- docs/ — production packages (auto-generated)
- docs/generator.html — web form interface
- docs/index.html — productions index

---

## Author

**Daffa Novendra Aditama**
AI Automation Engineer | Banten, Indonesia

[![LinkedIn](https://img.shields.io/badge/LinkedIn-daffanovendraaditama-blue)](https://linkedin.com/in/daffanovendraaditama)
[![GitHub](https://img.shields.io/badge/GitHub-Tama260-black)](https://github.com/Tama260)

---

*Built with Groq AI · Pipedream · Pollinations.ai · GitHub Pages*
