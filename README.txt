GRIDLOCK CITY - ANDROID PACKAGE
================================

Files: index.html (the game), manifest.json, sw.js (offline), 4 icon PNGs.
Keep all files together in ONE folder, no sub-folders.

STEP 1 - Put the files on the web (free, one time)
--------------------------------------------------
Easiest from a phone: GitHub Pages
  1. Make a free account at github.com.
  2. Create a PUBLIC repository named  YOURNAME.github.io  (replace YOURNAME with your username).
  3. Add file > Upload files. Select every file from this package (unzip it first).
     Include the hidden file .nojekyll if your file manager shows it.
  4. Commit. Wait 1-2 minutes. Your game is now at  https://YOURNAME.github.io/
From a computer: drag the unzipped folder onto  app.netlify.com/drop  and you get a link at once.

STEP 2A - Install it as an app (fastest, no APK)
------------------------------------------------
Open your link in Chrome on the phone. Menu (three dots) > "Install app" (or "Add to Home screen").
You get a Gridlock icon that opens full screen, landscape, and works offline after the first run.
The first run needs internet once so the fonts get saved.

STEP 2B - Make a real APK file (no Android Studio)
--------------------------------------------------
  1. Go to  pwabuilder.com  and paste your link. Press Start.
  2. Press "Package for stores", choose Android, then Generate. Choose "New" for the signing key.
  3. Download the zip it makes. Inside is the APK. Copy it to the phone and open it.
     Allow "install unknown apps" for your file manager when Android asks.
  4. Keep the signing key file the zip gives you. You need it for future updates.
  Optional: PWABuilder also gives an assetlinks.json file. Upload it to your site as
  .well-known/assetlinks.json (GitHub: Add file > Create new file, type the name with the slash).
  That removes the thin browser bar at the top of the APK.

UPDATING THE GAME
-----------------
Replace index.html in the repository. Then change the version name in sw.js
(CACHE = 'gridlock-v3' to 'gridlock-v4') so phones fetch the new version.

SAVE DATA
---------
The game saves in the phone's browser storage after each mission and at safehouses.
Clearing app data or uninstalling deletes the save.
