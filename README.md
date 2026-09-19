# TillThen — Android download website

**Official tagline:** For everything you want to tell them… later.

This public, static GitHub Pages site is the standalone Android download page for TillThen. The actual Flutter source remains in the [private TillThen repository](https://github.com/abdallahkhayroun00-crypto/TillThen).

## Publish the website

Open **Settings → Pages** in this repository, select **Deploy from a branch**, set **main** and **/(root)**, then Save.

Expected website address after deployment: https://abdallahkhayroun00-crypto.github.io/TillThen-download/

## How the Android download works

The website reads public releases from **this** repository (`TillThen-download`) using the GitHub Releases API. The download button remains disabled until it finds an attached `.apk` asset on a published release, including a prerelease. No APK is stored in the website source tree and the download is **not** available simply because the website is published.

1. Build and test the TillThen Android app in the private source repository. Keep production secrets and signing keys off GitHub.
2. Create a release in **TillThen-download → Releases** and attach a properly signed APK (e.g. `TillThen.apk`). Publish the release.
3. Refresh the published website and check that its download link points to your APK. Verify Android installation on a real test device.

Anyone with the website/release URL may download its APK: this is a **public distribution channel**, not a private beta invite. App upgrades must use the same package ID and signing key and a higher Android version code.

## Brand and privacy

The copied public logo artwork comes from the original TillThen project. The official palette is Deep Midnight `#1F2430`, Warm Ivory `#F6F1EC`, Muted Rose `#B85C7A`, Interactive Rose `#AE4F70`, Soft Gold `#D5B27C`, and Muted Lavender `#7C6F91`. The page uses Cormorant Garamond and Inter where available.

The website's phone/Box illustration is **concept art**, not an actual screenshot or a claim that the app backend is ready. It has no signup form, no email waitlist, no account creation, and no analytics added by this project.

**Never commit** app source code, credentials, user photos/memories, signing keys, service account files, or other private backend data to this public website repository.
