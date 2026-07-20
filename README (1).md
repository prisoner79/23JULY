# 💌 Your Surprise Website — Editing Guide

This is a single self-contained website (`index.html`) with the exact flow from your
reference video, restyled with cute original cartoon cat & dog characters:

1. **Passcode lock screen** — enter a 4-digit code to unlock
2. **Wrong passcode** screen if it doesn't match, with a "Try Again" button
   (animated crying cat & dog)
3. **"I made something special for you 💌"** — Yes / No screen (animated cat &
   dog peeking out of a box)
4. **"Why did you click no 🥺"** screen (loops back if No is pressed — animated
   crying cat & dog)
5. **Virtual hug** — an animated cat & dog hugging, with a "tap to continue" heart
6. **Happy Birthday, love** — an animated cat & dog hugging + a cheek kiss, party hats
7. **Photo memories carousel** — 8 photos of the two of you, auto-playing with a
   moving zoom animation, captions, and background music
8. **Final message screen** — a heartfelt letter where you root for her, with
   confetti hearts and mascots

All the cat/dog characters are original animated cartoon artwork (not copied
from anywhere), so you're free to use and share this however you like.

Everything is in **one file** (`index.html`), so it's easy to open, edit, and share.

---

## 1. Edit the text & password

Open `index.html` in any text editor (Notepad, VS Code, TextEdit — anything works).
Scroll down to the `<script>` section near the bottom and find the block that starts with:

```js
const CONFIG = {
  password: "2307",
  ...
```

Everything inside `CONFIG { ... }` is meant to be edited:

| Setting | What it does |
|---|---|
| `password` | The 4-digit code she'll type to unlock the site |
| `lockHint` | Small hint text under "Enter the passcode" |
| `lockPhoto` | Path to a photo shown on the lock screen (optional) |
| `wrongTitle` / `wrongSub` | Message shown for a wrong passcode |
| `askTitle` / `askSub` | The "I made something special for you" text |
| `noMessages` | List of messages that cycle each time she taps **No** |
| `hugTitle` / `hugSub` | Text on the "Virtual hug" level |
| `birthdayTitle` / `birthdaySub` | Text on the "Happy Birthday, love" level |
| `gifs` | File paths to the 5 animated GIFs (see below) |
| `photos` | Your 8 memory photos + captions (see below) |
| `photoDurationMs` | How long each photo stays on screen (in milliseconds) |
| `song` | Path to your background music file |
| `finalTitle` | Big heading on the last screen |
| `finalLetter` | Your full love letter / message — edit freely, keep line breaks |
| `finalSignoff` | Your sign-off line, e.g. "Forever yours, Prajwal 🐾" |
| `girlfriendName` | Only used for the browser tab title |

**Tip:** don't remove the quotation marks `" "` or commas `,` around each value —
just change the text between the quotes.

---

## 2. The animated GIFs (optional to change)

The `gifs` folder already comes with 5 original animated cartoon cat & dog GIFs,
one for each moment:

| File | Used on |
|---|---|
| `gifs/wrong-passcode.gif` | Wrong passcode screen |
| `gifs/surprise-box.gif` | "I made something special for you" screen |
| `gifs/crying-cat-dog.gif` | Shown every time she taps **No** |
| `gifs/virtual-hug.gif` | The "Virtual hug" level |
| `gifs/birthday-kiss-hug.gif` | The "Happy Birthday, love" level |

These already work out of the box — you don't need to touch them. If you'd
rather use your own GIFs, just replace the file (keep the same filename), or
point `CONFIG.gifs` at a different file. If a GIF file ever goes missing, the
site automatically falls back to a built-in animated illustration instead of
showing a broken image.

## 3. Add your own photos

1. Put your 8 photos inside the `photos` folder next to `index.html`.
2. Name them exactly `1.jpg`, `2.jpg`, `3.jpg` ... `8.jpg`
   *(or edit the `src:` paths in `CONFIG.photos` to match your actual filenames)*
3. Edit each `caption:` line with your own memory/caption.
4. (Optional) Add a photo named `lock-photo.jpg` to `photos/` for the lock screen.

If a photo is missing, the site shows a friendly placeholder telling you exactly
which file to add — so you'll never see a broken image.

## 4. Add your song

Put your song file in the `music` folder and name it `our-song.mp3`
*(or edit `song:` in `CONFIG` to match your filename)*.

> Note: most browsers block music from auto-playing with sound until the user
> interacts with the page. The music will start automatically the moment she
> taps **Yes**, and there's also a 🔈 note button top-right of the photo screen
> she (or you) can tap to turn it on/off manually.

---

## 5. Preview it

Just double-click `index.html` — it opens directly in any browser (Chrome, Safari,
Edge, etc.), no installation needed.

## 6. Send it to her

Pick whichever is easiest:

- **Easiest:** Zip the whole `surprise-website` folder and send it to her — she
  unzips it and double-clicks `index.html`.
- **Nicest (a real link):** Host it for free in ~2 minutes with
  [Netlify Drop](https://app.netlify.com/drop) — just drag the whole folder onto
  the page and it gives you a shareable link instantly.
- Also works great uploaded to **GitHub Pages** or any basic web host.

---

## File structure

```
surprise-website/
├── index.html      ← the whole website (edit CONFIG inside here)
├── gifs/            ← the 5 animated cat & dog GIFs (already included)
├── photos/          ← put 1.jpg ... 8.jpg (+ optional lock-photo.jpg) here
├── music/           ← put our-song.mp3 here
└── README.md        ← this file
```

Have fun making it yours 💕
