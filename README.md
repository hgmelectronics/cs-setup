# CS Setup Desktop App Releases

This repository contains release artifacts and deployment configurations for the CS Setup desktop application, built with Electron.

## Overview

This repository manages the distribution of pre-built binaries and installation packages for multiple platforms. This will be used for auto-updates of the Electron apps.

## Supported Platforms

- **macOS**: `.dmg` installer and `.zip` archive
- **Windows**: `.exe` installer and `.zip` portable version
- **Linux**: `.AppImage`, `.deb`, and `.rpm` packages

## Latest Release

Download the latest version from the [Releases](../../releases) section.

### Installation

1. Go to the [Releases](../../releases) page
2. Download the appropriate installer for your platform:
   - **macOS**: Download `CS-Setup-[version].dmg`
   - **Windows**: Download `CS-Setup-[version]-Setup.exe`
   - **Linux**: Download `CS-Setup-[version].AppImage` (universal) or platform-specific packages
3. Run the installer and follow the setup instructions

## Development

The main application source code is maintained in the [cs-setup repository](https://github.com/your-org/cs-setup).

### Building Releases

To build new releases:

1. Clone the main repository
2. Install dependencies: `npm install`
3. Build for all platforms: `npm run build:all`
4. Package the app: `npm run package:all`
5. Create a new release in this repository with the built artifacts

### Release Process

1. **Build**: Generate platform-specific binaries using Electron Builder
2. **Test**: Verify installations on target platforms
3. **Tag**: Create a git tag for the version (e.g., `v1.0.0`)
4. **Upload**: Attach built binaries to the GitHub release
5. **Announce**: Update documentation and notify users

## Requirements

- **macOS**: macOS 10.13 or later
- **Windows**: Windows 10 or later (64-bit)
- **Linux**: Most modern Linux distributions with glibc 2.17+
