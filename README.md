![Status](https://img.shields.io/badge/status-post--MVP-lightgrey)
![License](https://img.shields.io/badge/license-AGPL--3.0-blue)

# hush-mobile

Mobile application for [Hush](https://gethush.live), an end-to-end encrypted communication platform.

**Status: Planned**

---

## What this will be

hush-mobile is a React Native application with native Rust crypto bindings via UniFFI. Unlike the web client, which uses WASM, the mobile app will link `hush-crypto` directly as a native library for better performance and hardware security module access.

Planned platforms: iOS and Android.

### Key design decisions

| Concern | Approach |
|-|-|
| Crypto bindings | UniFFI (Rust to Kotlin/Swift via generated bindings) |
| UI framework | React Native |
| Key storage | iOS Secure Enclave / Android Keystore via native module |
| Push notifications | Platform-native (APNs / FCM) - notification content is always encrypted |

Push notification payloads will contain only an encrypted routing hint. The notification itself will not reveal sender, guild, or message content.

---

## Roadmap

hush-mobile is planned after the web client and Rust crypto foundations are stable enough to support native mobile bindings. Track progress at [gethush.live](https://gethush.live).

---

## Contributing

This repository is a placeholder. Contributions will be accepted once development begins. Watch this repository for updates.

---

## License

[AGPL-3.0](LICENSE). Modifications to this mobile application must be published under the same license.
