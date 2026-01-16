# HEIC to JPG Converter Walkthrough 

HEIC Converter to JPG

A secure, client-side batch HEIC to JPG converter with a premium dark-mode aesthetic.

Features Implemented
Client-Side Conversion: Uses heic2any to convert images locally in the browser. No uploads to server.
Batch Processing: Drag and drop multiple files to convert them in sequence.
Premium UI: Glassmorphism design, smooth animations, and responsive layout.
Zip Download: Download converted files individually or all at once as a ZIP archive.

How to Run:
1) Extract it
2) Navigate to the project directory:
cd "Heic Converter"
3) Start the development server:
npm run dev
Open the link shown (usually http://localhost:5173) in your browser.


Logic & Architecture:
Conversion: Uses libheif-js directly to decode HEIC images via WebAssembly.
WASM Loading: WASM files are served from /public and loaded via a custom factory configuration to avoid path issues.
State Management: App.jsx handles the queue and updates file status (pending -> converting -> done).
Styling: index.css defines CSS variables for a consistent dark theme.
Future Improvements
Web Worker integration for non-blocking UI during heavy conversions.
Custom quality settings slider.
