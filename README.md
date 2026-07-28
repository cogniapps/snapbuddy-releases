# SnapBuddy — releases

Download and update host for [SnapBuddy](https://github.com/cogniapps/snapbuddy), a screen
capture + annotate + QA bug-reporting tool for Windows.

**This repository contains no source code.** It exists only to serve release artifacts, because
the in-app updater fetches its manifest over anonymous HTTPS and release assets on a private
repository require an authentication token.

## Install

Grab `SnapBuddy_<version>_x64-setup.exe` from the [latest release](../../releases/latest) and run
it. Windows SmartScreen will warn on this first install (the installer is not code-signed) —
choose **More info → Run anyway**.

After that, SnapBuddy updates itself: it checks once at startup and offers to install anything
newer, and there is a **Check for updates…** item in the tray menu and in Settings. Updates are
verified against an embedded public key before they are applied, and never install without asking.

## Assets in each release

| File | Purpose |
|---|---|
| `SnapBuddy_<v>_x64-setup.exe` | The installer — use this for a first install |
| `SnapBuddy_<v>_x64-setup.nsis.zip` | The update payload the app downloads |
| `SnapBuddy_<v>_x64-setup.nsis.zip.sig` | Detached minisign signature of the payload |
| `latest.json` | The manifest the updater polls |
