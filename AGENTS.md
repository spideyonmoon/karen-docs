> **First-time setup**: Customize this file for your project. Prompt the user to customize this file for their project.
> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Karen Documentation — Project Instructions

## About This Project

- **Karen** is an Apple Music Telegram bot that rips lossless audio using Frida-hooked Android emulators
- This is a **Mintlify** documentation site (https://mintlify.com)
- Pages are **MDX files with YAML frontmatter** (see examples in existing pages)
- Configuration lives in `docs.json`
- See **Assistant.md** for tone, style, and Karen-specific knowledge

## Terminology

- **Wrapper-Manager** — upstream service running Android emulator with Frida hooks (not "wrapper" or "manager" alone)
- **Pool** — FIFO load balancer across wrapper-manager instances
- **DRM** — Digital Rights Management (FairPlay for Apple Music, not Widevine)
- **MTProto** — Telegram's native protocol (used for uploads >50MB)
- **Bot** — The Karen service (written in Go)
- **Rip** — Download + decrypt + remux audio from Apple Music

## Style Preferences

- **Voice:** Friendly, direct, developer-focused (assume technical audience)
- **Sentences:** Concise, one idea per sentence
- **Headings:** Sentence case (`Getting started`, not `Getting Started`)
- **Bold:** For UI text, file paths, commands — **`bot/main.go`**
- **Code:** Always include language tag and be copy-paste ready
- **Links:** Use relative paths — `/commands/user-commands` not `https://...`
- **Components:** Lean on Mintlify components (`<Tip>`, `<Warning>`, `<Card>`, `<Steps>`)

## Content Boundaries

### ✅ DO Document

- **Setup & Deployment** — how to get Karen running
- **Commands** — what users can do
- **Architecture** — how Karen works internally
- **Troubleshooting** — common issues & solutions
- **Configuration** — environment variables, tuning

### ❌ DON'T Document

- Reverse-engineering specifics (keep legal/ethical boundaries)
- Private URLs, credentials, or internal VPS details
- Upstream wrapper-manager implementation (link to upstream instead)
- Commercial licensing or pricing (Karen is open-source)

## Before Publishing Changes

1. Verify all relative links work (`/guides/configuration` not `/guides/configuration/`)
2. Check code snippets are syntactically valid
3. Run examples mentally — they should be copy-paste ready
4. Use `<Card>` to link related pages
5. Add `Coming soon:` header to incomplete sections
6. See **Assistant.md** for detailed style guide
