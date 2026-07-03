# Axion Releases

Download the latest Axion release for Windows and Android from the Releases page.

# Axion

Axion is a Windows application for using Axion with Brawl Stars through an Android emulator. This release includes a ready-to-use Windows build with the required internal files needed to run `Axion.exe`.

> **Note:** Use Axion only in ways that comply with the rules and terms of the services and games you use. Never publicly share personal tokens, license keys, or configuration files.

## Supported Platforms

| Platform                        | Status          | Notes                                          |
| ------------------------------- | --------------- | ---------------------------------------------- |
| Windows 10 / Windows 11, 64-bit | ✅ Supported     | This release includes `Axion.exe` for Windows. |
| macOS                           | ❌ Not supported | No macOS build is included.                    |
| Linux                           | ❌ Not supported | In development.                                |
| Android                         | ✅ Supported     | Axion runs directly on mobile using the APK.   |

## Requirements

For this release, you need:

* A Windows 10 or Windows 11 PC, 64-bit.
* The `Axion-0.0.4-windows.zip` download.
* Enough free storage space to fully extract the zip file.
* An Android emulator for Windows, such as BlueStacks, LDPlayer, MuMu Player, or a similar emulator.
* Brawl Stars installed in the emulator.
* A working internet connection.
* A valid Axion license or access, if required by your version.
* Access to your Axion configuration, such as player settings, emulator port, and optional webhook settings.

You normally do not need to install Python separately, because the Windows build includes the required internal runtime files.

## Installation

1. Download `Axion-0.0.4-windows.zip` from the GitHub Releases page.
2. Fully extract the zip file.
3. Open the extracted `Axion` folder.
4. Keep the folder structure intact. Do not move `Axion.exe` out of the folder, because the app requires the `_internal` folder.
5. Start your Android emulator.
6. Open Brawl Stars in the emulator and make sure your account is ready in the lobby.
7. Double-click `Axion.exe` to start Axion.

## Emulator Settings

Axion uses ADB to communicate with the Android emulator. Make sure that:

* The emulator is running before you start Axion.
* Brawl Stars is installed and open.
* ADB access is available in the emulator.
* The emulator port matches the value in `general_config.toml`.
* The emulator resolution and scaling match the settings Axion is configured for.

If Axion cannot find the emulator, check the emulator port and restart both the emulator and Axion.

## Updates

New versions may be published through GitHub Releases. When updating, download the latest zip file, extract it again, and only restore your own safe configuration files. Do not copy old internal files into a new version unless this is explicitly instructed.

## Troubleshooting

### Axion Does Not Start

* Make sure the zip file has been fully extracted.
* Start `Axion.exe` from inside the `Axion` folder.
* Check whether antivirus software is blocking the app.
* Try running Axion as administrator.

### The Emulator Is Not Found

* Restart the emulator.
* Check the `emulator_port` value in `general_config.toml`.
* Make sure ADB is available.
* Open Brawl Stars before starting Axion.

### Brawl Stars Is Not Detected Correctly

* Check the emulator resolution and window size.
* Make sure Brawl Stars is in the lobby.
* Avoid overlays, pop-ups, or other windows covering the emulator.
* Check the settings in `lobby_config.toml`.

### Webhooks Are Not Working

* Check `webhook_config.toml`.
* Make sure the webhook URL is correct.
* Check whether your internet connection is active.

## Project Structure

After extraction, the main folder structure should look similar to this:

```text
Axion/
├── Axion.exe
└── _internal/
    ├── cfg/
    ├── static/
    └── other internal files
```

## Security

Never publish sensitive data on GitHub. Always check the files inside `Axion/_internal/cfg/` before making anything public. This includes licenses, sessions, tokens, API keys, player tags, and webhook URLs.

Recommended `.gitignore` entries for your repository:

```gitignore
Axion/_internal/cfg/*session*.json
Axion/_internal/cfg/*client*.json
Axion/_internal/cfg/*api*.toml
Axion/_internal/cfg/webhook_config.toml
```

## License

This project is not permitted to be sold or monetized.

```text
All rights reserved.
```

## Disclaimer

Axion is not officially affiliated with Supercell or Brawl Stars. Brawl Stars and Supercell are trademarks of their respective owners. Use this project at your own risk.

## Credits

This project uses and benefits from open-source software created by the community.

Special thanks to PylaAI for their open-source work and resources that helped make this project possible.

All third-party projects remain the property of their respective authors and are used according to their original licenses. Please check the original repositories and license information for more details.

https://github.com/PylaAI/PylaAI
