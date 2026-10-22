---
title: Privacy Policy
description: "Camlane privacy policy: Camlane collects nothing; the ad-supported Android build includes Google AdMob; the foss build has no ad or tracking SDKs."
permalink: /camlane/privacy/
layout: default
---

# Privacy Policy

**Effective date: 2026-10-22**

This policy covers the Camlane Android app (the ad-supported `ads` build published on GitHub Releases and the ad-free `foss` build you can compile yourself), the Camlane desktop app and `camlane-cli`. It is also published at https://aryan0078.github.io/camlane/privacy/.

## Summary

- **Camlane itself collects nothing.** It has no accounts, analytics, telemetry or crash reporting, and no Camlane server exists to send data to.
- **Your camera and microphone stream only to the desktop you pair with on your own local network.** They never go to the developers or to any server.
- **The `ads` build includes Google AdMob**, which may collect data as described below. The **`foss` build contains no third-party advertising, analytics or tracking SDKs.**
- **The desktop app fetches one static JSON file from GitHub** at most once a day to show a sponsor card. That request carries no identifiers.

## What is processed, where it goes, and who receives it

| Data | Where it goes | Who receives it |
|------|---------------|-----------------|
| Camera video and microphone audio | over your local network, directly to the desktop you paired with | you only |
| Pairing PIN and token, paired-device list, settings, imported LUTs | stored on your phone and your computer | nobody |
| Discovery information: the desktop's display name, OS and Camlane version; the phone's model name and a random per-install ID | your local network only | devices on your local network and the desktop you connect to |
| Logs | stored locally; shared only if you paste them into a bug report yourself | nobody unless you choose |
| **`ads` build only:** advertising ID, IP address, device and app information, ad interactions | Google AdMob, when the phone is online | Google, under Google's policies (see below) |
| **Desktop GUI only:** one HTTPS request for `sponsors/desktop.json`, at most once a day | `raw.githubusercontent.com` (GitHub) | GitHub receives the standard information of any web request (IP address, user agent) under the [GitHub Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement). Camlane adds no cookies, identifiers or query parameters. |

## Permissions on Android

- **Camera and microphone:** used only to capture what you stream to your paired desktop.
- **Nearby devices** (Android 13+) **or location** (Android 8–12): Android requires these permissions to discover devices on Wi-Fi. Camlane never reads or stores your location.
- **Notifications:** required for the foreground-service notification that keeps streaming alive.
- **Internet:** Android requires this for any network socket, including local-network ones. In the `ads` build it is also used to load ads.
- **Advertising ID** (`ads` build only): declared by the Google Mobile Ads SDK.

## Advertising (`ads` build only)

The APK published on GitHub Releases shows banner ads from **Google AdMob** on the Devices and Settings screens. There are never ads on the camera preview. Ads pause while you stream and do not load when the phone is offline.

Google may collect and use your device's advertising ID, IP address, device information and ad interactions to deliver, measure and personalise ads. Read **[How Google uses information from sites or apps that use its services](https://policies.google.com/technologies/partner-sites)** and the [Google Privacy Policy](https://policies.google.com/privacy).

- **Consent:** if you are in the European Economic Area, the United Kingdom or Switzerland, the app asks for consent through Google's User Messaging Platform before personalised ads are requested. You can review or change your choice any time in **Settings → Privacy & ad choices**.
- **Advertising ID controls:** you can reset or delete your advertising ID, or opt out of ad personalisation, in your Android settings (Settings → Google → Ads, or Settings → Privacy → Ads, depending on the device).
- **No ads at all:** build the `foss` flavor, which contains no ad SDK. See [MONETIZATION.md](https://github.com/aryan0078/camlane/blob/main/MONETIZATION.md).

Camlane never passes camera, microphone or stream data to the ad SDK.

## Children

Camlane is not directed at children under 13 and does not knowingly collect personal information from children. Camlane itself collects no personal information from anyone.

## Retention, access and deletion

The Camlane developers hold no data about you, so there is nothing for us to give you, correct or delete. To remove everything Camlane stores locally, clear the app's data or uninstall it on Android, and delete the desktop config directory (`~/.config/camlane`, `%APPDATA%\camlane` or `~/Library/Application Support/camlane`). For data collected by Google through ads, use Google's controls linked above.

## Security

Version 1 of the streaming protocol is not encrypted. It is meant for networks you trust. Pairing uses a PIN that is never transmitted. See the [security policy](https://github.com/aryan0078/camlane/blob/main/SECURITY.md) for the full threat model.

## Changes to this policy

When this policy changes, the effective date above is updated. The full history is visible in the repository's git log, and material changes are noted in the [changelog](https://github.com/aryan0078/camlane/blob/main/CHANGELOG.md) and release notes.

## Contact

- Questions: [open a GitHub issue](https://github.com/aryan0078/camlane/issues).
- Sensitive or private reports: [GitHub Security Advisories](https://github.com/aryan0078/camlane/security/advisories/new), or email the maintainer at the address on the GitHub profile [@aryan0078](https://github.com/aryan0078).

Maintainer: Aryan Singh.
