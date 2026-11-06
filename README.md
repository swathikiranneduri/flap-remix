# Flap Remix — Telugu Meme Edition

A static browser game: watch the intro, tap to fly, and get a Telugu meme reaction when the round ends.

- Intro video before each round, with skip and disable controls.
- Tap/click, Space or Arrow Up to flap. Double-tap zoom is suppressed within the game area.
- Default transparent photo character; upload a photo for automatic on-device background removal and adjust its size.
- 435 locally archived audio clips: random without immediate repeats, searchable fixed selection, custom upload, volume, and mute.
- Classic Sky, Village Festival, and Balayya Mass scenery; custom backgrounds and obstacles.
- Custom music and flap sounds. Uploaded files remain in the current browser session.

The audio files are packaged into binary collections. Each library entry identifies a byte range; the game fetches only the selected clip with HTTP Range, or slices the collection when a host does not support ranges. No external sound API is needed at runtime.

## Hosting

Serve this directory as static files. No build command or backend is needed. The public game is https://flap-remix.netlify.app/.

For local testing with Node.js, use a static server that supports byte ranges, for example the local preview starter supplied separately with this project.

## Credits

- Audio catalogue: [Telugu Meme Sounds](https://telugumemesounds.com/). These are the 435 unique clips in the local download; the source API did not confirm the catalogue's completeness. Source links are retained in `library.js`.
- Intro video and character photo supplied by the project owner. Default transparent character prepared with the built-in image-generation editor.
- Automatic background removal: [IMG.LY background-removal-js 1.7.0](https://github.com/imgly/background-removal-js), AGPL licensed. The module and model download on first use; photo inference happens in the browser. Source and licensing terms are available in that dependency's repository.

Audio, video, and likeness rights remain with their respective owners; this repository does not grant third-party content rights.
