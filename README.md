# Our Little Universe 🌌

An elegant, interactive single-page web experience built to celebrate meaningful memories, milestones, and personal messages through modern web animations and interactive components.

---

## 📖 Overview

**Our Little Universe** is a lightweight, responsive client-side web application crafted with vanilla HTML5, CSS3, and JavaScript. Designed with aesthetic typography and smooth micro-interactions, the application guides visitors through a multi-stage visual journey starting with a passcode-protected welcome gate and leading into curated memory reels, live milestone counters, interactive note vaults, and embedded audio.

---

## ✨ Features

- **🔐 Passcode Gatekeeper**
  - Pin-protected entry overlay with real-time input verification.
  - Supports numeric keypad input, keyboard Enter handling, and automated authentication upon reaching target code length.
  - Smooth opacity transitions and animated unlock effects upon successful verification.

- **⏱️ Live Milestone Counter**
  - High-precision, real-time timer tracking elapsed days, hours, minutes, and seconds from a designated milestone date.
  - Continuous 1-second interval refresh with synchronized pulsation visual cues.

- **📸 Interactive Memory Gallery**
  - Responsive carousel with navigation controls and dot pagination indicators.
  - Integrated mobile touch-swipe gestures (`touchstart`, `touchend`) with swipe threshold recognition.
  - Image fallback and error-handling states to maintain visual continuity.

- **🫙 Interactive Message Vault (Notes Jar)**
  - Stylized glass jar component utilizing CSS gradients and glassmorphism styling.
  - Interactive click-to-draw interaction with animated jar vibration and floating particle bursts.
  - Modally rendered cards featuring non-repeating message generation and exploration tracking.

- **🎵 Background Audio Engine**
  - Embedded HTML5 audio player supporting seamless looping.
  - Persistent, floating audio control toggle button reflecting live playback state.
  - Automated initial playback trigger coordinated with successful unlock event.

- **✨ Ambient Particle System**
  - Procedural floating particle generator with randomized trajectories, variable velocities, and automated lifecycle management (garbage collection on completion).

---

## 🛠️ Tech Stack

- **Markup:** HTML5 (Semantic Elements, Accessible ARIA Attributes)
- **Styling:** CSS3 (Flexbox, CSS Grid, Glassmorphism, CSS Custom Properties, Keyframe Animations)
- **Scripting:** Vanilla JavaScript (ES6+, DOM Manipulation, Event Handling, Touch Events)
- **Typography:** Google Fonts (*Cormorant Garamond*, *Great Vibes*, *Montserrat*)
- **Dependencies:** None (Zero external libraries or npm packages required)

---

## 📂 Project Structure

```text
our-little-universe/
│
├── index.html                 # Core application markup, styles, and scripts
├── I Love You Too Much.mp3    # Background audio asset
├── photo1.jpg                 # Gallery memory slide 1
├── photo2.jpg                 # Gallery memory slide 2
├── photo3.jpg                 # Gallery memory slide 3
├── photo4.jpg                 # Gallery memory slide 4
└── README.md                  # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

A modern web browser supporting ES6 JavaScript and HTML5 Audio (e.g., Google Chrome, Mozilla Firefox, Apple Safari, Microsoft Edge).

### Running Locally

1. Clone or download the project directory to your local machine.
2. Open `index.html` directly in any web browser:
   - **Double-click** `index.html` in your file explorer, OR
   - Serve using a lightweight static server:
     ```bash
     # Using Python
     python -m http.server 8000

     # Using Node.js (npx)
     npx serve .
     ```
3. Enter the configured passcode to unlock the experience.

---

## ⚙️ Configuration & Customization

All primary configuration options are localized within `index.html`:

### 1. Updating the Passcode
Locate the `secretCode` constant inside the `<script>` section:
```javascript
const secretCode = "13022005"; // Set desired passcode string
```
Adjust the `maxlength` attribute and placeholder dots in the `<input id="code">` element accordingly.

### 2. Adjusting the Milestone Date
Modify the `relationshipStart` timestamp to update the live counter base:
```javascript
const relationshipStart = new Date("2026-05-13T18:13:00");
```

### 3. Modifying Note Vault Messages
Edit the `loveNotes` array to supply personalized messages:
```javascript
const loveNotes = [
    "Message entry 1...",
    "Message entry 2...",
    // Add additional custom strings
];
```

### 4. Replacing Photos and Audio
- Overwrite `photo1.jpg` through `photo4.jpg` in the root folder with desired images (recommended aspect ratio: 3:4 or 4:5 portrait).
- Replace `I Love You Too Much.mp3` with any preferred `.mp3` audio track, ensuring the filename matches the `<source>` tag in `index.html`.

---

## 📱 Browser Compatibility

- Google Chrome (Desktop & Mobile)
- Apple Safari (macOS & iOS)
- Mozilla Firefox
- Microsoft Edge

---

## 📄 License

This project is open for personal use and private celebrations.
