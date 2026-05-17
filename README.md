# 🎬 AI-Powered Infographic Creator

<div align="center">

![License](https://img.shields.io/badge/License-MIT-green.svg)
![Platform](https://img.shields.io/badge/Platform-n8n-blue.svg)
![AI](https://img.shields.io/badge/AI-Gemini-purple.svg)

**Transform any YouTube video into a stunning infographic — automatically!**

[Features](#-features) • [How It Works](#-how-it-works) • [Tech Stack](#-tech-stack) • [Setup](#-setup) • [Usage](#-usage)

</div>

---

## 🚀 Overview

Say goodbye to manual summarization and boring presentations! This n8n workflow automatically converts any YouTube video into a professional, shareable infographic.

### ✨ Why This Project?

| Why | Benefit |
|-----|---------|
| **Zero Code** | Build entirely in n8n — no programming needed |
| **AI-Powered** | Gemini AI understands and summarizes content intelligently |
| **Super Fast** | From video URL to infographic in under 60 seconds |
| **Production-Ready** | Built-in error handling, validation, and monitoring |

---

## 🔥 Features

### 📥 Smart Input
- Accept any YouTube video URL
- Auto-validates URL format before processing

### 📜 Automatic Transcription
- Fetches video transcripts via Apify
- Supports multiple languages
- Handles long videos seamlessly

### 🧠 AI Summarization
- Gemini AI extracts key insights
- Creates structured, easy-to-read summaries
- Identifies main topics and takeaways

### 🎨 Infographic Generation
- Professional visual layouts
- Engaging design elements
- Clear information hierarchy

### ☁️ Cloud Hosting
- Instant upload to Cloudinary
- Public URL generation
- Share anywhere — social media, presentations, documents

---

## ⚙️ How It Works

```
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│   SUBMIT     │───▶│   EXTRACT     │───▶│   ANALYZE    │
│  YouTube URL │    │  Transcript   │    │   with AI    │
└──────────────┘    └──────────────┘    └──────────────┘
                                                  │
                                                  ▼
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│    SHARE     │◀───│   UPLOAD      │◀───│   GENERATE   │
│  Image URL   │    │  Cloudinary   │    │  Infographic │
└──────────────┘    └──────────────┘    └──────────────┘
```

### Step-by-Step Breakdown

**Step 1** — User submits a YouTube URL through the n8n form

**Step 2** — Apify extracts the full video transcript automatically

**Step 3** — Gemini AI analyzes the content and generates key insights

**Step 4** — Gemini creates a visually appealing infographic

**Step 5** — Image uploads to Cloudinary for instant hosting

**Step 6** — User receives a public URL to share anywhere

---

## 🛠 Tech Stack

<div align="center">

| Technology | Purpose | Badge |
|------------|---------|-------|
| **n8n** | Workflow automation | ![n8n](https://img.shields.io/badge/-n8n-000000?style=flat&logo=n8n) |
| **Google Gemini AI** | Content analysis & image generation | ![Gemini](https://img.shields.io/badge/-Gemini-8AB4F8?style=flat) |
| **Apify** | YouTube transcript extraction | ![Apify](https://img.shields.io/badge/-Apify-2D2D2D?style=flat) |
| **Cloudinary** | Image hosting & CDN | ![Cloudinary](https://img.shields.io/badge/-Cloudinary-3448C5?style=flat) |

</div>

---

## 📂 Project Structure

```
ai-infographic-creator/
├── workflow.json       → Complete n8n workflow definition
├── README.md           → This documentation
├── screenshots/        → Visual documentation
│   ├── workflow.png    → Workflow builder view
│   ├── form.png        → Input form interface
│   └── output.png      → Generated infographic
└── .gitignore          → Git ignore rules
```

---

## 🏁 Getting Started

### Prerequisites

Before you begin, make sure you have:

- [ ] An n8n instance (self-hosted or cloud)
- [ ] Google Gemini API key (with vision capabilities)
- [ ] Apify account with API token
- [ ] Cloudinary account with credentials

---

### Step 1: Import the Workflow

1. Open your **n8n instance**
2. Go to **Workflows** → **Import from File**
3. Select `workflow.json` from this repository
4. Click **Import**

### Step 2: Configure Credentials

In n8n, add these credentials:

| Credential | Where to Get It |
|-----------|-----------------|
| `gemini-api` | [Google AI Studio](https://aistudio.google.com/app/apikey) |
| `apify-api` | Apify Dashboard → Settings → API Tokens |
| `cloudinary` | Cloudinary Dashboard → Settings → API Keys |

### Step 3: Activate the Workflow

1. Toggle the workflow to **Active**
2. Access the form via the webhook URL
3. Start creating infographics!

---

## 📖 Usage Guide

### Quick Start

1. **Get the form URL** — Find your webhook URL in n8n
2. **Paste a YouTube link** — Any valid video URL works
3. **Hit submit** — Watch the magic happen
4. **Grab your link** — Get your shareable infographic URL

### Processing Time

- **Typical**: 30-60 seconds
- **Long videos**: Up to 2 minutes

---

## 🔧 API Setup Guide

### Google Gemini API

1. Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Create a new API key
3. Ensure **Gemini Vision** is enabled for image generation
4. Copy the key and add it to n8n credentials

### Apify

1. Create an account at [apify.com](https://apify.com)
2. Go to **Settings** → **API & Tokens**
3. Copy your **API token**
4. Add it to n8n credentials

### Cloudinary

1. Sign up at [cloudinary.com](https://cloudinary.com)
2. Open your **Dashboard** — note your **Cloud Name**
3. Go to **Settings** → **API Keys**
4. Copy your **API Key** and **API Secret**
5. Add all three to n8n credentials

---

## ⚠️ Error Handling

The workflow gracefully handles:

- ❌ Invalid YouTube URL format
- ❌ Videos without available transcripts
- ❌ API rate limits and timeouts
- ❌ Cloudinary upload failures
- ❌ Gemini API errors

Each error returns a clear, helpful message explaining what went wrong.

---

## 🎨 Customization

### Change Infographic Style

Edit the Gemini prompt in the workflow to adjust:

- **Color scheme** — Match your brand colors
- **Layout** — Different templates and structures
- **Fonts** — Custom typography options
- **Content density** — Compact or detailed layouts

### Extend Functionality

Add support for:

- 📻 Podcast RSS feeds
- 📄 Article URLs
- 📁 Local video files
- 🎙 Audio file transcription

---

## 🤝 Contributing

Found a bug? Have a feature request?

- 🐛 Open an issue
- 🔀 Submit a pull request
- 💡 Suggest new integrations

All contributions are welcome!

---

## 📜 License

**MIT License** — Free to use, modify, and distribute.

---

## 🙏 Acknowledgments

- **[n8n](https://n8n.io/)** — The incredible workflow automation platform
- **[Google Gemini](https://gemini.google.com/)** — Powerful AI content generation
- **[Apify](https://apify.com/)** — Robust web scraping and data extraction
- **[Cloudinary](https://cloudinary.com/)** — Excellent image hosting and CDN

---

## 💬 Support

Questions? Need help?

- 📋 Open a GitHub issue
- 💬 Check the n8n community forums
- 📖 Review the workflow JSON for node details

---

<div align="center">

**Made with ❤️ using n8n + AI**

*Star ⭐ this repo if you found it useful!*

</div>
