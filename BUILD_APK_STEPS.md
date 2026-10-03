# Vedic Quotation - APK banane ke steps

## Method A (RECOMMENDED, PC pe kuch install nahi karna): GitHub Actions
1. github.com par naya repo banao (e.g. `vedic-quotation`).
2. Is zip ke andar ke SAARE files/folders (www/, .github/, package.json, capacitor.config.json, .gitignore) repo me upload karo
   (Add file > Upload files; `.github` folder bhi upload hona chahiye).
3. Repo > Actions tab > "Build Android APK" > "Run workflow" > Run workflow (green button).
4. 5-8 min baad run complete hone par us run par click karo > neeche "Artifacts" me `Vedic-Quotation-APK` download karo.
5. Zip kholo -> `app-debug.apk`. Phone me bhejo, install karo (Settings > "Install unknown apps" allow karna padega).

## Method B: Android Studio (local)
1. Node 18+ aur Android Studio install karo.
2. Zip folder me terminal kholo:
   npm install
   npx cap add android
   npx cap sync android
   npx cap open android
3. Android Studio > Build > Build Bundle(s)/APK(s) > Build APK(s).
4. "locate" par click -> android/app/build/outputs/apk/debug/app-debug.apk

## Method C: PWABuilder (hosting chahiye)
1. www/ folder ko Netlify/GitHub Pages par host karo (HTTPS zaroori).
2. pwabuilder.com > URL daalo > Package for stores > Android > Generate > Download.

## Notes
- Installed APK me PDF button Android Share sheet kholta hai (Save to Files / WhatsApp / Drive).
- Release (Play Store) APK ke liye keystore se sign karna padega; personal use ke liye debug APK kaafi hai.
- Company/bank details index.html me "Our Details" aur buildQuotHTML() ke andar editable hain.
