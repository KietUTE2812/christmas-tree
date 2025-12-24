# 🎄 Noel Gestures - Interactive Christmas Tree

An immersive 3D gesture-controlled Christmas tree experience built with Three.js and MediaPipe Hands. Created with AI assistance from **Google Gemini 3**.

![Christmas Tree Demo](demo.gif)

## ✨ Features

- **Gesture Control**: Control the Christmas tree with hand gestures
  - ✊ **Fist**: Coalesce particles into tree form
  - 🖐 **Open Palm**: Scatter particles in 3D space
  - 🔄 **Hand Rotation**: Rotate the scene in scatter mode
  - ✌️ **Victory/Thumb Up**: Focus and cycle through photos
  
- **Visual Effects**
  - Cinematic bloom and glow effects
  - 3,500+ instanced particles with dynamic lighting
  - Metallic gold, crimson red, and emerald green color palette
  - Real-time particle animations with smooth state transitions
  
- **Photo Integration**
  - Upload multiple photos to decorate the tree
  - Photos maintain original aspect ratios
  - Automatic dark-toned background with golden frames
  - Dynamic positioning around the tree structure
  
- **Audio Experience**
  - Background music plays when photos are uploaded
  - Smooth fade-in effect (3 seconds)
  - Looping Christmas atmosphere

## 🚀 Quick Start

1. **Clone or download** this repository
2. Place your `music.mp3` file in the same directory as `ms.html`
3. Open `ms.html` in a modern browser (Chrome/Edge recommended)
4. **Allow camera access** when prompted
5. **Upload photos** using the "UPLOAD MEMORIES" button
6. Use **hand gestures** in front of your camera to control the tree

## 🎨 AI Prompt Used

This project was created using **Google Gemini 3** with the following prompt:

### Role Setting:
You are a creative frontend development expert proficient in Three.js, WebGL, and computer vision.

### Task Objective:
Write a single-file application containing HTML, CSS, and JavaScript. The application should combine Three.js and MediaPipe Hands to create a gesture-controlled 3D particle + photo cloud Christmas tree.

### Requirements:

**1. Overall Content:**
- Color scheme: Matte green + metallic gold + Christmas red
- Cinematic bloom and halo effects with a luxurious feel
- Christmas tree composed of spheres, cubes, candy canes, and photo clouds (photos uploaded by users)

**2. Interaction Logic and States:**
- **Tree State (Initial)**: All elements coalesce into a cone-shaped Christmas tree
- **Scattered State**: All elements float and scatter randomly in 3D space
- **Photo Focus State**: Enlarge a single photo while background remains scattered

**3. Gesture Controls:**
- **Closed Fist**: Return to tree state
- **Open Palm**: Enter scattered state
- **Hand Rotation**: Rotate the scene in scattered state based on hand movement
- **Grab Gesture**: Grab and enlarge a photo (focus state)

**4. Interaction Requirements:**
- Smooth transitions between states with animated effects
- Responsive to real-time hand tracking

**5. Technology Stack:**
- Three.js
- WebGL
- Instanced Mesh
- Shaders / GLSL
- MediaPipe Hands

## 🛠️ Technical Stack

- **Three.js** (r160) - 3D rendering engine
- **MediaPipe Hands** - Real-time hand tracking
- **GSAP** - Smooth animations
- **Post-processing**: Bloom effects with UnrealBloomPass
- **Instanced Rendering**: 3,500+ particles with efficient GPU rendering

## 📁 File Structure

```
12.21/
├── ms.html          # Main application (single file)
├── music.mp3        # Background music (user-provided)
└── README.md        # This file
```

## 🎮 Controls

| Gesture | Action |
|---------|--------|
| ✊ Closed Fist | Coalesce into tree form |
| 🖐 Open Palm | Scatter particles |
| 🔄 Hand Movement (in scatter mode) | Rotate scene |
| ✌️ Victory / 👍 Thumb Up | Focus on photo |

## 🎨 Visual Customization

You can customize colors and effects by modifying these constants in the code:

```javascript
const CONF = {
    particleCount: 3500,
    colors: [0x006400, 0xFFC125, 0xDC143C, 0xF0F8FF], // Green, Gold, Red, White
    treeHeight: 25,
    treeRadius: 10,
    scatterRadius: 30
};
```

### Bloom Effect Adjustment:
```javascript
bloomPass.threshold = 0.1;  // Lower = more glow
bloomPass.strength = 2.5;   // Higher = stronger glow
bloomPass.radius = 0.8;     // Glow spread radius
```

## 🔧 Browser Compatibility

- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14.1+ (macOS/iOS)
- ⚠️ Requires camera access
- ⚠️ Works best on desktop/laptop

## 🐛 Troubleshooting

**Problem: Photos appear too bright/washed out**
- Adjust the `color` value in `createPhoto()` function (line ~285)
- Lower values = darker photos (e.g., `0x777777`)

**Problem: Music doesn't play**
- Ensure `music.mp3` is in the same folder
- Check browser console for errors
- Some browsers require user interaction before playing audio

**Problem: Camera not working**
- Grant camera permissions in browser settings
- Check if another application is using the camera
- Try refreshing the page

**Problem: Gesture recognition not accurate**
- Ensure good lighting conditions
- Keep hand clearly visible in the camera preview (bottom-left)
- Try adjusting hand distance from camera

## 📝 License

This project is open source and available for personal and educational use.

## 🙏 Credits

- **AI Assistant**: Google Gemini 3
- **3D Library**: Three.js
- **Hand Tracking**: MediaPipe (Google)
- **Animation**: GSAP
- **Concept**: Interactive gesture-controlled Christmas experience

## 🌟 Future Enhancements

- [ ] Add more particle shapes (stars, snowflakes)
- [ ] Custom gesture recognition for more interactions
- [ ] Photo filters and effects
- [ ] Export/save decorated tree as image
- [ ] Mobile touch controls as fallback
- [ ] Multiple tree themes (winter, spring, etc.)

---

**Made with ❤️ and ✨ AI Magic**

*Powered by Google Gemini 3 | December 2025*
