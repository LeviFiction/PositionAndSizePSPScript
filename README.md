# PositionAndSizePSPScript
A script to offer exact positioning and sizing of objects and layers similar to that offered by PhotoImpact

## Purpose
A question was posed on the User to User forums asking if it was possible to set exact positions of objects on the canvas similar to the way PhotoImpact could, including the ability to set them according to physical measurements like Inches and Centimeters.

The PhotoImpact dialog I was shown in a screenshot had two frame labels, one for position (in pixels I assume) and one for size (using any measurement offered).  Available units were not defined.  Need to find documentation to get exact specifications on options but otherwise looks pretty straight forward.  

## How I will accomplish this
The GUI will be made in the only way possible without doing something annoying or weird with input boxes, with Tkinter.

Once all settings are set the pick tool command will be used to convert given coordinates to pixels and the distortion will be made.  If only position changes and not original size then the mover command will be used as it's faster.  PSP assumes distortion when Pick is used and sends it through that command slowing things down.  Mover simply moves the layer.  
