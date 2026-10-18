# Dark Souls II: Scholar of the First Sin Launcher

A Windows launcher for switching between **Seamless Co-op**, **OnlineFix Co-op**, and the **original game**, with built-in launcher and mod updates.

**[Download the launcher](https://github.com/itsMohammedAli/ds2-launcher-releases/releases)** — choose the asset ending in **`-online.zip`**.

## What is Seamless Co-op?

[Seamless Co-op by Yui](https://www.nexusmods.com/darksouls2/mods/1468) changes multiplayer in **Dark Souls II: Scholar of the First Sin** so friends can explore together through the game.

- Play with up to five other players.
- Boss victories and normal deaths do not end the session.
- Progression is shared, and normal multiplayer area barriers are removed.
- The mod uses separate saves from the original game. Keep backups and do not convert mod saves to vanilla saves.

The mod is in alpha and can contain bugs. This repository distributes a separate launcher; **Yui is the author of Seamless Co-op**. Read the [official mod description](https://www.nexusmods.com/darksouls2/mods/1468) for its full features and requirements.

## Before you install

- Use **Dark Souls II: Scholar of the First Sin** on Windows.
- For official Seamless Co-op multiplayer, be signed into Steam in online mode. Friends need matching game and mod versions.
- Have an internet connection for the first mod download and future updates.
- Close the game and launcher before replacing launcher files.
- Back up saves and existing game modifications. Switching launcher modes replaces matching game files.

The official mod's supported setup and limitations are described on [Nexus Mods](https://www.nexusmods.com/darksouls2/mods/1468).

## Which download?

Open [Releases](https://github.com/itsMohammedAli/ds2-launcher-releases/releases), expand **Assets**, and select:

| Asset | What to use it for |
| --- | --- |
| **`ds2-sotfs-launcher-…-online.zip`** | **Use this for a fresh install or manual upgrade.** Contains the launcher; the mod downloads from its official source when needed. |
| `ds2-sotfs-launcher-….zip` without `-online` | Compatibility package selected automatically by older launchers during an upgrade. |
| Source code archives | GitHub repository snapshots, not an installable launcher. |

## Installation

1. Download the **`-online.zip`** asset.
2. In Steam, right-click the game → **Manage → Browse local files**, then open its **Game** folder.
3. Extract the ZIP's **Launcher** folder directly into **Game**. Replace matching launcher files if upgrading.
4. Open **`Game/Launcher/ds2_sotfs_launcher.exe`**.

Your folders should look like this immediately after extraction:

```text
Dark Souls II Scholar of the First Sin/
└── Game/
    ├── DarkSoulsII.exe
    └── Launcher/
        ├── ds2_sotfs_launcher.exe
        ├── flutter_windows.dll
        ├── data/
        ├── bundles/
        │   ├── original/
        │   └── online_fix/
        ├── seamless_coop/
        │   └── install-release.ps1
        ├── updater/
        └── readme.txt
```

Keep all launcher files together. Avoid nesting another **Launcher** folder inside **Launcher**.

### First co-op launch and password

1. Choose **Seamless Co-op** in the launcher. On first use, it downloads and installs the latest stable [official GitHub release](https://github.com/yuiamoroll/DarkSouls2SeamlessCoopRelease/releases/latest), then starts the mod.
2. After that first installation, close the game before configuring your session.
3. Open **`Game/SeamlessCoop/ds2sc_settings.ini`** in a text editor and set a private co-op password. Everyone in your group must use the same password.
4. Save the file and launch **Seamless Co-op** again.

The installed mod adds **`Game/ds2sc_launcher.exe`** and **`Game/SeamlessCoop/`**. Existing INI settings and passwords are preserved during later updates.

For hosting, joining, and in-game items, follow the [official play instructions](https://www.nexusmods.com/darksouls2/mods/1468).

## Launcher modes

| Mode | What the launcher does |
| --- | --- |
| **Seamless Co-op** | Restores the original game file set, updates the official mod when needed, and starts the co-op launcher. |
| **OnlineFix Co-op** | Restores the supplied OnlineFix file set, updates the official mod when needed, and starts the co-op launcher. This is an additional mode provided by this launcher. |
| **Original Game** | Restores the original game file set and starts `DarkSoulsII.exe`. No mod download is needed. |

## Updates

Use **Options → Check for updates** to check again manually.

The same button at the top handles available updates:

| Available | Top button |
| --- | --- |
| Launcher only | **Update available** |
| Seamless Co-op only | **Update Seamless Co-op** |
| Both | **Update launcher & Seamless Co-op** |

When both need updating, the mod installs first, then the launcher updates and restarts. A mod-only update keeps the launcher open without starting the game. **Close the game before updating the mod.**

Co-op launches also check for mod updates automatically. Downloads are checked against GitHub's published size and SHA-256 digest before installation. A matching checksum verifies the download against that release; it does not independently prove a file is malware-free.

Once the mod is installed, verified installed files can be used if the release check is unavailable. Online multiplayer still requires the mod's normal Steam/network connection.

The bottom-left version links to the [Nexus Mods files page](https://www.nexusmods.com/darksouls2/mods/1468?tab=files). The bottom-right corner shows the launcher version and build.

## Troubleshooting

### Windows Defender / files missing after extraction

If a file disappears, extraction fails, or the launcher reports a missing DLL, check **Windows Security → Virus & threat protection → Protection history** for the affected file and detection name.

False positives are possible, but **a detection must not automatically be assumed to be a false positive**. Keep Defender enabled while investigating. Download only from this repository's releases and the official mod sources, and compare the ZIP's SHA-256 with the digest shown in GitHub's Assets list.

If you believe a detection is incorrect, report the filename and detection name to the relevant maintainer and [submit the file to Microsoft for analysis](https://www.microsoft.com/en-us/wdsi/filesubmission). Keep the file quarantined until its safety has been established; do not disable protection or add broad exclusions just to make it run.

See Microsoft's [Protection History guidance](https://support.microsoft.com/en-us/windows/security/windows-security/protection-history-in-the-windows-security-app).

### Update fails

- Close the game and leave only one launcher window open.
- Check your connection and write permissions for the installation folder, then retry.
- If recovery files are reported, keep them until the issue is resolved.
- For a manual launcher upgrade, close the launcher and extract a fresh **`-online.zip`** into **Game**.

### Cannot connect to friends

Check that everyone has matching mod/game versions and the same session password. For mod-specific errors, use the [official Nexus page](https://www.nexusmods.com/darksouls2/mods/1468).

## Credits and links

- **Seamless Co-op author: Yui** — [Nexus Mods](https://www.nexusmods.com/darksouls2/mods/1468)
- [Official Seamless Co-op GitHub releases](https://github.com/yuiamoroll/DarkSouls2SeamlessCoopRelease/releases)
- [Launcher downloads](https://github.com/itsMohammedAli/ds2-launcher-releases/releases)
