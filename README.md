# ✋ Gesture‑Controlled 3D Particle System (Mobile‑Ready)

A **real‑time, camera‑driven 3D particle system** that runs entirely in the browser using **Three.js + MediaPipe Hands**. Designed to work reliably on **mobile Chrome** (Android / iOS) and deployable directly on **GitHub Pages**.

No build tools. No backend. Just one `index.html`.

## ✨ Features

* 📱 **Mobile‑first** (Chrome, HTTPS)
* 🎥 **Real‑time hand tracking** via MediaPipe
* 🌌 **GPU‑accelerated 3D particles** (Three.js)
* 🤏 **Gesture controls**

  * Move hand → rotate particle system
  * Open / close hand → expand & contract
  * Pinch (thumb + index) → switch particle shapes
* 💖 Multiple particle templates

  * Heart
  * Flower
  * Saturn ring
  * Firework burst
* 🧠 **Robust hand re‑entry handling** (no freezes when hand leaves / re‑enters camera)
* 🌀 Smooth motion with gesture smoothing

---

## 🚀 Live Demo

Once deployed on GitHub Pages:

```
https://afrid2007.github.io/hand-tracking-particles/
```

Open **on mobile Chrome**, allow camera access, tap **START CAMERA**, and show your hand.

## 🛠️ How It Works

### Core Technologies

* **Three.js** → 3D rendering & particles
* **MediaPipe Hands** → real‑time hand landmark tracking
* **WebGL** → GPU acceleration

### Gesture Logic

* Index fingertip controls rotation
* Distance between thumb & index = pinch detection
* Hand visibility state is tracked to safely recover when the hand leaves the camera frame

### Stability Fixes Implemented

* Explicit hand visibility state
* Lost‑frame detection
* Pinch state reset on hand loss
* Motion smoothing to prevent jitter & freezes

These fixes are critical for **mobile reliability**.

## 📂 Project Structure

```
/
├── README.md     # Documentation
└── index.html    # Full application (HTML + JS)
```

## 📦 Deployment (GitHub Pages)

1. Create a GitHub repository
2. Add `index.html` and `README.md`
3. Go to **Settings → Pages**
4. Select branch (usually `main`) and root directory
5. Save
6. Open the provided GitHub Pages URL on mobile Chrome

> ⚠️ Camera access only works on **HTTPS** (GitHub Pages is HTTPS by default)

## ✅ Usage Tips

* Use **front camera**
* Ensure **good lighting**
* Keep your hand fully in frame when re‑entering
* Wait ~0.5s after re‑entering before pinching

## 🔧 Customization Ideas

* Increase particle count for high‑end devices
* Add new mathematical shapes
* Color control via palm openness
* Two‑hand gestures
* Audio‑reactive particles
* Shader‑based morphing

## 🧠 Known Limitations

* Performance depends on device GPU
* Very low‑light environments reduce tracking accuracy
* Safari has lower WebGL performance than Chrome

## 📜 License

MIT License — free to use, modify, and share.

## 🙌 Credits

* Three.js
* Google MediaPipe Hands

Built for experimentation, learning, and creative coding.
