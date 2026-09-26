
https://github.com/user-attachments/assets/308a1769-094e-42e1-ae38-2854c6cd1232
# Chest GUI Editor (THIS STILL NEEDS FIXING IM PLANNNG A BIG OVERHAUL OF THIS)

Convert Java resource pack chest GUIs into Bedrock chest screen overlays, and fit them to the chest slots. One HTML file, runs in your browser, nothing is uploaded.

## What it does

- Reads a Java pack (zip or folder) and finds GUI glyphs in font files, language files, and Nexo or ItemsAdder glyph configs.
- Builds Bedrock `ui/chest_screen.json` overlays for chests, ender chests, barrels, shulker boxes and large chests: a title bar plus the chest background. (if applicable)
- Fits each GUI to the chest automatically, with a live preview, drag and nudge editing, and per GUI fit settings.
- Exports a ready to install `.mcpack`.
- Can also open a converted Bedrock pack and edit its overlays.

Textures are never edited. They are only cropped to their artwork, or shown by region.

## Use it (sorry for not inclduing in video but u can disable the slot grids at the top hotbar)

1. Open [GUI Gen](https://wlsgunzz.github.io/Chest-GUI-Generator/) in a browser.
2. Load a Java pack: click **Load pack** or **Load folder**, or drop a zip or folder on the page. If the zip holds several packs, pick one.
3. Check the fit in the preview and adjust anything that looks off.
4. Set the real glyph character for each GUI on the **Trigger** tab if the pack did not assign one.
5. Click **Export pack**.
6. Put in your Geyer Packs or merge with existing packs (make sure there is nothing counteracting)






## Notes

- Nexo and ItemsAdder assign glyph characters at runtime, so packs straight from the download may have none. Those GUIs get a placeholder (U+E200 and up) and a warning. Load the pack your server builds to get the real characters.
- If a pack ships without its images, the tool borrows them from the nearest other pack in the same zip or folder.
- Only chest screens are supported. Anvil, furnace and other screens are skipped.
- Not yet verified in game on every Bedrock and Geyser version. Check one GUI before rolling out.

## Development

The page is a single file: styles, markup, JSZip, and two scripts (pure logic, then the interface). There is no build step for the source.
