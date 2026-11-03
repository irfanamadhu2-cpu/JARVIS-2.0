# Jarvis (Android)

A voice-and-text AI butler that operates your phone. It looks at the screen, taps, swipes, types, opens apps and
links, and **asks your approval before anything irreversible** (sending, paying, calling, deleting).

Needs Android 11 or newer. Powered by the Claude API (your own API key from console.anthropic.com).

## Get the APK (one time, ~10 minutes, needs a computer)

**Option A - GitHub (no coding)**
1. Make a free account at github.com, click **New repository** (private is fine), name it `jarvis`.
2. Click **uploading an existing file** and drag in **everything inside this folder** (including the hidden `.github` folder).
   Commit.
3. Open the **Actions** tab, wait for "Build Jarvis APK" to finish (green tick, ~5 min).
   If it did not start, click it, then **Run workflow**.
4. Open the finished run, scroll to **Artifacts**, download `jarvis-apk`, unzip, and send `app-debug.apk` to your phone.

**Option B - Android Studio**
Open this folder in Android Studio, let it sync, then Build > Build APK(s).

## Install and set up on the phone
1. Open `app-debug.apk`, allow "install unknown apps" when asked, install it.
2. Open Jarvis. Tap **1. Turn on phone control**, find **Jarvis** in the list, turn it on.
   - If Android says "Restricted setting": go to Settings > Apps > Jarvis > top-right menu (three dots) >
     **Allow restricted settings**, then try again.
3. Paste your API key, tap **Save key**.
4. Tell Jarvis what to do (type, or use **Mic: Tamil / Mic: English**). Jarvis goes to the home screen and starts working.

## Safety
- Approve/Reject box appears before sends, payments, calls, orders, deletes. It also appears automatically if Jarvis taps
  a button labelled Send / Pay / Confirm / Delete etc., even if the AI forgets to ask.
- Jarvis refuses to type into password/PIN/OTP fields. It asks you to type them (box with a Done button).
- Red **STOP** button floats on screen while Jarvis works.
- Screenshots of your screen are sent to the Claude API to decide the next step. Don't run it on screens you
  wouldn't want an AI to see.
- Your API key is stored in the app's private storage on your phone.

## Not included yet
Always-listening "Hey Jarvis" wake word (battery + extra permissions), iPhone support.
