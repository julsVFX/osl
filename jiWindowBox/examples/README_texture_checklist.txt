
___________________________________
###jiWindowBox Texture Checklist###
___________________________________


**Make sure you only have an alpha in the midground and curtains area.
-All walls, the ceiling and the floor should have a black alpha.


**For use with RenderMan and Arnold, make sure to convert your textures to mipmapped texture files using maketx (Arnold) or txmake (RenderMan).
-This is mainly for performance reasons but is a requirement for RenderMan.


**If you are exporting your texture in an initial format that keeps bounding boxes (like OpenEXR), make sure that the bounding box matches your format exactly.
-Most renderers will take the bounds of the data window over the actual display window (this is also the case when converting to .tex files). 
-If your bounds are bigger or smaller than your output format it will mess up the alignment in the shader. 


**The midground and curtains layer should be unpremultiplied.
-Premultiplication is happening in the shader, so if your input midground/curtains area is already premultiplied you will most likely get dark edges.
