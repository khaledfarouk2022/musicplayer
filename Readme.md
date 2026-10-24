# Music Player

A simple pink-themed music player page built with HTML, CSS and JavaScript. It plays one song, "Sawahna" by Tamer Hosny, with a custom play/pause button and a progress bar.

## Features

- Play and pause the song with the big pink button
- The button shows a play icon when paused and a pause icon while playing
- The icon stays correct even if you use the gray built-in audio controls
- Progress bar that moves as the song plays, and can be dragged to jump to any point
- The icon goes back to play when the song ends

## Built With

- HTML5 (including the `<audio>` element)
- CSS3
- JavaScript (vanilla, no libraries)
- [Font Awesome](https://fontawesome.com/) for the icons, loaded through a kit script

## Project Structure

```
music-player/
├── index.html
├── style.css
├── images/
│   └── Tamer Hosny.jpg
└── Media/
    └── sawahna.mp3
```

## How to Run

1. Download or clone the project.
2. Make sure the `images` and `Media` folders sit next to `index.html`, with the file names shown above.
3. Open `index.html` in your browser.

An internet connection is needed the first time so Font Awesome can load the icons.

## How It Works

- `PlayPause()` checks `song.paused` and calls `song.play()` or `song.pause()`.
- The `onplay` and `onpause` events call `setIcon()`, which rewrites the button's icon. The whole `<i>` tag is replaced, because Font Awesome's kit turns icons into SVGs and changing only the class would not redraw it.
- `ontimeupdate` moves the progress bar, and `oninput` on the bar sets `song.currentTime` so you can seek.

## Known Limitations

- The backward and forward buttons are only visual for now. There is just one song, so they don't do anything yet.
- The menu and back buttons at the top are not connected to anything.

## Ideas for Later

- Add a playlist so the backward and forward buttons switch between songs
- Show the current time and the song's length next to the progress bar
- Add a volume control

## Credits

Song: "Sawahna" by Tamer Hosny. The audio and the photo are used here for learning purposes only, so check the usage rights before publishing the page online.