# Type Nothing — downloads

Dictation for Windows that runs on your own PC. Your voice and your words never
leave your computer; the only things it downloads are the speech model, once, and
its own updates.

**[Download the latest version](../../releases/latest)** — grab the
`.exe` under Assets.

Windows will show a blue "Windows protected your PC" screen the first time,
because this installer is not code-signed yet. Click **More info**, then
**Run anyway**.

## What is in this repository

Installers and the signed manifests the app reads to update itself. That is all.
There is no source code here.

| file | what it is |
|---|---|
| `Type Nothing_<version>_x64-setup.exe` | the installer, and also what the app downloads when it updates itself |
| `Type Nothing_<version>_x64-setup.exe.sig` | its signature, which the app checks before installing an update |
| `latest.json` | the manifest the stable channel reads |
| `alpha.json` | the manifest the alpha channel reads |

Every update is signed. The app carries the public key and refuses anything that
does not verify, so a release here cannot be substituted by anyone who does not
hold the private key.

## Problems

Use **Settings → Support → Tell us what broke** inside the app. It carries the
version, the machine and the tail of the log, and never your audio or anything
you dictated.
