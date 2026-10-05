# bassmax · sub-bass, but louder

> one html file that makes your car-audio clips hit like the ones that go viral. no install, no account, no upload. your clips never leave your device, mostly because there's nowhere for them to go.

**open it:** https://notarqen.github.io/bassmax/

---

## what it does

drop in a clip (mov, mp4, m4a, wav, mp3). it finds the sub-bass and lets you crank exactly those parts, instead of turning the whole thing into mud.

- auto-detects the sub (under 120 hz) and marks bassmax zones on the waveform. it's usually right. when it isn't, drag your own.
- per-zone intensity from 0 to 200%. 200% is not a suggestion.
- default chain: 25 hz high-pass, +18 db at 60 hz, +8 db at 45, +6 db at 150, saturation, 10:1 compression, normalized to −12 lufs, soft limiter. subtle, it is not.
- live preview with bypass, so you can confirm the original was in fact worse.
- loop, zoom, pan, undo. the usual.
- **export video**: the video track is copied untouched and only the audio is swapped. no re-encode, no quality loss. iphone .mov stays .mov.
- **wav only**: for when you just want the audio.

## on a phone

works on iphone and android, portrait or sideways. in safari, share → add to home screen and it'll pretend to be an app. pinch the timeline to zoom.

"copy video" is mac-only. no phone browser will put a video on the clipboard, so use export.

## heads up

exports keep your camera's metadata, **gps location included** if the clip had it. that's on purpose, it keeps the file looking like an original. it also means posting the export posts where you filmed it. strip it first if you care.

## under the hood

one file, vanilla js. web audio does the processing, webcodecs and [mediabunny](https://mediabunny.dev) (bundled inline, [mpl-2.0](https://www.mozilla.org/MPL/2.0/)) handle the muxing. no build step, no tracking, no network requests at all.

needs a recent browser. if export fails, it's the browser's fault, not yours. probably.
