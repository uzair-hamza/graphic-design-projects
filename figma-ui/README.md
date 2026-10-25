# Plant Disease Detector — Mobile App UI (Figma-ready)

UI design for a Plant Disease Detector app, tied to the Plant Disease
Detection ML project (PlantVillage, 38 classes, 94.57% validation
accuracy). Four phone screens, one consistent green/white theme.

## Screens (all 1080×1920)
1. `ui_home.png` — Home. App title "Plant Disease Detector",
   tagline "Snap a leaf, know the disease.", big green
   "Diagnose a Leaf" button, stat cards (38 diseases covered,
   94.6% lab accuracy, 1 photo is all it takes), and a
   "How it works" 3-step list.
2. `ui_camera.png` — Camera/Upload. "Scan a Leaf" title, camera frame
   with corner marks and a leaf placeholder ("Leaf goes here"),
   "Take Photo" button, "Upload from Gallery" button, and the tip
   "Tip: photograph one clear leaf in daylight."
3. `ui_result.png` — Diagnosis Result. Leaf photo area ("Tomato leaf"),
   disease name "Tomato Late Blight", "Confidence: 92%" with a 92%
   progress bar, an Advice card (remove affected leaves, avoid
   wetting leaves, apply a recommended fungicide, check again in
   3 days), and "Save to History" + "Scan Another" buttons.
4. `ui_history.png` — Scan History. Four past scans with leaf thumb,
   disease name, date, and confidence badge:
   Apple Scab 24 Oct 2026 95%, Tomato Late Blight 23 Oct 2026 92%,
   Potato Early Blight 21 Oct 2026 88%, Corn Healthy 20 Oct 2026 99%
   (green badge = healthy, rust badge = diseased).
   Footer note: "4 scans saved on this phone."

## Layout spec (for rebuilding in Figma)
- Frame: 1080×1920 per screen. Side margin: 60 px.
- Status bar: time "9:41" left, battery "100%" right, ~90 px tall.
- Bottom nav bar: y 1760–1920 (160 px tall). Four items, evenly
  spaced (centres x 135, 405, 675, 945): Home, Diagnose, History,
  About. Active item in green, inactive in grey. Nav icon circles
  are 64 px, labels are 30 px bold.
- Cards: white fill, 2 px #DCE4DC border, corner radius 40–48 px.
- Primary button: green fill, height 150 px, corner radius 60 px,
  48 px bold white text. Secondary button: white fill, 4 px green
  outline, same size.
- Stat cards (Home): 300 px wide, 30 px gaps, value 56 px bold,
  label 30 px regular.
- List rows (How it works): height 120 px, gap 30 px.
- History rows: height 220 px, gap 40 px; leaf thumb 120×130 px
  rounded box; confidence badge is a pill (rust #C8501E for
  diseased, green #2E7D32 for healthy), 36 px bold white text.
- Confidence bar (Result): track 960 px wide, 40 px tall, rounded
  20 px, light grey #DCE4DC; fill width = confidence percent.
- Corner radius: cards 40 px, camera frame 48 px, buttons 60 px.

## Colours (hex)
- Primary green: #2E7D32
- Dark green: #1B5E20
- Light green fill: #E8F5E9
- Screen background: #F5F9F5
- Ink (headings/body): #1A1A1A
- Muted text: #646464
- Card border: #DCE4DC
- Leaf green: #4CAF50
- Rust badge (diseased): #C8501E
- White: #FFFFFF

## Fonts
- In Figma use Inter (Bold for headings/buttons, Regular for body).
  These preview renders use DejaVu Sans as the closest font
  available on this machine.
- Sizes: app/screen title 72 px bold, section title 48 px bold,
  body 40 px, small text 36 px, stat value 56 px bold,
  button text 48 px bold, nav label 30 px bold, status bar 36 px.

## How to rebuild in Figma
1. Create 4 frames, 1080×1920, fill #F5F9F5.
2. Create components: StatusBar, BottomNav, PrimaryButton,
   SecondaryButton, Card, StatCard, HistoryRow, ConfidenceBar.
3. Copy the text, colours, sizes, and spacing above into each frame.
4. Replace the drawn leaf placeholders with real leaf photos.
5. Prototype flow: Home Diagnose button → Camera screen →
   Take Photo → Result screen → Save to History → History screen.

## Tools
- Screens drawn entirely with Python (Pillow): flat shapes, cards,
  buttons, and all text. No AI-generated text, no photos, so every
  word is spelled correctly and the layout is exact.
