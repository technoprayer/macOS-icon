# Instructions

**TODO:** Is Photoshop's **Save As...** the best method for creating the different size/resolution combinations for the icon? Could `ffmpeg` do this more quickly?

1. Use the `icon_562x562@2x.png` sample to create the new folder design

	Note: the background of the folder icon isn't "light blue", it's actually the same "textured" light blue from the rest of the folder; you can use Photoshop's **Clone** tool to generate this textured effect

2. **Save As...** a `.png` file for all of the following image sizes / resolutions:

	| File Name		| Size (Pixels)	| Resolution (PPI)	|
	| --------------------- | ------------: | --------------------: |
	| icon_512x512@2x.png	| 1024x1024	| 144 			|
	| icon_256x256@2x.png	| 512x512	| 144 			|
	| icon_128x128@2x.png	| 256x256	| 144 			|
	| icon_32x32@2x.png	| 64x64		| 144 			|
	| icon_16x16@2x.png	| 32x32		| 144 			|
	| icon_512x512.png	| 512x512	| 72 			|
	| icon_256x256.png	| 256x256 	| 72 			|
	| icon_128x128.png	| 128x128 	| 72 			|
	| icon_32x32.png	| 32x32 	| 72 			|
	| icon_16x16.png	| 16x16 	| 72 			|

	Note: It's **very important** that the file names are *exactly* as noted above; the file name will *not* match the size of the image in pixels for the 144 (2x) variants, but macOS will know what to do with each, nonetheless; you should have 10 `.png` files in total

3. Now that you have 10 separate `.png` files with all of the correct sizes and resolutions, you need to build a new `.iconset` file (folder); to do this, simply group all of the images inside of a folder and name it

	`<name>.iconset`

	You'll be asked if you want to add the extension `.iconset` to the folder — yes, add it.

4. Use the `iconutil` command to generate the `.icns` file from the `.iconset` folder:

	`> iconutil -c icns <name>.iconset`

5. Finally, open the target folder's **Get Info** window, and *drag* the newly created `.icns` file onto the folder icon preview.