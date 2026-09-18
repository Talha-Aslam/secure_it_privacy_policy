# Privacy Policy for Secure It

**Last updated:** 18 September 2026
**Applies to:** Secure It (Android package `com.talha.secure_it`)

## Summary

Secure It is a local-first, zero-knowledge password manager. Your vault is
encrypted on your device with a key derived from your master password. We
operate no servers, and we never receive, store, or have any ability to read
your passwords, your master password, or your recovery phrase.

## The data Secure It stores on your device

All of the following stays on your device unless you explicitly turn on
Google Drive sync or export a file yourself:

- **Vault entries** — the service names, usernames, passwords, categories
  and notes you add. These are stored only inside an encrypted vault file
  (`vault.enc`) in the app's private storage.
- **Your master password** — never stored anywhere in any form. Only a
  value derived from it (Argon2id) is used to unwrap your vault's
  encryption key, and that derivation cannot be reversed.
- **Your recovery phrase** — never stored. It is shown to you once, and
  only its effect (a second wrapped copy of your vault key) is saved.
- **App preferences** — non-secret settings such as your light/dark theme
  choice.
- **Optional biometric unlock** — if you enable it, your master password is
  placed in the operating system's own secure storage (Android Keystore) so
  a fingerprint check can retrieve it instead of you retyping it. It never
  leaves the device.

Secure It does not collect analytics, advertising identifiers, crash
telemetry, location, contacts, or any device identifier.

## Google Drive sync (optional, off by default)

If you choose to link a Google account:

- Secure It requests only the `drive.file` and `userinfo.email` scopes.
  `drive.file` restricts the app to files it creates itself — it cannot see,
  read, or browse any other file in your Google Drive. `userinfo.email` is
  used solely to display which account is linked.
- The only file created is `vault.enc`: the same encrypted blob stored
  locally. It is encrypted on your device before upload and decrypted only
  on your devices. Google stores the encrypted file; Google cannot decrypt
  it, and neither can we.
- Your master password and recovery phrase are never uploaded.
- Data handled here is governed by
  [Google's Privacy Policy](https://policies.google.com/privacy) while it is
  at rest in your Drive account.

Unlink at any time from within the app. Deleting `vault.enc` from your
Google Drive removes the synced copy.

## Exports you create

"Backup Vault" and the "Emergency Kit" PDF produce files at your request and
hand them to your device's share sheet or file picker. Where those files go
is entirely your choice. **The Emergency Kit contains your recovery phrase
in plain text** — treat it as you would a key to a safe. We never see these
files.

## Clipboard

Passwords you copy are placed on the system clipboard, flagged sensitive so
Android does not display them in its clipboard preview, and automatically
cleared after 45 seconds if you have not copied something else since.

## Data sharing

Secure It contains no advertising SDKs, no analytics SDKs, and no third-party
trackers. No data is sold or shared with anyone. The only network
destination the app ever contacts is Google's own APIs, and only when you
have linked Google Drive.

## Data deletion

Uninstalling Secure It removes the vault and all app data from your device.
To remove synced data, delete `vault.enc` from your Google Drive and revoke
the app's access at
[myaccount.google.com/permissions](https://myaccount.google.com/permissions).

Because we hold no data about you, there is no account to delete and no
server-side deletion request to make.

## Children

Secure It is not directed at children under 13 and collects no data from
anyone.

## A note on what zero-knowledge means for you

Because we never hold your master password or recovery phrase, **we cannot
recover your vault if you lose both.** This is the deliberate trade-off that
makes the design safe. Keep your Emergency Kit somewhere secure.

## Changes

Material changes to this policy will be published at this URL and reflected
in the "Last updated" date above.

## Contact

Questions about this policy: **talha@otsys.co**
