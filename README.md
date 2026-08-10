# Kazumi Lite

A lightweight anime (番剧) tracking & playback application for Windows, inspired by [Kazumi](https://github.com/Predidit/Kazumi).

## Features

- **Multi-source search** — aggregated search across multiple anime sources
- **Playback via mpv** — lightweight, hardware-decoded video playback with a daemon-based mpv controller
- **Player customization** — hardware decoding, GPU API, cache, playback speed/volume, screenshot directory, audio/subtitle track preferences
- **Super resolution (Anime4K)** — GPU shader upscaling, hot-swappable during playback (Light / Quality modes)
- **Anti-leech support** — per-source referer / user-agent / cookie forwarding
- **Bilingual UI** (中文 / English / 日本語)
- **Danmaku (弹幕)** — planned: Bilibili anime danmaku via the [dandanplay](https://www.dandanplay.com/) danmaku library (BGM ID → danmaku library matching)

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React + TypeScript + Vite (dark terminal-inspired UI) |
| Backend | Dart (shelf HTTP server + rule-based source plugins) |
| Player | mpv (daemon mode, IPC control, Anime4K shaders) |
| Packaging | Tauri (planned) |

## Why danmaku via dandanplay

Kazumi Lite integrates danmaku by matching the anime's Bangumi ID against the public dandanplay danmaku library, following the same approach as Kazumi. This keeps danmaku data well-organized per episode without relying on private APIs.

## Status

Early-stage personal project. Not affiliated with Kazumi or dandanplay.
