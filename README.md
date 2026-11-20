# ClipForge

A free, local-first alternative to paid AI clipping tools. Import a video or record your screen, trim and reorder clips, add captions, reframe for social formats, and export without an account, credits, watermark, cloud upload, or subscription.

## What it does

- **Import, paste, or record** MP4/WebM/MOV and other browser-decodable videos, **YouTube links** (including 8–9 hour uploads), direct `.mp4`/`.webm` URLs, or a screen/tab/window with optional microphone audio.
- **Generate viral clip candidates** inside the editor from a long video: ranked, scored, 0–30 second windows based on caption hooks, impact words, speech density, and audio-energy peaks. Hinglish captions can be added with **Auto-caption** or SRT/VTT import and stay editable.
- **Edit clips** by trimming source in/out points, splitting at the playhead, duplicating, reordering, and deleting.
- **Find highlights locally** using deterministic heuristics: no API key, no model download, no usage meter.
- **Captions** with manual editing, SRT/VTT import, automatic mapping from source time to the edited timeline, and SRT export.
- **Reframe** to 9:16, 16:9, or 1:1 with zoom, black/blur/gradient backgrounds, and styled captions.
- **Export** through browser-native canvas + MediaRecorder to WebM, or MP4 where the browser supports it. No watermark and no expiry.
- **Publish** rendered clips directly to connected **YouTube** or **Instagram Reels** accounts from the editor (one click after setup), using your own API credentials.
- **Local library** stored in IndexedDB, including the original media blobs.

## Quick start

Requirements:

- Node.js 20.19+ or 22.12+
- A Chromium-based browser is recommended (Chrome/Edge) for the broadest MediaRecorder and screen-capture support.
- FFmpeg is **required for some YouTube imports**: modern YouTube often serves video and audio as separate streams, and active live capture needs FFmpeg to stop after 30 seconds. **Fast** mode prefers a single progressive file when one exists. Direct file import and recording do not need FFmpeg.

```powershell
cd free-clip-studio
npm install
npm run dev
