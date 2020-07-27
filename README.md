# Color SVG for manim library

[manim](https://github.com/ManimCommunity/manim/) can import svg's, but it removes all color information. 

This is a very simple script to color again. It doesn't work with gradients, textures, etc.

![lowquality](dumbgif.gif "aaa")

To use, just copy all the code in your file and then do something like this:

```python
from manimlib.imports import *

# copy everything here, or import color_svg_like_file, if you figure out how.

class MyScene(Scene):
    def construct(self):
        svg = SVGMobject("drawing.svg")
        color_svg_like_file(svg)
        self.play(ShowCreation(svg))
        self.wait()
```

**Note**: manim's svg support is not very good right now. Most svg's fail. This code only works with solid colors (opacity works), not gradients, textures, etc.
