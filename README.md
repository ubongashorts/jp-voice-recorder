# jp-voice-recorder

A one-page recorder for collecting native-speaker example sentences for the
**jp-voice** Minecraft mod — a Japanese-learning mod that speaks item, block
and mob names aloud.

The mod already has sentence audio for 248 words. This covers the gap: **287
words**, which between them appear in **629 item names** that currently have
no example sentence at all. The list is ordered by how many names each word
unlocks, so stopping early still helps.

## For the reader

Open the page, choose a folder, allow the microphone, and read each line.

- Nothing is uploaded. Every recording is written straight to the folder you
  chose, on your own machine.
- Recordings are 16-bit WAV so the audio is encoded exactly once, when it is
  converted for the mod — not twice.
- The sentence is editable. If one reads awkwardly, fix it and record what you
  actually said; the text is saved alongside the audio.
- Silence is *suggested*, never cut on its own: the green handles are placed
  where the speech seems to start and end, and you can move them. A hard
  automatic cut clips consonant attacks and devoiced vowels, and Japanese is
  full of both.
- Stop whenever. Reopening the page and choosing the same folder picks up
  where you left off — the files on disk are the progress.

Needs Chrome or Edge, for the folder-writing API.

## What comes back

Alongside the `.wav` files the page writes `manifest.json`:

```json
{"index": 1, "word": "ハーフブロック",
 "sentence": "ハーフブロックを二つ重ねます。",
 "file": "001_ハーフブロック.wav", "names": 68}
```

That is what maps a recording to the word the mod looks it up by, and it
records the sentence as actually read rather than as originally drafted.
