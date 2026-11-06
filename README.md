<p align="center"><img src="icon.png" alt="ToyBridge logo" width="200"></p>

# ToyBridge-Releases
Installers and updates for ToyBridge

ToyBridge makes your toys react to SPS contacts in VRChat. It connects to toys
through Intiface Central, so it works with Lovense and anything else Intiface
supports. Built to stay running: start it once and leave it in the tray.

**[Download the latest version](https://github.com/xanderdigitalVT/ToyBridge-Releases/releases/latest)**

## What it does

**Each motor gets its own channel strip, like on a mixing desk:**

- **On / Off:** turns that motor on or off. The big meter shows its current level, and the thin bar beside it shows the raw contact.
- **Depth / Motion / Mix:** reacts to how deep the contact is, how fast it's moving, or a mix of both.
- **Min / Max:** Min is the level as soon as anything touches. Max is the strongest it will go.
- **Routing:** chooses what the motor reacts to (my hands, others' hands, my own parts, others' parts, frotting), which part types, and which SPS parts. If you pick no parts, it follows all of them.
- **Test:** pulses the motor for a moment.

**It handles these without a restart:**

- **VRChat** starting before or after ToyBridge, restarting, closing or crashing. Toys stop if VRChat closes or crashes.
- **Avatar changes.** The new avatar's SPS parts are read from VRChat, and your toy settings for that avatar come back.
- **Intiface Central** closing, restarting or going silent. ToyBridge keeps trying to reconnect, and a tray notice tells you.
- **Toys** turning off, dropping out or coming back. They reappear on their own, with their settings, and a tray notice names the toy.
- **Failed toy scans,** such as Bluetooth being off. ToyBridge keeps retrying.

**Features:**

- **Avatar profiles:** each avatar remembers its own routing, Depth / Motion / Mix and Min / Max, which come back when you switch to it. An avatar you haven't used before keeps the current settings with all parts selected, and switching never turns on a toy you switched off. **Avatar** in the top bar lists your saved avatars, and you can turn this off in **Settings**.
- **Connection notices:** a tray notice appears when Intiface or a toy drops, and again when it returns, so you'll know why the buzzing stopped. Short blips don't count. It's a normal Windows notification, so seeing it in a headset takes an overlay that shows them. You can turn these off in **Settings**.
- **Clear port messages:** if another app, such as Warudo, holds the port VRChat sends to while VRChat is open, ToyBridge names the app and explains what to do.
- **Master and Stop all:** the Master fader scales every toy, and Stop all stops every toy at once. Stop all is in the tray menu too, called Pause.
- **Automatic updates:** new versions download in the background, and ToyBridge never restarts by itself, so toys won't stop mid-session. Click **Restart to update** in the top bar, or the update installs the next time you quit ToyBridge. **Settings** shows your version and has a **Check now** button.

Your settings are kept in `%APPDATA%\ToyBridge\config.json`, and logs are in the `logs` folder beside it.

## Install

You'll need Windows, [Intiface Central](https://intiface.com) (free), an avatar with SPS, and a toy that Intiface supports. Most toys also need Bluetooth on the PC running Intiface.

1. Download `ToyBridge-<version>.zip` from the [latest release](https://github.com/xanderdigitalVT/ToyBridge-Releases/releases/latest) and extract it.
2. Run `ToyBridge-Setup-<version>.exe`. If Windows says "Windows protected your PC," click **More info**, then **Run anyway**. This appears because the app isn't code-signed.
3. Follow the installer. ToyBridge then appears in your Start menu.

To uninstall, open the Start menu and run **Uninstall ToyBridge**. Your settings and logs are kept in case you reinstall.

## Getting started

1. In Intiface Central, press **Start Server**.
2. In VRChat, open the Action Menu, go to **Options → OSC** and turn on **Enabled**.
3. Turn on your toy. It should appear in ToyBridge on its own. Pair it through Intiface, not through Windows Bluetooth settings.
4. Press **Test** on a toy's strip. The motor should pulse for a moment.

If Intiface runs on another PC, change the Intiface address in **Settings**.

Don't run OscGoesBrrr at the same time, or both apps will drive the same toys.

Closing the window only hides ToyBridge in the tray. To exit fully, right-click the tray icon and choose **Quit ToyBridge**.
