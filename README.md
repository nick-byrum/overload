# Overload

A lift tracker built around rep ranges and progressive overload. It installs on your phone and works offline.

## Put it on your phone (one time, about 10 minutes)

1. On GitHub, create a new **public** repository named `overload`.
2. Click **"uploading an existing file"**, drag in every file from this folder, and commit.
3. Go to **Settings → Pages**. Under "Build and deployment," set Source to **Deploy from a branch**, Branch to **main**, folder **/ (root)**, and save.
4. Wait about a minute. Your app is live at `https://<your-username>.github.io/overload/`.
5. On your Android phone, open that link in **Chrome**, tap the **⋮** menu, then **Add to Home screen → Install**.

It now opens full-screen from its own icon and works with no signal.

## Updating

Replace the files in the repo with new versions. The app picks up the update the next time you open it with internet. Your data isn't affected.

## Your data

Everything is stored on your phone. Use **Library → Settings → Export backup** now and then, and keep the file in Google Drive.

## Google Drive auto-sync (one-time setup, about 10 minutes)

Google requires every app that touches Drive to have its own "client ID". You make one once, for free:

1. Go to https://console.cloud.google.com and create a project called **Overload**.
2. **APIs & Services → Library**: search for **Google Drive API** and click **Enable**.
3. **APIs & Services → OAuth consent screen** (shown as "Google Auth Platform"): click Get started, App name **Overload**, pick your email, Audience **External**, then finish. Under **Audience → Test users**, add your own Gmail address.
4. **Clients → Create client**: Application type **Web application**. Under **Authorized JavaScript origins**, add `https://nick-byrum.github.io`. Create, then copy the **Client ID**.
5. In the app: **Library → Settings → Google Drive sync**. Paste the ID, tap **Save**, then tap **Connect Google Drive**.

Google will warn that the app "hasn't been verified". That's expected because it's your own app: tap **Continue**. The app can only see the one file it creates (`overload-backup.json`), not the rest of your Drive.
