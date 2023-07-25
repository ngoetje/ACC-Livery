Skin with Blender

Transcribed from
https://www.youtube.com/watch?v=5rWCdsldUCw

## Setting up the paint environment
1. File > Import > Waveform (Legacy)
2. Select car model
3. Zoom out
4. Left click on car
5. Right click on car > Shade Smooth
6. Activate "Texture Paint"
7. "Texture Slots" menu on the right ("Draw") click + to add:
![314ea44bec474bc85789616e2efd925e.png](:/9054f2e60ac949febc2d624e9f406763)

7.1 Base Color Paint Slot named "base" with 4096x4096 and a bright color

7.2 Add another Base Color Paint Slot named "decals" with 4096x4096 and color's alpha = 0

7.3 Add another Base Color Paint Slot named "sponsors" with 4096x4096 and color's alpha = 0

9. On the Texture Map pane, move mouse to lower right corner. When cursor changes, pull up another pane.
10. In the new Pane select "Shader Editor" (Shift+F3 or via menu in top left)
11. In the Shader Editor:
10.1 Remove all connections
10.2 Go to Add > Search > "Mix" to add Mix object
10.3 Right click on header > Duplicate
10.4 Connect as follows:
		- base Color > Mix 1 A
		- decals Color > Mix 1 B
		- decals Alpha > Mix 1 Factor
		- Mix 1 Result > Mix 2 A
		- sponsors Color > Mix 2 B
		- sponsors Alpha > Mix 2 Factor
		- Mix 2 Result > Base Color

![bed88fb30800b794175c491d3d3ec022.png](:/1480cbafa7104f1cac87a851976bcf0f)
11.Select "Viewport Shading (Solid)"
![739a01a630da93a4e2c3b7a546bcd317.png](:/ebbf57bd839a4e6fa2ead524129bdf8d)
12. Select "decals" layer
13. Select X on the upper right corner to enable symmetrical painting
![39f34ab7c71aae5414ecbd674389258e.png](:/9289112340f14ae7a8931ed4c89c5be4)

**You can now paint your car!**


## Select target sites to paint on:
1. Hit TAB to show the wireframe of the car.
2. Yellow edges are selected
3. Click somewhere to deselect edges.
4. Select Paint Mask in upper left corner
5  ![5a444d781d62c4af019e097cb8b9b9a7.png](:/2817e95ada59436e9b3b9591c938896a)
6. You will be unable to paint now, because nothing is selected.
7. While hovering over the target area with the cursor, press L to set the selection to it.
8. To enable symmetrical you have to select the other side as well.

## Adding decals
1. Go to Texture Properties 
![678a9f77ae2fb2fb5eabcaa3d950f78d.png](:/404e4671c5914499bd0a8cce1caa59bf)
3. Create new brush
4. Click on Open
5. Select logo to use as decal
6. Select maping and "Clip" 
![e2e375e88a91c54d24d9943e32ae76f9.png](:/ac4c28500dbd4788866ab140f4c12d31)
8. Go to Active Tool > Texture > Mapping and select Stencil 
![5b7bb877ba6d320f1061cca4d2be58b5.png](:/ee2b058cac244353913f6efb59b92c5d)
10. Click on Image Aspect and Reset Transform to reset stencil 
![926cfa5ca55f1132f355940ffa39449b.png](:/0d3242c2525e46858b76573948c42708)
12. Select White color and paint over the stencil
13. Hold shift+right mouse button to resize stencil
14. Hold ctrl+right mouse button to rotate stencil

## How to make the words read from left to right correctly when using stencil tool for both sides of the car because the words are backwards?

The way I do it:
1. Set up a texture with a stencil
2. Position the stencil on the car
3. Paint the logo/wording on the car with X axis symmetry enabled (it will be backward on the otherside, but it's important to have it painted on the other side for the followingstep)
4. Switch the view to the other side
5. Position the stencil over the backward wording on the other side
6. On the right dock under the Texture image click on the X to remove it
7. Disable symmetry
8. With Erase Alpha mode erase the painted logo/wording
9. On the right dock click on the checkered board where the image used to be before and select the previously used stenctil
10. Stencil should be in the same position as you positioned it before so that you can paint over the stencil once more 

## Misc Notes:
Falloff: configures the edges of the brush
