# NexaGuard CMP — GTM Template

This repository contains the official **Google Tag Manager Community Template** for the **NexaGuard Consent Management Platform (CMP)**.

The template enables websites to:

- Apply **Google Consent Mode v2** defaults via GTM consent APIs
- Configure defaults with **global** values plus optional **region override**
- Set Google developer ID automatically (`developer_id.dZTNmYW`, non-editable)
- Optionally load the NexaGuard Web CMP Loader
- Ensure early execution during **Consent Initialization**

This template is intended for GTM users who want to deploy NexaGuard CMP without modifying website code directly.

---

## Current behavior

- Uses `setDefaultConsentState` for consent defaults.
- Uses `updateConsentState` for optional initial updates.
- Supports required consent types:
  - `ad_storage`
  - `analytics_storage`
  - `ad_user_data`
  - `ad_personalization`
- Injects NexaGuard loader script when enabled.
- Passes `data-consent-mode=off` to avoid duplicate default handling by loader.

---

## Main fields

- `settingsId` (required)
- `globalDefaultsJson`
- `regionList` (optional CSV)
- `regionDefaultsJson` (optional JSON)
- `waitForUpdateMs`
- `initialUpdateJson` (optional JSON)
- `loadNXG`, `loaderUrl`, `cdnUrl`, `assetsUrl`

---

## Installation (via GTM Community Template Gallery)

1. Open GTM → **Templates**
2. Click **Search Gallery**
3. Search for **NexaGuard CMP**
4. Add the template to your workspace
5. Create a new Tag → Select **NexaGuard CMP**
6. Enter your **Settings ID**
7. Keep defaults as needed (global + optional region override)
8. Trigger it on **Consent Initialization – All Pages**
9. Validate in Tag Assistant before publishing

---

## Support

For implementation support and documentation, visit:

👉 https://developer.nexaguard.com  
👉 https://nexaguard.com/

---

## License

This project is licensed under **Apache License 2.0**.
