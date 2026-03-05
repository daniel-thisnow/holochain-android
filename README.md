# Holochain for Android (aarch64)

Cross-compiles Holochain conductor for `aarch64-linux-android` using GitHub Actions.

## Usage

1. Go to **Actions** tab
2. Click **Build Holochain for Android**
3. Enter the holochain version tag (default: `holochain-0.6.1-rc.1`)
4. Click **Run workflow**
5. Wait ~30-60 min
6. Download the `holochain-android-aarch64` artifact

## What it builds

- `holochain` — conductor binary (iroh transport)
- `lair-keystore` — key management
- `hc` — CLI tools

All compiled for Android ARM64 without needing PRoot or glibc shims.

## Install on device

```bash
# In Termux (no proot needed):
cp holochain $PREFIX/bin/
cp lair-keystore $PREFIX/bin/
chmod +x $PREFIX/bin/holochain $PREFIX/bin/lair-keystore
holochain --version
```
