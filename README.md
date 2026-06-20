# Live Detection

Real-time object detection and tracking, running entirely in the browser tab — nothing uploaded anywhere.

## Features
- Detection via TensorFlow.js + the pre-trained **coco-ssd** model (80 object classes)
- Works with a live webcam or an uploaded video file
- Custom IoU-based multi-object tracker — a simplified take on SORT's core idea: match each new detection to the closest existing box, keep its ID across frames, age out tracks that disappear, assign new IDs to new objects
- Each detection drawn with a bounding box, class label, confidence score, and a persistent tracking ID (`#3 person 92%`)
- Live object count + FPS readout
- Single HTML file — no install, no build step, no backend

## Run it
Open `index.html` in any modern browser.

**Webcam mode** needs a secure context — works on GitHub Pages (https) or `localhost`, but most browsers block camera access on a plain double-clicked local file. **Video upload mode** works anywhere, no special hosting needed — that's the reliable option for a quick local demo.

## Stack
HTML, CSS, vanilla JS, TensorFlow.js, coco-ssd (loaded via CDN — needs an internet connection on first load to fetch the model).

---
CodeAlpha AI Internship — Task 4: Object Detection and Tracking
