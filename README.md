# Habit Tracker PWA - Installation Guide

## 📱 How to Install on Your Phone

### Option 1: Using a Web Server (Recommended)

1. **Upload all files to a web server:**
   - index.html
   - habit-tracker.jsx
   - manifest.json
   - service-worker.js
   - icon-192.png (you need to create this)
   - icon-512.png (you need to create this)

2. **Open the URL in Safari (iOS) or Chrome (Android)**

3. **Install as PWA:**
   - **iOS/Safari:** Tap Share → "Add to Home Screen"
   - **Android/Chrome:** Tap Menu (⋮) → "Add to Home screen" or "Install app"

### Option 2: Using Python Simple Server (Local Testing)

1. **Put all files in a folder on your computer**

2. **Open Terminal/Command Prompt in that folder**

3. **Start a local server:**
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Or Python 2
   python -m SimpleHTTPServer 8000
   ```

4. **Find your computer's IP address:**
   - macOS/Linux: `ifconfig` or `ip addr`
   - Windows: `ipconfig`
   - Look for something like `192.168.1.x`

5. **On your phone, open browser and go to:**
   ```
   http://YOUR_IP_ADDRESS:8000
   ```
   Example: `http://192.168.1.105:8000`

6. **Install as PWA** (see step 3 above)

### Option 3: Using GitHub Pages (Free Hosting)

1. **Create a GitHub account** (if you don't have one)

2. **Create a new repository** named `habit-tracker`

3. **Upload all files to the repository**

4. **Go to Settings → Pages**

5. **Enable GitHub Pages** (select main branch)

6. **Your app will be live at:**
   ```
   https://YOUR_USERNAME.github.io/habit-tracker
   ```

7. **Open on your phone and install as PWA**

## 🎨 Creating Icons

You need two icon files:
- **icon-192.png** (192x192 pixels)
- **icon-512.png** (512x512 pixels)

### Easy way:
1. Go to https://favicon.io/favicon-generator/
2. Create a simple icon (e.g., checkmark on black background)
3. Download and rename to `icon-192.png` and `icon-512.png`

### Or use the SVG:
- I've included `icon.svg` - you can convert it to PNG using:
  - Online: https://cloudconvert.com/svg-to-png
  - Or any image editor (Photoshop, GIMP, etc.)

## ✅ Features

Once installed:
- ✅ Works offline
- ✅ Looks like a native app
- ✅ No browser UI
- ✅ Data stored locally
- ✅ Fast and responsive
- ✅ Can be on home screen

## 🔧 Troubleshooting

**PWA not installing?**
- Make sure you're using HTTPS (or localhost)
- Check that manifest.json and service-worker.js are accessible
- Icons must be present and correct size

**Data not saving?**
- The app uses Claude's storage API - make sure it's working
- Check browser console for errors

**App not updating?**
- Clear browser cache
- Uninstall and reinstall the PWA

## 📝 Files Included

- `index.html` - Main HTML file
- `habit-tracker.jsx` - React app (your Habit Tracker)
- `manifest.json` - PWA configuration
- `service-worker.js` - Offline functionality
- `icon.svg` - Icon template (convert to PNG)
- `README.md` - This file

Enjoy tracking your habits! 🎯
