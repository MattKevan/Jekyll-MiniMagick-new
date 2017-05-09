# Jekyll MiniMagick new
MiniMagick integration for Jekyll

This is an updated and working version of [zroger's Ruby Gem](https://github.com/zroger/jekyll-minimagick), integrating new features and bugfixes from pull requests and the issue queue which haven't yet made their way back into the code.

Put the file in your `_plugins` folder and add the jekyll-minimagick dependency to your config. You'll also need ImageMagick itself.

Presets are defined in `_config.yml` like so:

```
mini_magick:
    thumbnail: # Preset name
        source: images/originals # source directory - change this to whatever you want
        destination: images/thumbnail # generated destination directory
        resize: "100x70^" # standard imagemagick options - you can chain multiple commands
        gravity: "center"
        extent: "100x70"
```

This will scale and crop all images in `images/originals` to 100x70 pixels and save them into `_site/images/thumbnail` on build.

See [here](https://www.kevan.tv/2016/10/17/automatic-image-resizing-with-jekyll-and-imagemagick.html) for full instructions
