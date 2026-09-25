# ✈ Airport Optimizer

Airport Optimizer is an unofficial Windows utility that safely reduces the disk space used by Tower! Simulator 3 airport `.asset` files. It applies Windows NTFS compression without moving, renaming, unpacking, or rewriting proprietary asset contents.

## Features

- Automatically detects common Steam installation locations.
- Supports manual installation paths, file selection, and drag-and-drop.
- Lists only verified ICAO airport folders containing their matching `<ICAO>.asset` file.
- Excludes AirportEditorHD and unrelated Unity assets.
- Shows logical size, actual disk usage, space saved, and compression status.
- Requires read-only analysis before selected optimize or restore operations.
- Optimizes selected airports or every detected airport.
- Restores airports by removing NTFS compression.
- Creates and verifies path-unique backups by default.
- Checks available backup space before making changes.
- Includes search, activity logs, folder shortcuts, mouse-wheel scrolling, and clear progress reporting.

## Download and installation

1. Download `AirportOptimizer-v3.4.exe` from the repository's **Releases** page or the official Google Drive link shared by the developer.
2. Keep the file anywhere convenient; no installer is required.
3. Close Tower! Simulator 3 before optimizing or restoring airports.
4. Run the executable and use **Auto-detect**, or select the game folder containing the `Airports` directory.
5. Keep **Create a backup before optimizing** enabled.

The v3.4 executable is self-contained. Friends do not need to install the .NET runtime separately.

## Safe usage

1. Scan for airports.
2. Select one or more airports.
3. Click **Analyze Selected**. Analysis does not change files.
4. Review the reported sizes and status.
5. Choose **Optimize Selected**, **Optimize All**, or **Restore Selected**.

Airport files remain at the exact paths expected by Tower! Simulator 3. Backups are stored in:

```text
Documents\Tower 3 Airport Optimizer\Backups
```

## Verify the v3.4 download

SHA-256:

```text
557A5A9D090FBE5438927195CB308D24A0A472392E916DE0F0392356BDDF364D
```

To verify it in PowerShell:

```powershell
Get-FileHash .\AirportOptimizer-v3.4.exe -Algorithm SHA256
```

## Windows security notice

The current release is not digitally signed. Windows may display an **Unknown publisher** or SmartScreen warning. Never disable Microsoft Defender. Verify that the file came from the official release link and confirm the SHA-256 value above before deciding whether to run it.

## Sharing the application

**GitHub Releases is recommended for public distribution.** It provides permanent versioned downloads, release notes, and a professional project page. Google Drive is suitable for privately sharing the executable with a few friends. In Discord, post the GitHub or Drive link rather than uploading the 68 MB executable directly.

## Build from source

Requirements: Windows and the .NET 8 SDK.

```powershell
dotnet build Tower3AirportOptimizer.csproj -c Release
```

Publish a standalone Windows executable:

```powershell
dotnet publish Tower3AirportOptimizer.csproj -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -p:IncludeNativeLibrariesForSelfExtract=true -o outputs
```

## Support

[💬 Discord profile](https://discord.com/users/1489371816215711905)

When reporting a problem, include the app version, what action you attempted, and the relevant entry from the Logs page. Do not upload proprietary airport `.asset` files.

## Disclaimer

Airport Optimizer is an unofficial community utility and is not affiliated with, endorsed by, or supported by the developers or publishers of Tower! Simulator 3. Always keep backups. Use the application at your own risk.
