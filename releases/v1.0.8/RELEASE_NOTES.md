# ABM AV Player v1.0.8 — Stability, diagnostics and unified design system

**Windows x64 installer:** [Download ABM-AV-Player-Setup.exe](https://github.com/abmullick/ABMAVPlayer/releases/download/v1.0.8/ABM-AV-Player-Setup.exe)

**SHA-256:** `209f40d5518251b3ddcdd2b70725324e12e073c198859c91222a8312e0a3ffee`

## What's new

- Unified the Main Player, Streaming Centre, Torrent Stream, Settings, Advanced Settings, Help Centre, About, Equalizer and modal surfaces around shared ABM Direct2D/DirectWrite rendering, typography roles, icon-font tokens, semantic surfaces and common geometry.
- Improved typography consistency, wordmark alignment, control surfaces, focus/hover states, clipping, text trimming and fallback rendering across application windows.
- Reworked Settings sizing and scrolling for constrained window sizes and monitor work areas, with custom ABM-rendered scrollbars, keyboard navigation and improved focus visibility.
- Improved Help Centre article navigation, search, typography, paragraph rendering and the Advanced Settings diagnostics guidance.

## Playback, streaming and Torrent reliability

- Added structured playback failure reporting and safer playback cleanup; centralized local playback engine commands.
- Hardened Torrent playback and streaming lifecycles, including stale callback rejection, decoder-error teardown, HTTP request lifetime, stream readiness and cancellable worker shutdown.
- Improved Torrent recovery for classified transient errors and stalled downloads, corrected paused-state handling, and fixed cache quota accounting to include actual torrent payload storage.
- Reclaimed queued worker payloads and cleaned up stale artwork downloads and resource ownership during playback changes and Streaming Centre teardown.
- Preserved separation between the local player, Streaming Centre casting/discovery and Torrent Stream's independent playback/casting paths.

## Diagnostics and documentation

- Added the VLC Runtime & Codecs diagnostics page and included runtime details in diagnostic reports.
- Documented the evidence levels File Found, Plugin Loaded, Runtime Tested and Playback Verified; plugin discovery/loading is not the same as codec certification.
- Expanded Settings, User, Developer, UI design-system and Windows QA documentation.

## Installation

1. Download the Windows x64 installer.
2. Close ABM AV Player before upgrading an existing installation.
3. Run the installer and follow the prompts.

## Verify download

Use PowerShell:

```powershell
Get-FileHash .\ABM-AV-Player-Setup.exe -Algorithm SHA256
```

Compare the result with the SHA-256 value above.

## Compatibility notes

- Windows x64.
- Microsoft Edge WebView2 Evergreen Runtime is required for Streaming Centre browser integration.
- The installer is unsigned; Windows SmartScreen may display an unknown-publisher warning.

© 2026 Abhishek Basu Mullick. All rights reserved. Original ABM AV Player materials are proprietary. Third-party components remain subject to their respective licences.
