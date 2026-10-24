# Awesome-Video-Screen-Recording-E-Learning

# Top Video Screen Recording & E-Learning Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Self-Hosted Recording, Browser-Native Capture & Interactive Course Authoring*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Video Screen Recording & E-Learning**. These tools span two related jobs: capturing screen activity with cursor effects and narration for demos or tutorials, and turning that content into structured learning experiences — with a spectrum running from polished commercial recorders to open-source tools you can self-host and audit.

**Examples** include OBS Studio, OpenScreen, Cap, SendRec, eXeLearning, and H5P (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, GPU-accelerated recording, and transparent data ownership — ideal for educators, developers, and teams who want Loom-style sharing or Camtasia-style editing without subscription fees.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Loom** — **The reference async video messaging platform.** Screen and camera recording with instant share links, viewer analytics, and team workspaces. **Free tier** with limits; paid plans per-user. **Trade-offs**: cloud-only, per-viewer analytics gated behind paid tiers, and recordings live on Loom's infrastructure. **Best for teams wanting the most frictionless async video sharing** and accepting vendor dependency.

- **TechSmith Camtasia** — **The professional screen recording and editing suite.** Timeline-based editing with zooms, annotations, cursor effects, and built-in quizzing. **One-time purchase** (no subscription for the desktop app). **Best for educators and creators** wanting deep editing control without recurring fees, accepting desktop-only and Windows/macOS only.

- **TechSmith Snagit** — **The screenshot and quick-capture specialist.** Annotated screenshots, short screen recordings, and GIF export with a polished capture toolbar. **One-time purchase** with optional maintenance. **Best for quick bug reports and documentation** rather than full course production.

- **Screencastify** — **The browser-based recorder for Chromebooks and education.** Records tab, screen, or camera directly in Chrome with basic editing and sharing. **Free tier** with watermark; paid plans for education and teams. **Best for K-12 Chromebook deployments** where installing desktop software isn't viable.

## Open-Source GitHub Projects

- **OBS Studio** — **The reference open-source recording and streaming suite.** GPL-2.0 licensed. **Complete video recording and live streaming** with multiple scenes, H.264 encoding, audio mixing, and direct streaming to Twitch and YouTube . **The most capable free recorder for full-screen capture** but **not designed for polished demo videos** — it lacks cursor zoom, smoothing, and timeline annotation tools that Camtasia and Screen Studio provide. **Best for live streaming and raw screen capture** where editing happens elsewhere.

- **OpenScreen** — **The open-source Screen Studio alternative for demo videos.** MIT licensed, **no watermarks, no subscriptions, free for commercial use** . **GPU-accelerated recording** on macOS (ScreenCaptureKit), Windows (Windows Graphics Capture), and Linux (PipeWire) . **Timeline editing with zooms, backgrounds, motion blur, crop/trim/speed, blur regions, annotations, auto-captions, and AI editing** . **CLI and MCP server** for headless recording and AI agent integration — the agent can plan a storyboard, record, edit, and attach the video to a pull request . **Runs on Windows, macOS, and Linux** with signed macOS builds notarized by Apple . **Best for developers and creators** wanting polished demo videos with cursor zoom and background styling without Screen Studio's cost.

- **Cap** — **The open-source Loom alternative with self-hosting and S3 storage.** **AGPL licensed**, **Instant Mode** uploads while recording for a share link the moment you stop, and **Studio Mode** records locally with timeline editing, backgrounds, zooms, captions, and export controls . **Own your storage**: connect AWS S3, Cloudflare R2, Backblaze B2, MinIO, or Wasabi; keep recordings local; or **self-host the full platform with Docker Compose** . **Comments, reactions, transcripts, viewer analytics, team workspaces, custom domains, and AI summaries/chapters** . **Best for teams migrating from Loom** wanting shareable links with full data ownership and no per-viewer pricing.

- **SendRec** — **The self-hosted Loom alternative focused on GDPR and analytics.** **AGPL licensed**, **runs anywhere Docker runs** . **Browser-native recording** on Chrome, Safari, and Firefox — no desktop app required . **Sharing with password protection, expiry dates, and per-video download controls** . **Automatic transcription** via local whisper.cpp or OpenAI-compatible/Deepgram cloud providers, with AI-generated summaries, chapter markers, clickable transcripts, and closed captions . **Per-video analytics**: view counts, completion funnel (25/50/75/100%), and CTA click-through rates . **Slack notifications, webhooks, embeddable player, custom branding, and email gating** . **Best for EU organizations** needing data residency and Loom-style sharing with browser recording.

- **Recordly** — **The open-source recorder with timeline editing and a cursor-effects focus.** **AGPL licensed**, **prebuilt releases for macOS and Windows** with Linux builds from source . **Timeline editing for zooms, trims, speed regions, annotations, extra audio regions, and crop-aware edits** with **.recordly project persistence** . **Cursor controls**: size adjustment, smoothing, motion blur, click bounce, sway, loop mode, and macOS-style cursor assets . **Webcam overlay** with mirroring, sizing, positioning, roundness, and shadow controls . **Frame styling** with wallpapers, gradients, padding, rounded corners, background blur, and drop shadows . **Extensions marketplace** for community-built cursor sounds, device frames, browser mockups, and render hooks . **Best for polished demo videos** where cursor smoothing and frame styling matter.

- **eXeLearning** — **The AGPL-licensed authoring tool for interactive educational resources.** **Maintained by Spain's Ministry of Education** through Cedec-INTEF, with coordinated development across regional administrations . **Creates interactive educational projects with iDevices** (interactive elements), hierarchical content structure, and multilingual support . **Exports to various formats including SCORM**, with **Moodle integration**, RESTful API, **real-time collaborative editing via Yjs WebSocket**, and multiple authentication methods (Password, CAS, OpenID Connect) . **Docker deployment**: `docker run -p 8080:8080 exelearning/exelearning` . **Offline installers** for Linux, Windows, and macOS via Electron . **Best for educators** wanting a self-hosted course authoring platform with Moodle integration.

- **H5P (via Lumi Desktop Editor)** — **The interactive content format with an offline authoring editor.** **Lumi Desktop Editor is free, open-source, and works offline without programming** . **Creates H5P content types**: interactive books, interactive videos, course presentations, quizzes, drag-the-words, branching scenarios, and 360° tours . **Exports to standalone HTML and SCORM 1.2** for distribution without a platform, via Moodle, or through Lumi Cloud . **H5P integrates with Moodle, Brightspace, Blackboard, and other LMS platforms** . **Best for teachers** wanting to build interactive video quizzes and branching scenarios that run offline or embed in an LMS.

### Additional Strong Open-Source Options

- **Framepipe** — GPU-accelerated screen recorder for **Linux/Wayland only**, with cursor smoothing/smearing, auto follow/zoom, and GStreamer encoding (VAAPI/QSV/CPU). **DRM/KMS or PipeWire capture**, H.264/H.265/AV1 support, and **a self-described "broken gui"** — CLI-focused . Best for Linux power users wanting zero-copy recording with cursor effects.
- **GPU Screen Recorder** — Linux recorder minimizing system impact by using the GPU only, similar to Windows Shadowplay . Best for gaming capture on Linux.
- **vokoscreenNG** — User-friendly Linux screencaster with Qt/GStreamer, rewritten from the discontinued Vokoscreen project . Best for simple Linux desktop recording.
- **Kooha** — Simple GTK-based Linux recorder to "elegantly record your screen" . Best for minimal Wayland recording.
- **Screendrop** — Native macOS screenshot + recording + Loom alternative with **teleprompter**, non-destructive session packages, and on-device transcription . Best for Mac users wanting a native teleprompter-equipped recorder.

**Frameworks for building custom systems**: Combine **OBS Studio** for raw screen capture and streaming, **OpenScreen** or **Recordly** for polished demo videos with cursor zoom and timeline editing, **Cap** or **SendRec** for Loom-style shareable links with self-hosted storage, **eXeLearning** for structured course authoring with Moodle integration, and **H5P/Lumi** for interactive video quizzes — to build a screen recording and e-learning stack tailored to your need for raw capture versus polished demos, async sharing versus structured courses, and cloud versus self-hosted deployment.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Screen recording and e-learning tools differ significantly in editing depth, deployment model, and e-learning authoring capability. **OBS Studio is the most capable free recorder** for raw capture and streaming, but lacks the cursor zoom and demo polish of Screen Studio alternatives . **OpenScreen is a Screen Studio alternative**, not a Camtasia replacement — it handles demo videos well but isn't a full course authoring tool . **Cap and SendRec are Loom alternatives** — they handle async video sharing, not interactive e-learning content . **eXeLearning and H5P are e-learning authoring tools**, not screen recorders — they create interactive courses and quizzes that can embed recorded video, but you record separately . **Framepipe is Linux/Wayland only** and its GUI is self-described as broken — it's a CLI tool . **Recordly's Linux builds require building from source** .
- Self-hosted open-source solutions require proper storage configuration (S3-compatible for Cap), Docker deployment (SendRec, eXeLearning), and awareness that browser-based recording is limited by browser APIs compared to native capture pipelines.

---

**Made for educators, developers, and creators choosing screen recording and e-learning tools they can own and control.**
Let's make video screen recording and e-learning more open, self-hostable, and creator-friendly.
