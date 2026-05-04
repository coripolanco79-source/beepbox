# BeepBox v3.0.13

BeepBox is an online tool for sketching and sharing instrumental melodies. Try it out [here](https://www.beepbox.co)!

All song data is packaged into the URL at the top of your browser. When you make changes to the song, the URL is updated to reflect your changes. When you are satisfied with your song, just copy and paste the URL to save and share your song!

BeepBox is a passion project, and will always be free to use. If you find it valuable and have the means, any gratuity via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=QZJTX9GRYEV9N&currency_code=USD) would be appreciated!

BeepBox is developed by [John Nesky](https://johnnesky.com/). This source code is available under the [MIT license](LICENSE.md).

## Features

- 🎵 Compose chiptune music directly in your browser
- 🔗 Share songs via URL - all song data is in the URL hash
- 🎛️ Synthesizer with multiple instruments
- 📱 Responsive design
- 🎹 Keyboard shortcuts for efficient composition
- 💾 Auto-save to URL
- 🔊 Real-time audio playback

## Synthesizer Library

You can use BeepBox's synthesizer to play music in your own web app! See [the npm package](https://www.npmjs.com/package/beepbox) for more details.

### Using the Synthesizer in Your Project

```html
<script type="module">
	import { Synth } from "https://cdn.jsdelivr.net/npm/beepbox/esm/synth/index.js";
	
	const synth = new Synth("#9n30sbk7l00e00t2-a7g00j00r1i0o443T0v2u00f0qw02d03w2h0E0T0v2u00f0qw02d03w2h0E0T0v0u00f0qw02d03w1h0E0bUp1OFEYtghQ4sBihS7dQQuwE8W2eywzwPbGcKCzZk4t17hghQCngpo");
	
	document.getElementById("playButton").addEventListener("click", event => {
		if (synth.isPlaying()) {
			synth.pause();
		} else {
			synth.play();
		}
	});
</script>
```

## Compiling

The code is written in TypeScript, which requires Node & npm so [install those first](https://nodejs.org/en/download). To contribute changes, you'll also need [git](https://github.com/git-guides/install-git). Then to build this project, open the command line and run:

```bash
git clone https://github.com/coripolanco79-source/beepbox.git
cd beepbox
npm install
npm run build
```

## Build Commands

### Build All Components
```bash
npm run build
```

### Build Individual Components

Build just the synth library:
```bash
npm run build-synth
```

Build just the editor:
```bash
npm run build-editor
```

Build just the player:
```bash
npm run build-player
```

### Development

Live editor with file watching and hot reload:
```bash
npm run live-editor
```

Fast live editor without type checking:
```bash
npm run live-editor-fast-typeless
```

## Project Structure

```
beepbox/
├── src/
│   ├── synth/          # Synthesizer library
│   ├── editor/         # Editor interface
│   ├── player/         # Embedded player
│   └── types/          # TypeScript type definitions
├── website/            # Website files (HTML, CSS)
├── scripts/            # Build scripts
├── dist/               # Compiled output
├── package.json        # Dependencies and scripts
├── tsconfig.json       # TypeScript configuration
└── README.md          # This file
```

## Dependencies

- **TypeScript** - Type-safe JavaScript
- **esbuild** - Fast JavaScript bundler
- **rollup** - Module bundler
- **terser** - JavaScript minifier
- **five-server** - Local development server

## License

BeepBox is released under the [MIT License](LICENSE.md). See the LICENSE.md file for details.

## Contributing

Contributions are welcome! Feel free to:
- Report bugs and issues
- Suggest new features
- Submit pull requests with improvements
- Improve documentation

## Support

For issues, questions, or suggestions, please visit the [GitHub Issues](https://github.com/coripolanco79-source/beepbox/issues) page.

## Changelog

### v3.0.13
- Accurate TypeScript implementation
- Modular architecture with synth, editor, and player components
- Build pipeline with esbuild and rollup
- Development tools with live reloading
- Comprehensive documentation

---

Made with ❤️ by [John Nesky](https://johnnesky.com/) and contributors.
