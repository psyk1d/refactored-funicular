# Reel Framer

A static site that turns any Short or Reel into a 1080x1920 video in the style of hook/meme reels:

1. white background with your hook on top (with an emoji like 😭🤡)
2. the video in an inset box, black or white bars removed automatically
3. your logo, or a looping ad video, underneath

Everything runs in your browser. No uploads, no server, no build step.

## Use it

1. Open the site.
2. Pick your video(s) and your logo. The logo can be a PNG or a video. A logo video loops until the main video ends, so it works as an ad. It is remembered in your browser.
3. Pick a niche, add a short topic and press **Write hooks for my clips**, or type one hook per line, in the same order as the videos. Tap emojis to insert them, or turn on auto-emoji.
4. Check the live preview. Choose Full HD, 2K or 4K and an optional Sharpen level under "Quality and export". Change the font, weight, alignment, box size, or use the size and position sliders. "Reset to reference style" restores the defaults.
5. Click **Render videos** and keep the tab open and visible until it finishes.
6. Press **Save video** on each result. (Inside the Claude app the page asks you to confirm the save. In a normal browser it downloads directly.)

## Put it on GitHub Pages

1. Create a new public repository on GitHub and upload everything in this folder (keep the `.github` folder).
2. Go to **Settings > Pages** and set **Source** to **GitHub Actions**. Every push to `main` then deploys the site.
   (Alternative without Actions: set Source to **Deploy from a branch**, `main`, `/ (root)`.)
3. After a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

You can also just double-click `index.html` to use it locally.

## Notes

- Hooks: inside Claude the page asks Claude to write them while looking at one frame of each clip (you are asked to allow this). Anywhere else it uses built-in niche templates.
- Post captions: press **Write captions and hashtags** to get the text you paste under the post, hashtags included. It is not drawn on the video. Each finished video has copy buttons for the Instagram caption, the YouTube title and the YouTube description (caption plus your links, optional #Shorts).
- Posting: the page cannot sign in to Instagram or YouTube, so you upload yourself. Step 6 (**Links and posting**) holds the links added to the YouTube description and shortcuts to the upload pages.
- 4K needs a fast computer. It cannot add detail the original clip does not have.
- Rendering runs in real time: a 30s video takes about 30s.
- Chrome and Edge export MP4 (H.264 where the browser supports it). Firefox exports WebM.
- The logo's own background (white, black or any plain colour) is removed automatically so it blends into the white. Use the "Make the logo background transparent" option to force white or black, or turn it off.
- Only the main video's audio is kept. The logo video's sound is not used.
- Clips that are already framed (a caption on a white background, with or without a logo) are detected automatically. The picture is cut out and your own hook and logo replace the old ones. Use the **Clip type** menu to force or turn this off.
