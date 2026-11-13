# Mark Dave's Sound Studio (Android + web)

Sound studio (keys, drum pads, beat maker, recorder), Piano Tiles, Piano Teacher and Song Catcher in one app.
Created by Mark Dave.

## One-time setup
1. Create a **public** GitHub repo called `sound-studio` and upload everything in this folder, including `.github`.
2. In the repo, go to **Settings > Pages** and set **Source** to **GitHub Actions**.
3. Open the **Actions** tab. Each run builds the APK, publishes it as a release, and updates the website.

If the Actions tab only shows "Get started", the `.github` folder did not upload (Windows often skips it).
Click **set up a workflow yourself**, name the file `build.yml`, and paste in the contents of
`.github/workflows/build.yml` from this folder.

## Links the QR codes use
- Android app: https://github.com/gnotesamsung7-hue/sound-studio/releases/latest/download/SoundStudio.apk
- Web app: https://gnotesamsung7-hue.github.io/sound-studio/

The QR codes are built into the app for these two links, so keep the repo name `sound-studio`.

## Installing the APK
Scan the Android QR, download the file, and open it. Allow "Install unknown apps" for your browser if Android asks.
Every build is signed with the same key (`app/soundstudio.keystore`), so newer builds install over older ones.

## Changing the app
The whole app is one file: `app/src/main/assets/index.html`. Replace it and commit; the build runs again.

## Song Catcher and the microphone
Song Catcher listens through the microphone and writes down the notes it hears. Android asks for
microphone permission the first time you press **Start listening**. Nothing is recorded or sent anywhere;
the sound is analysed on the phone and only the notes are kept.
