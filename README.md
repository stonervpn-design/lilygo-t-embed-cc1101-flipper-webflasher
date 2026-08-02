# Flipper — LilyGo T-Embed CC1101+ (Public) · Web Flasher

Flash the **public** Flipper port for the **LilyGo T-Embed CC1101+** straight from your browser — no drivers, no Python, no command line.

👉 **[Open the flasher](https://stonervpn-design.github.io/lilygo-t-embed-cc1101-flipper-webflasher/)** in desktop **Chrome** or **Edge**, plug in via USB‑C data cable, click **Connect & Install**.

## What this is

- **Public build:** the in-tree ProtoPirate car‑key SubGHz decoders and the **CAN Commander** (OBD/CAN) app are removed. The **Defender** RF attack detector and everything else stay; the community standalone **ProtoPirate** app is included.
- **App image, ESP32‑S3, 16 MB flash**, merged at offset `0x0`. The T-Embed's on-board **CC1101** is the SubGHz radio.

## ⚠️ You need a microSD card

Like the Cardputer, the T-Embed keeps its databases on a **real microSD card**, not internal flash. **[Download `sd_content.zip`](./sd_content.zip)** and extract it to the **root of a FAT32 microSD** so the card root has `/subghz`, `/nfc`, `/infrared`, and `/Manifest`. Without it, SubGHz KeeLoq decoding, NFC dictionaries, and IR universal remotes won't work. (The loose files are also in [`sd_content/`](./sd_content).)

The `sd_content/` set is **public databases only** (`keeloq_mfcodes_user`, `dangerous_settings`, NFC dicts, IR databases). Proprietary encrypted keystores (`keeloq_mfcodes`, `alutech_at_4n`, `nice_flor_s`) are intentionally excluded.

## Requirements

- LilyGo T-Embed CC1101+ + microSD (FAT32)
- Desktop **Chrome** or **Edge** (Web Serial); a USB‑C **data** cable

## Community

📢 Official updates & community — join at **[nexoria.chat](https://nexoria.chat/join/0f30a32e)**.

*Not affiliated with Flipper Devices or LilyGo. For authorized security testing, education, and hardware you own.*
