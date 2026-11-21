# Penguibot V5.1 — Blue Edition

Penguibot is an independent custom extension for [PenguinMod Studio](https://studio.penguinmod.com/) that adds OpenAI-based chatbot and image-generation blocks.

**Status:** Public beta / community release. Not an official PenguinMod or OpenAI product, and not listed in the official PenguinMod gallery.

## Features

- **Setup:** configure an API key, choose a chat model, check connection.
- **Chats:** ask questions, retrieve answers, configure response length.
- **Mood:** change and reset chatbot personality.
- **Memory:** automatic/manual/off modes, add/clear/save/load memory, project persistence.
- **Images:** generate costumes/backdrops, preset and custom output dimensions, resizing modes, quality controls.
- **Status:** last error, success status, request-in-progress Boolean.

## Install in PenguinMod

1. Download `penguibot_v5_1_blue.js` from this repository or the website.
2. Open https://studio.penguinmod.com/.
3. Open **Extensions → Load Custom Extension → File**.
4. Select `penguibot_v5_1_blue.js`.
5. Allow **Run without sandbox** only after you have reviewed and trust the code.
6. Locate the new blue **Penguibot** block category.

The extension needs an OpenAI API key for API requests. API usage may incur charges and requires your own API account and access to supported models.

## Key security — read before using

**Never commit an API key or save/share a PenguinMod project that contains a key in a block.**

This V5.1 extension uses **direct browser-to-OpenAI requests**. Even though the extension's `serialize()` method excludes its runtime key, entering a key as literal block input can cause the project itself to store it. Browser-side keys can be extracted by code running in the browser. This architecture is meant for private testing, **not secure production deployment**. For a safer public deployment, use an authenticated backend proxy, server-side credentials, usage limits, and abuse protections.

The public website in this repository is an informational/download page, not a working chat app and never asks for an API key.

## Project files

- `penguibot_v5_1_blue.js` — extension source
- `index.html` — static download/documentation website
- `assets/penguibot-banner.webp` — logo/banner
- `LICENSE` — MIT License
- `.nojekyll` — GitHub Pages static-site support

## Publish with GitHub Pages

Create a **public** GitHub repository called `Penguibot`. Upload all these files preserving the `assets/` directory. Open **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/(root)**, then save.

Your site will typically be at `https://YOUR-USERNAME.github.io/Penguibot/`. That URL is an example, not a live link until you publish.

## License

MIT. See `LICENSE`.
