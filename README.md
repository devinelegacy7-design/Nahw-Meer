# Nahw Mir App — GitHub + Codemagic se APK banane ka tareeqa

## Files ka maqsad
- `www/index.html` — aapki app (search + copy wala demo)
- `package.json` — Capacitor ki dependencies
- `capacitor.config.json` — app ki settings (naam, ID)
- `codemagic.yaml` — Codemagic ko batata hai APK kaise banana hai
- `.gitignore` — extra files GitHub pe upload hone se rokta hai

---

## Step 1: GitHub pe Repository banayein
1. github.com pe login karein (ya account banayein — free hai)
2. Upar right corner "+" button > "New repository"
3. Naam dein: `nahw-mir-app`
4. "Create repository" dabayein

## Step 2: Files Upload karein
1. Nayi repository ke page pe "uploading an existing file" wala link dikhega — us par click karein
2. Is zip mein se saari files (sub-folders sameet) drag-and-drop karein
   - Zaroori: `www` folder poora upload hona chahiye (index.html sameet)
3. Neeche "Commit changes" button dabayein

## Step 3: Codemagic Account banayein
1. codemagic.io par jayein
2. "Sign up" > GitHub account se sign up karein (sabse asaan tareeqa)
3. Permission dein taake Codemagic aapki repositories dekh sake

## Step 4: App Add karein
1. Codemagic dashboard pe "Add application" dabayein
2. GitHub select karein, phir `nahw-mir-app` repository choose karein
3. Codemagic khud `codemagic.yaml` file detect kar lega

## Step 5: Build Start karein
1. Workflow "android-debug-apk" select hoga (already configured)
2. "Start new build" dabayein
3. 5-10 minute intezar karein (cloud mein build ho raha hoga, aapke laptop pe kuch load nahi)

## Step 6: APK Download karein
1. Build complete hone par "Artifacts" section mein `.apk` file ka link milega
2. Wo file download kar ke apne Android phone pe bhej dein (WhatsApp, USB, ya Google Drive se)
3. Phone pe file open karein — pehli dafa "Install from unknown sources" allow karna hoga (Settings mein permission mangega, "Allow" kar dein)
4. App install ho jayegi, khol kar test karein

---

## Agar build fail ho (error aaye)
Codemagic build ka poora "log" dikhata hai — jahan error aaye, uska screenshot mujhe bhej dein, main fix kar dunga.

## Zaroori note
Ye abhi ek **debug APK** hai (sirf testing ke liye). Play Store pe publish karne se pehle ek "signed release APK/AAB" banani hoti hai — jab aap us stage par pahunchein, main aapko wo process bhi guide karunga (signing key banana, waghera).
