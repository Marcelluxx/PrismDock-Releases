# PrismDock Official Releases

This repository hosts the public Windows installers, SHA-256 checksums, and Minisign-verified auto-updater feed (`latest.json`) for **PrismDock**.

> **Source Code:** PrismDock's source code is maintained privately. This repository distributes compiled release binaries and cryptographic update manifests only.

## Downloads

- **Latest Release:** [GitHub Releases](https://github.com/Marcelluxx/PrismDock-Releases/releases/latest)
- **Windows x64 NSIS Installer:** `PrismDock_<version>_x64-setup.exe` (used by the in-app auto-updater)
- **Windows x64 MSI Installer:** `PrismDock_<version>_x64_en-US.msi` / `it-IT.msi`
- **Updater Feed:** `https://github.com/Marcelluxx/PrismDock-Releases/releases/latest/download/latest.json`

## Verifying Checksums & Signatures

1. Verify installer SHA-256 against `SHA256SUMS.txt` on the corresponding release:
   ```powershell
   Get-FileHash .\PrismDock_0.6.0_x64-setup.exe -Algorithm SHA256
   ```
2. In-app updates are cryptographically verified by `tauri-plugin-updater` using the embedded **Minisign (Ed25519)** public key ID `3B8EB4CAB2BA1229`.