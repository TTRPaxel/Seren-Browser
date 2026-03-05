Seren Browser

A lightweight, privacy-focused web browser built with Python.

Seren is designed for users who value privacy, control, and transparency — without telemetry, data collection, or corporate search engines baked in. It integrates with self-hosted tools like SearxNG and Ollama to keep everything local and under your control.

⚠️ Seren is an experimental project and is actively evolving. Expect rough edges.


✨ Features
🔎 SearxNG Search
Uses a self-hostable, privacy-respecting metasearch engine instead of Google, Bing, or other traditional providers. Includes a custom new tab dashboard with a live clock and news feed pulled directly from your SearxNG instance.
🛡 Ad & Tracker Blocking
Blocks 60+ known ad networks and tracking domains by default, with a live blocked-request counter in the navbar. Also strips tracking parameters (UTM tags, fbclid, gclid, and 30+ others) from URLs before requests go out.
📋 Custom Block List
Add your own domains to block via the Settings page — no config file editing required.
🔒 WebRTC Leak Protection
Prevents WebRTC from exposing your real IP address, even when using a VPN. This is hardcoded on and cannot be disabled.
🎨 Canvas & WebGL Fingerprint Protection
Injects per-session noise into canvas pixel reads, WebGL renderer strings, and AudioContext data to prevent browser fingerprinting. Also spoofs hardware concurrency and device memory.
🌐 DNS-over-HTTPS (DoH)
Encrypts DNS queries to prevent ISP-level snooping. Choose from Cloudflare, Google, Quad9, AdGuard, or NextDNS in Settings.
⚙️ JavaScript Control
Toggle JavaScript on or off globally from the Settings page, similar to Firefox's enhanced tracking protection.
🤖 AI Assistant (Optional)
A sidebar AI assistant powered by a locally hosted Ollama instance. Supports model selection, conversation history, and injecting the current page as context. Completely optional — if you're not running Ollama, just ignore it.
🧩 Extensions Support
Load unpacked Chromium extensions (like uBlock Origin MV3) from a local folder via the Extensions manager.

⚙️ Configuration
Settings are accessible via the ⚙ button in the navbar or Ctrl+,. They're saved to ~/.seren_settings.json.
SearxNG URL — default is http://localhost:5000. If you're using a shared or remote instance, update this in Settings.

The public instance at 25.32.56.63:5000 can be used if you aren't self-hosting. If you are self-hosting, replace it with your own address.

News Feed — the home page fetches news from your SearxNG instance automatically. If it shows a 403 error, add the following to your SearxNG settings.yml and restart:
yamlserver:
  limiter: false
search:
  formats:
    - html
    - json
    - rss
Ollama (AI Assistant) — only relevant if you're running a local Ollama instance at http://localhost:11434. If you're not, you can safely ignore all AI-related settings.

⌨️ Keyboard Shortcuts
ShortcutActionCtrl+TNew tabCtrl+WClose tabCtrl+LFocus URL barCtrl+RReloadCtrl+,SettingsCtrl+\Toggle AI sidebarAlt+←BackAlt+→Forward

🔒 Privacy Philosophy
Seren aims to:

Minimize external data exposure by default
Avoid forced telemetry entirely
Support self-hosted alternatives to mainstream services
Give users direct, visible control over what gets blocked

Privacy in Seren is configurable and transparent — not hidden behind marketing language.

⚠️ Disclaimer
Seren Browser is an independent project and is not affiliated with any browser vendor, search engine, or AI provider. It is still under active development. Use at your own discretion.

📜 License
Copyright © 2026 Paxel. All rights reserved.
This software is provided for personal and team use only.
You may:

Use the software for personal purposes
Modify it for personal or internal team use

You may not:

Resell this software
Redistribute it commercially
Re-upload it as your own project
Claim authorship
