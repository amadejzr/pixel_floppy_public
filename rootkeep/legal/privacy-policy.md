# Privacy Policy

**Last updated:** July 22, 2026

Amadej Jerlah ("we," "us," or "our") operates the Rootkeep mobile application ("the App"). This Privacy Policy explains how we collect, use, and protect your information when you use the App.

## 1. Information We Collect

### 1.1 Information You Provide

- **Contact information:** Names, email addresses, phone numbers, companies, roles, birthdays, and personal notes about people in your network.
- **Interaction history:** Records of meetings, calls, messages, and other interactions you log, including dates, notes, and follow-up reminders.
- **Goals:** Relationship goals you create and the contacts you link to them.
- **AI conversations:** Messages you exchange with the AI advisor feature.
- **Voice input:** When you dictate, your speech is transcribed by your device's built-in speech recognizer, provided by your operating system.
We do not record your audio to a file, and we never receive it.
- **API key:** If you use the AI advisor, you provide your own Anthropic (Claude) API key.
It is stored securely on your device and is never sent to us.

### 1.2 Information from Your Device

- **Device contacts:** If you choose to import contacts, we access your device's address book with your explicit permission.
The details of the contacts you select (name, phone, email, company, birthday) are copied into the App's on-device database, along with a reference identifier linking back to the address-book entry.
We do not upload your address book.
- **Microphone:** If you use voice input, we access your microphone with your permission so your device's built-in speech recognizer can transcribe what you say. The audio is handled by the operating system; the App does not save it to a file and never receives it.

### 1.3 Information We Do NOT Collect

- Location or GPS data
- Device identifiers or advertising IDs
- Usage analytics or telemetry
- Crash reports (planned for a future release)
- Payment or financial information
- Photos, media, or files
- Browsing history

## 2. How Your Data Is Stored

**Your data lives on your device.** Rootkeep uses an on-device SQLite database as the single source of truth.
We do not operate any server that stores your personal data - there is no Rootkeep account and no Rootkeep-run backend.

On iOS, you may also enable **iCloud backup**, which stores a copy of your data in your own private iCloud account (see Section 3.2).
This is your iCloud, not ours; we never receive or access it.
Its confidentiality is governed by Apple's iCloud encryption and your Apple ID settings, which Section 3.2 explains in full.
On Android, the App is local-only and does not back up to the cloud.

Your API key is stored using your device's secure storage (Keychain on iOS, Keystore on Android), encrypted at rest by the operating system.

## 3. Third-Party Services

Rootkeep sends data to third-party services only when you actively use features that require them, and only with API keys you provide yourself.

### 3.1 Anthropic (Claude API)

The AI advisor runs on your own Anthropic (Claude) API key.
Requests go directly from your device to Anthropic's Claude API; they do not pass through any server we operate, and we never see them.

Before a request leaves your device, the App replaces the identities of the people in your network with opaque handles that only your device can map back, so Anthropic never receives who your contacts actually are:

- **Contact names are replaced** - each contact's name is swapped for a neutral placeholder (for example, "Marko Novak" becomes a code such as "Person 1"), and the AI's replies are translated back to real names on your device after they return. The one exception is a bare first name shared by two or more of your contacts: because we cannot tell which person you mean, that first name may be sent as-is so the AI can ask you to clarify, rather than us masking it as the wrong person.
- **Email addresses and phone numbers are redacted** - detected emails and phone numbers are removed before a request leaves your device, and the AI can neither read nor set them; you manage those details yourself in the App.
- **The AI sees context, not identifiers** - roles, companies, interaction notes, and goals are shared under these placeholders, never with real names or contact details attached.

This handling covers every contact, including anyone mentioned inside your questions, notes, or interaction history.
Anthropic therefore receives your questions and the relevant context under your own API key, with direct identifiers replaced by placeholders.

This **reduces, but does not eliminate,** the personal data that is sent.
Placeholder-masked data is still personal data.
Details the App cannot detect automatically - such as a third party's name written inside a note, or the substance of a note itself - may still be sent.
For this reason we describe this as replacing direct identifiers, not as full anonymization.

Anthropic does not use data submitted through its API to train its models by default.
Anthropic's handling of the data is governed by their [privacy policy](https://www.anthropic.com/privacy) and [API terms](https://www.anthropic.com/api-terms).

### 3.2 Apple iCloud (Backup - iOS only)

If you enable iCloud backup on iOS, the App stores a snapshot of your data in your own private iCloud account, inside a container tied to your Apple ID.
No custom server and no third party holds this data - it lives in your iCloud and counts against your iCloud storage.
We never receive or access it.

The snapshot is protected by Apple's standard iCloud encryption: it is encrypted in transit and encrypted at rest on Apple's servers.
It is end-to-end encrypted, so that not even Apple can read it, only if you have turned on [Advanced Data Protection](https://support.apple.com/en-us/108756) for your Apple ID.
Without Advanced Data Protection, Apple holds the keys and can technically access the data, the same as any file you keep in iCloud Drive.
The App does not add its own layer of encryption on top of Apple's, so the confidentiality of your backup is exactly that of your iCloud account.
Apple's handling of iCloud data is governed by their [privacy policy](https://www.apple.com/legal/privacy/).

### 3.3 Crash Reporting

The App does not currently use any crash-reporting or error-tracking service.
If we add one in the future (for example, Sentry), it will receive only diagnostic information such as an error message, stack trace, device type, and operating system version - never your contacts, interactions, goals, or any personal content you enter into the App.
We will update this Policy before enabling it.

### 3.4 No Other Third Parties

We do not use analytics services, advertising networks, or any other third-party services that receive your data.
Notifications are generated and delivered locally on your device.

## 4. How We Use Your Information

We use the information you provide solely to:

- Display and manage your contacts, interactions, and goals within the App
- Generate AI-powered suggestions and responses (via third-party APIs listed above)
- Send local on-device reminders and nudges
- Display information on iOS home screen widgets (data stays on your device)

We do not sell, rent, or share your personal data with any third party for marketing, advertising, or any purpose other than the services described above.

## 5. Data Retention and Deletion

Since all data is stored locally on your device:

- **Delete individual records:** You can delete any contact, interaction, goal, or conversation within the App.
- **Delete all data:** Use Settings → Data → Delete All Data to erase everything on your device, together with any iCloud backups the App created (see Section 3.2).
- **Clear AI conversations:** Use Settings → AI Advisor → Clear Conversations.
- **Remove API keys:** Remove your keys in Settings → AI Advisor.
- **Export your data:** Use Settings → Data → Export Data to share a copy of your database with any app or destination you choose.
- **Uninstall:** Deleting the App removes all locally stored data.
  One exception is the API key you entered: iOS keeps Keychain items after an app is deleted, so the key stays in your device's Keychain.
  Rootkeep erases it automatically the first time the App runs again, and you can remove it yourself at any time in Settings → AI Advisor.

We have no server-side data to delete because we do not store your data on any server.

## 6. Children's Privacy

Rootkeep is not directed at children under the age of 13 (or the applicable age in your jurisdiction). We do not knowingly collect personal information from children. If you believe a child has provided us with personal information, please contact us so we can delete it.

## 7. Data Security

We take reasonable measures to protect your data:

- All data is stored locally on your device, protected by your device's security (passcode, biometrics)
- API keys are stored in the device's secure enclave (iOS Keychain / Android Keystore)
- Communication with third-party APIs uses HTTPS/TLS encryption in transit
- iCloud backups (if you enable them) rely on Apple's iCloud encryption, and are end-to-end encrypted when you turn on Advanced Data Protection (see Section 3.2)
- We do not transmit data to our own servers

No method of storage or transmission is 100% secure. We cannot guarantee absolute security, but we minimize risk by keeping your data on your device.

## 8. Your Rights

Depending on your jurisdiction (including under the GDPR, UK GDPR, or CCPA), you may have the right to:

- **Access** your personal data — all your data is visible in the App at all times
- **Delete** your data — see Section 5 above
- **Port** your data — use Settings → Data → Export Data to get a copy of your database file, which you can save or move anywhere you like
- **Restrict processing** — you can stop using AI features at any time by removing your API keys
- **Withdraw consent** — you can revoke device permissions (contacts, microphone) in your device settings

Since we do not store your data on our servers, most of these rights are exercised directly through the App or your device settings. If you have questions, contact us at the address below.

## 9. Changes to This Policy

We may update this Privacy Policy from time to time. We will notify you of material changes by updating the "Last updated" date at the top and, where feasible, through an in-app notice. Continued use of the App after changes constitutes acceptance of the updated policy.

## 10. Future Features

On iOS, backup to your own private iCloud is available today, as described in Section 3.2.
We may add live multi-device sync and other features in a future release.
When we do, this Privacy Policy will be updated to reflect any new data collection, storage, or processing, and any such sync will remain within your own iCloud account rather than a server we operate.

## 11. Contact Us

If you have questions about this Privacy Policy, contact us at:

**Amadej Jerlah**
Email: amadej@jerlah.si
