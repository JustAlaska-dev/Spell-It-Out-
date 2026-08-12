# 🔊 Spell It Out

A volume control that only understands words. Type `45` and nothing happens — type `forty-five` and the dial sweeps, a synthesized ambient drone fades in, and a nebula blooms behind it.

**[Live demo →](https://justalaska-dev.github.io/Spell-It-Out-/)**



<img width="800" height="434" alt="ScreenRecording2026-08-12121034-ezgif com-video-to-gif-converter" src="https://github.com/user-attachments/assets/75c8b2e9-9366-44a7-839f-f3202094d8c8" />


## Why I built this

Volume sliders are everywhere and nobody thinks twice about them. I wanted to build something that takes a completely mundane interaction and makes you actually stop and think about it — you can't just drag a thumb across a track, you have to spell out what you want. It's a small, self-contained idea, but it let me dig into a few things I wanted more practice with: parsing natural language input, the Web Audio API, and canvas animation.

## How it works

- Type a number as an English word (`zero` through `one hundred`) into the input field
- A parser converts the word into a number — anything else (digits, typos, unsupported words) is rejected with feedback
- The dial animates to that value, an ambient space drone (built entirely with oscillators and filtered noise — no audio files) fades to match the volume, and a nebula glow behind the dial brightens

## Tech stack

- Vanilla HTML, CSS, and JavaScript — no frameworks, no build step
- Web Audio API for the synthesized ambient sound (oscillators, biquad filters, an LFO, and a noise buffer)
- Canvas 2D for the animated starfield/nebula background
- Hosted with GitHub Pages

## Running it locally

No install needed — it's a single HTML file.

1. Clone or download this repo
2. Open `index.html` in any modern browser
3. Click anywhere once (browsers require a user interaction before audio can play)

## Notes on the code

The JavaScript is broken into labeled sections (word-to-number parser, starfield/nebula canvas, ambient audio synthesis, dial rendering) with comments explaining what each part does, so it's readable top to bottom even without prior context.
