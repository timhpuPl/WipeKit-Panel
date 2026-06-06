  <div align="center">

  <img src="https://wipekit.net/wipekit.svg" width="64" height="64" 
  alt="wipekit" />

  # WipeKit

  **Self-hosted Rust dedicated server management panel**

  [![Version](https://img.shields.io/badge/version-v0.1.0-blue?style=flat-square)](https://github.com/timhpuPl/WipeKit-Panel/releases)
  [![Node](https://img.shields.io/badge/node-20+-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
  [![Platform](https://img.shields.io/badge/platform-Ubuntu%20%2F%20Debian-E95420?style=flat-square&logo=ubuntu&logoColor=white)](https://ubuntu.com)
  [![License](https://img.shields.io/badge/license-Proprietary-red?style=flat-square)](#license)
  [![Early Access](https://img.shields.io/badge/status-Early%20Access-yellow?style=flat-square)]()

  [Documentation](https://wipekit.net/docs) ·
  [Support](https://wipekit.net/support) ·
  [Releases](https://github.com/timhpuPl/WipeKit-Panel/releases)

  </div>

  ---

  
  ## Overview

  WipeKit is a self-hosted web panel for managing Rust dedicated servers. It
  runs entirely on your own machine - no cloud, no subscriptions, no tracking.

  Connect to your server via RCON and get a modern browser-based interface for
  controlling, monitoring, and automating everything.

  ## Features

  - **Dashboard** - live server status, CPU, memory, uptime, and RCON console
  - **Server Control** - start, stop, restart, update via SteamCMD
  - **Player Management** - track playtime, VAC/game bans, kick/ban/mute
  - **Scheduler** - cron-based jobs for wipes, restarts, broadcasts, and custom
  commands
  - **Wipe Tool** - map wipe and full wipe with configurable seed and world size
  - **File Manager** - browse, edit, and delete server files without SSH
  - **Addons** - install and auto-update Oxide or Carbon from GitHub releases
  - **Plugin Manager** - view and remove Oxide/Carbon plugins
  - **Discord Integration** - webhook notifications and bot chat bridge
  - **Multi-admin** - role-based permissions per tab and action
  - **Setup Wizard** - guided first-run setup with SteamCMD installer

  ## Requirements

  - Ubuntu 20.04+ or Debian 11+ (x86_64)
  - Node.js 20+
  - `sudo` access (for system dependencies and systemd)

  ## Installation

  Download the latest release from the 
  [Releases](https://github.com/timhpuPl/WipeKit-Panel/releases) page and run 
  the installer:

  ```bash
  wget https://github.com/timhpuPl/WipeKit-Panel/releases/download/Early_Access/wipekit-v0.1.0.zip
  unzip wipekit-v0.1.0.zip
  cd wipekit-v0.1.0
  ./install.sh

  The installer will:
  - Check and install all required system packages (curl, unzip, lsof, SteamCMD
  libs)
  - Install backend dependencies
  - Create a default config
  - Register wipekit as a systemd service that auto-starts on reboot

  The panel will be available at http://YOUR_SERVER_IP:3000.
  On first launch you will be taken through the setup wizard.

  Managing the service

  # Start / stop / restart
  sudo systemctl start wipekit
  sudo systemctl stop wipekit
  sudo systemctl restart wipekit

  # Check status
  sudo systemctl status wipekit

  # View live logs
  journalctl -u wipekit -f

  # Disable autostart on boot
  sudo systemctl disable wipekit

  Changelog

  v0.1.0 - Early Access

  - Initial release
  - Dashboard with metrics, live RCON console, player list, and server info
  - Server control: start / stop / force-stop / graceful stop / restart / update
  - Player tracking with Steam ban data
  - Cron scheduler with countdown announcements
  - Wipe tool with seed and world size configuration
  - File manager with text editor
  - Oxide and Carbon addon management with auto-update on server stop
  - Plugin manager for Oxide/Carbon plugins
  - Discord webhook notifications and bot chat bridge
  - Multi-admin support with per-role permission system
  - Setup wizard with SteamCMD installer
  - systemd service auto-registration on install

  License

  WipeKit is free to use. The software is distributed in compiled form.
  Redistribution, reverse engineering, or resale is not permitted.
  All rights reserved © 2026 timhpu.
