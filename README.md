# BGMI Squad Picker

A tiny, one-page tool for picking a fair squad for game night. Tap one button, get four names, share the result card in your group chat.

It is a single `index.html` file. No build step, no dependencies, no account, no server.

## What it does

- **Pick today's squad**: chooses 4 players from your list.
- **Fair turns**: it counts how many times each player has been picked and always favours the people with the fewest turns. Ties are broken with a secure random shuffle (`crypto.getRandomValues`), so the result is unpredictable but nobody gets picked more than everyone else.
- **Share card**: draws a clean image of the squad and the bench. "Share on WhatsApp" copies the image and opens WhatsApp with the squad typed out as text. You can also press and hold the image to save or share it.
- **Players**: add a name, tap a name to rename it, tap × to remove it. A new player starts level with the others, not ahead or behind.

## Use it

Open `index.html` in any modern browser, or host the folder on any static host (for example GitHub Pages: repo Settings, Pages, deploy from the `main` branch).

## Good to know

- Your player list and turn counts are saved in your own browser (`localStorage`). They are not shared between phones or people. For the fair-turn counting to work, use it from the same browser each time.
- The default player names are examples. Change them in the list.
- Image copy needs a secure page (`https://` or a local file) and a browser that supports copying images to the clipboard. If it does not work, press and hold the card image instead.

## Customise

The default players are at the top of the script (`var players = [...]`) and the squad size is `SIZE`. The card is drawn on a `<canvas>` in the `poster()` function, so colours, fonts and layout are easy to change.

## Disclaimer

This is an unofficial fan-made tool for friends playing together. It is not affiliated with or endorsed by Krafton, PUBG Studios or any game publisher. All game names belong to their owners. The icons on the card (parachute and crosshair) are original drawings.

## License

MIT. See [LICENSE](LICENSE).
