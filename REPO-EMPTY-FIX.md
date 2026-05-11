# Repo Empty? Fix It Here.

**Symptom:** the Mire Sirens Repository installed without errors, but when
you open **Install from repository → Mire Sirens Repository**, you see no
categories or no add-ons.

This is a Kodi caching/initial-fetch quirk, not a problem with the repo
itself. Here's how to get around it.

## Quick fixes to try first

In Kodi, try these in order — one of them usually works:

1. **Settings → Add-ons → Check for updates** — wait 30 seconds, then
open the repo browser again.
2. **Settings → System → Add-ons → Manage dependencies → Mire Sirens
Repository → Disable → Enable**.
3. Force-close Kodi completely and reopen it. Then check the repo
browser again.

If the repo is still empty after all three, use the Downloader workaround
below.

## The Downloader workaround

This installs the repo *directly* from the URL instead of going through
Kodi's built-in zip installer, which sidesteps the empty-repo bug
entirely. Especially reliable on Fire TV and Android TV.

### Step 1 — Install the Downloader app

If you don't already have it, install **Downloader** by AFTVnews from your
device's app store. (It's free.)

### Step 2 — Uninstall the broken repository in Kodi

**Settings → Add-ons → My add-ons → Add-on repository → Mire Sirens
Repository → Uninstall**

Then force-close Kodi and reopen it. This clears any cached state.

### Step 3 — Download the repo zip via Downloader

1. Open **Downloader**
2. Paste/type this URL into the address bar:
   https://isleysharleen.github.io/packages/repository.miresirens/repository.miresirens-1.1.0.zip
  OR IF YOU HAVE TO TYPE USE THIS URL INSTEAD: https://tinyurl.com/43bdwh8a
3. Click **Go**
4. When the download finishes, Downloader will ask if you want to install
the file — say **yes**. This hands the zip to Kodi.

### Step 4 — Install in Kodi

1. **Settings → Add-ons → Install from zip file** → pick the downloaded
zip (you'll have to know where your downloader app downloads on your device as that's where the file will be)
2. Wait for the "Mire Sirens Repository — Add-on installed" notification
3. **Install from repository → Mire Sirens Repository** — the categories
should now appear

### Step 5 — Install the add-ons

Same as the normal install, in this order:

1. **Program add-ons → FENtastical Helper** (install first)
2. **Look and feel → Skin → FENtastical**
3. **Video add-ons → Mire Sirens**

Then switch skin: **Settings → Interface → Skin → FENtastical**.

NOTE - your main path for your FENtastical widgets must be setup first or you will get black screen of death if you dont do this and only create widgets.

## Still stuck?

If the repo browser is *still* empty after the Downloader workaround,
the issue is likely connectivity rather than Kodi caching:

1. Open `https://isleysharleen.github.io/packages/addons.xml` in a browser
on the same network as your Kodi device. You should see XML text. If
you get nothing or a timeout, your network is blocking GitHub Pages.
2. Some VPNs and DNS filters (pi-hole, NextDNS) block GitHub-hosted
content. Try briefly disabling them and reinstalling.
3. As a last resort: uninstall the repository, restart your entire
device (not just Kodi), and try the Downloader install fresh.

