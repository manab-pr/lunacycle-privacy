# LunaCycle Privacy Policy

**Effective date:** 22 September 2026 · **App:** LunaCycle (Android, package `com.manabxd.periodtracker`) · **Developer:** Manab Maity, India · **Contact:** manab2001maity@gmail.com

LunaCycle is a period and cycle tracker built to keep your data on your phone. This policy explains exactly what the app stores, what leaves your device, and how you stay in control.

## 1. The short version

- Everything you log stays in a database inside the app's private storage on your phone. No account is needed.
- LunaCycle contains **no analytics, no advertising, and no tracking SDKs**. We do not collect usage statistics, device identifiers, or crash reports.
- **Cloud backup is optional and off by default.** If you turn it on, your data is encrypted on your phone with a passphrase only you know before it is stored in your Google-authenticated LunaCycle account. Nobody, including the developer, can read it.
- You can export or delete all of your data, and delete your cloud account, from inside the app at any time.

## 2. Data the app stores on your phone

When you use LunaCycle you may record:

- period start and end dates;
- daily entries: flow, mood, symptoms, medicine and contraceptive taken, energy, sleep, appetite and free-text notes;
- preferences: language, theme, cycle and period length, reminder times, discreet mode, and an optional app-lock PIN (stored only as a salted hash) with an optional fingerprint unlock flag.

This information is used solely to show your calendar, predictions and reports on your device. Predictions are estimates based on what you log; LunaCycle is not a medical device and does not replace medical advice.

## 3. Optional cloud backup (Firebase)

If you choose **Backup & Sync → Continue with Google**, the following happens:

- **Authentication.** You sign in with your Google account through Firebase Authentication (a Google LLC service). Firebase receives your Google account identifier, name and email address to create your LunaCycle account. We use these only to identify your backup and to show your name in the app.
- **Encryption before upload.** You choose a backup passphrase. The app derives an encryption key from it on your phone (PBKDF2-HMAC-SHA256, 200,000 iterations) and encrypts every period and daily-log record with AES-256-GCM before uploading. Your passphrase and key never leave your phone. If you forget the passphrase, the backup cannot be recovered by anyone.
- **Storage.** Encrypted records are stored in Cloud Firestore (Google LLC) under a path only your account can access, enforced by server-side security rules. Google encrypts data in transit (TLS) and at rest. Firestore may cache data on your device for offline use; that cache is protected by Android app sandboxing.
- **What is stored:** encrypted period and daily-log records, their timestamps, deletion markers, and a small encrypted verifier used to check your passphrase on a new phone. Preferences, PIN and reminder settings are **not** backed up.
- **Data location.** The Firestore database is hosted in Google's `asia-south1` (Mumbai) region.

You can turn backup off, sign out, or delete the cloud copy at any time (see section 6).

## 4. Data we never collect

No analytics, advertising identifiers, location, contacts, precise device identifiers, or crash logs. The app requests internet access only for the optional backup; without it, the app never connects to any server.

## 5. Permissions

- **Notifications:** for the optional period and daily-log reminders. Reminder text is neutral unless you enable detailed wording.
- **Biometrics:** for the optional fingerprint unlock. Biometric data never leaves the Android system and is not accessible to the app.
- **Internet:** only for the optional cloud backup.
- **Boot completed:** to re-schedule your reminders after a restart.

## 6. Your controls

- **Export:** Reports → Export your data, or Settings → Data, produces CSV or PDF files that you choose where to share.
- **Delete everything on the phone:** Settings → Data → Delete all data. If backup is on, the cloud copy is deleted as well.
- **Delete your cloud account:** Backup & Sync → Delete from the cloud removes all of your backup data and your Firebase account. You can also request deletion by emailing manab2001maity@gmail.com from the Google address you signed in with; we will delete the account and data within 30 days.
- **Sign out:** keeps everything on your phone and stops any synchronisation.

## 7. Children

LunaCycle is intended for people aged 13 and over. We do not knowingly collect data from children under 13; the app has no way to do so because it collects nothing without the optional backup, which requires a Google account.

## 8. Sharing and third parties

We do not sell, rent or share your data. The only third party involved is Google LLC as the infrastructure provider for Firebase Authentication and Cloud Firestore, and only if you enable backup. Google processes this data under the [Firebase terms](https://firebase.google.com/terms) and the [Google Privacy Policy](https://policies.google.com/privacy). Because your records are encrypted with your passphrase, Google and the developer see only ciphertext.

## 9. Security

Local data lives in the app's private storage protected by Android's app sandbox, with an optional PIN or fingerprint lock. Backup data is encrypted end-to-end as described above. No system is perfectly secure; keep your device and passphrase safe.

## 10. Changes

If this policy changes, the new version will be published at the same address and the effective date updated. Material changes to how backup works will be announced inside the app.

## 11. Contact

Questions or deletion requests: manab2001maity@gmail.com
