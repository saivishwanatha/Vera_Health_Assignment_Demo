# Vera Health Assignment Demo

Expo React Native app that streams SSE from the assignment API, renders markdown as it arrives, and turns tagged blocks like `<guideline>` and `<drug>` into collapsible sections. It also shows live SEARCH_STEPS.



## Screenshots

1. Primary streaming view  
   ![Streaming view](docs/I1.jpeg)

2. Collapsible section expanded  
   ![Section expanded](docs/Image1.jpeg)

3. Search steps progress  
   ![Search steps](docs/Image2.jpeg)

4. Final rendered markdown  
   ![Final markdown](docs/Image3.jpeg)

## Demo video

<video src="docs/Demo_video.mp4" controls width="720"></video>

If GitHub does not inline the video due to size, keep this file under 25 MB or link it from a release asset or a short Loom link.

## What this app does

- Connects to  
  `https://vera-assignment-api.vercel.app/api/stream?prompt=<encoded-prompt>`
- Handles both top level `{"type":"STREAM"}` chunks and `{"type":"NodeChunk","content":{"nodeName":"STREAM"}}`
- Parses `<guideline>` and `<drug>` into collapsible cards
- Renders text outside tags as normal markdown
- Displays SEARCH_STEPS with active and done states
- Batches UI updates with requestAnimationFrame for smooth rendering

## Quick start

Requirements

- Node 18 or 20
- Xcode for iOS simulator or Android Studio for emulator

Run

```bash
npm i
npx expo start -c
# press i for iOS or a for Android
