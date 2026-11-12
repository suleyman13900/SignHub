# SignHub

A simple web interface for signing and installing iOS applications.

SignHub provides a straightforward way to upload an IPA file, add your signing certificate and provisioning profile, and prepare the app for installation on an iPhone.

## Features

- **Import IPA** – Upload the iOS application you want to sign.
- **Import certificate** – Provide your `.p12` signing certificate.
- **Provisioning profile** – Upload the matching `.mobileprovision` file.
- **Sign & Install** – Start the signing process and receive an installation link.

## Requirements

To sign and install an iOS application, you need:

- An `.ipa` application file.
- A valid Apple signing certificate (`.p12`).
- The password for your certificate.
- A matching provisioning profile (`.mobileprovision`).
- A configured signing backend.

## How it works

1. Open SignHub in your browser.
2. Select the IPA file you want to install.
3. Upload your signing certificate.
4. Enter the certificate password.
5. Upload the provisioning profile.
6. Press **Sign & Install**.
7. Open the generated installation link on your iPhone.

## Backend

SignHub uses a backend to handle the actual IPA signing process. The frontend communicates with the backend through the `/api/sign` endpoint.

The backend is responsible for signing the IPA and returning an installation URL.

**Note:** The frontend alone does not sign applications. A working signing backend must be configured.

## Security

Signing certificates contain sensitive private-key information. Always use HTTPS and ensure certificate files and passwords are handled securely. Never expose signing credentials in client-side code or public repositories.

## Project

SignHub is designed to keep the signing process simple: upload, sign and install.
