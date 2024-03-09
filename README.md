# gimp-scripts


Scheme scripts for Gimp's script-fu.

Define vars: (define <name> <val>)

Set var: (set! <var>(<expr>))

Lists: '(<val> <val> <val>)
<br />- can be different types- int, string, double
<br /> Get first from list: (car <var>)
<br /> Get all except first item: (cdr <var>)

Do (gimp-displays-flush) at end of script

Look for methods in Help > Procedure Browser




(script-fu-register
  "script-fu-smooth-threshold" >> starting point of script
  "<Image>/Colors/Smooth Threshold" >> where to put script in menu, goes to Image menu then goes in colors, name appears as Smooth Threshold
  "Threshold with smooth edges." >> description of script (when you hover over item in menu)
  "monsoonami" >> name of author
  "monsoonami" >> copyright info
  "June 2012" >> date script was written
  "RGB*, GRAY*" >> which image modes the script can apply to
  SF-IMAGE      "Image" 0 >> what values need to input into script... 
  SF-DRAWABLE   "Layer" 0 >> drawable (layer, channel, layer mask...) ... gimp should figure out what these are. 0 = default val for params
)