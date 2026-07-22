# ✂️ Easy-Audio-Trimmer

### The world's easiest audio trimmer. No installs. No accounts. No "free trial" that isn't free.

You just want to chop 8 seconds off a voice memo so it fits in a text message. You don't need
a 400MB "professional audio suite" that asks for your email, tries to install a toolbar, and
still slaps a watermark on your file when you're done. You need a page that opens, lets you
drag two little handles, and spits out a clean clip.

That's this.

---

## What it does

- 🎵 Drop in a **WAV or MP3** file
- 🌊 See an actual **waveform**, not just a boring progress bar
- 🖱️ **Drag the start and end handles** right on the waveform (or type exact seconds if you're precise like that)
- ▶️ **Preview your selection** before committing to anything
- 💾 Export as **WAV** (always works) or **MP3** (works once you add one small file — see below)
- 🔒 Runs **100% in your browser**. Your audio never leaves your computer. No upload, no server, no "processing in the cloud," no weird EULA.

Perfect for trimming Suno tracks, voice memos, podcast clips, or that one perfect 15-second
loop for a social media post — without opening a full DAW to do a 5-second job.

---

## How to use it

1. Download `audio-trimmer.html`
2. Double-click it. It opens in your browser. That's the install process. You're done installing.
3. Drop your audio file on the page
4. Drag the yellow handles to where you want your clip to start and end
5. Hit **Trim & Download**
6. Go be a content creator or whatever

No sign-up. No "Pro" tier. No ads. No idea what your file even sounds like, honestly, because
it never gets sent anywhere for anyone to listen to.

---

## About MP3 export (the one asterisk)

Browsers can natively export WAV files with zero extra setup — that part just works.

MP3 is a patented-adjacent format that browsers don't know how to *create* on their own (they can
only play it), so MP3 export needs a small, free, open-source encoder library called `lame.js`.

**One-time setup:**

1. Grab `lame.min.js` from [the lamejs project](https://github.com/zhuker/lamejs) (or via
   [jsDelivr](https://cdn.jsdelivr.net/npm/lamejs@1.2.1/lame.min.js))
2. Drop it in the **same folder** as `audio-trimmer.html`
3. Reload the page. MP3 export now works too.

Don't add it, and the MP3 button just quietly gives you a WAV instead and tells you why.
Nothing breaks, nothing yells at you.

---

## Why this exists

Because "I need to trim an audio file" should not require:
- ❌ Downloading a 2009-era freeware program from a site with 14 popup ads
- ❌ Installing something that also installs three browser extensions you didn't ask for
- ❌ Paying $9.99/month to remove a watermark from a 6-second clip
- ❌ Creating an account to use a feature that used to be a right-click menu option

Your computer can already do this. It just needed someone to build the two-minute tool instead
of the twelve-dollar-a-month one.

---

## Tech notes (for the curious)

- Pure HTML/CSS/JS, zero build step, zero dependencies except the optional MP3 encoder
- Uses the Web Audio API to decode and trim audio in memory
- Waveform is drawn straight to a `<canvas>` from the raw audio samples
- WAV export is hand-rolled PCM encoding (no library needed)
- Works offline once the page (and optionally `lame.min.js`) are saved locally

---

## License

Do whatever you want with it. Trim your audio in peace. 🎧
