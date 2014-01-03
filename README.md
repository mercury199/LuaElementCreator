Lua-Element-Creator-Current
===========================

Used to create Lua scripts, which can in turn create an element in The Powder Toy

The different properties are:
Name	 
  Name, it is recommended to use 4 letters, but less works. 5 or more will probably not fit on the buttons
Colour
  Default color, in hexadecimal (RRGGBB)
MenuSection	 
  The menu section it's in, should be obvious from the pull-down menu
Advection	 
  How much the particle is accelerated by moving air. Normally 0 for solids, and up to 1 for other elements. It can be    negative, ANAR and DEST do this so it goes towards pressure
AirDrag	 
  How much air the particle generates in the direction of travel. Generally is very small, 0.04f creates a lot of
  positive air (- creates negative pressure).
AirLoss	
  How much the particle slows down moving air (although not as big an effect as a wall). 1 = no effect, 0 = maximum
  effect. Solids are generally above 0.90f, along with most other elements too
Loss	 
  How much velocity the particle loses each frame. 1 = no loss, .5 = half loss. Solids have it at 0. Only a few have it   at 1, like energy particles, and old moving sponge.
Gravity	 
  How fast the particle falls. A negative number means it floats. Generally very small, most gasses are negative,
  everything else is usually less than 0.04f
Diffusion	 
  How much the particle "wiggles" around (think GAS or HYGN). Set at 0, except for gasses, which is a positive number.    Up to 3 (or higher) for a large amount of wiggle, GAS is 0.75f, HYGN is 3.00f
HotAir	
  How much the particle increases the pressure by. Another property only for gasses, but VENT/VACU have theirs at
  (-)0.010f. An extremely small number, sometimes as small as 0.000001f. THIS IS NOT IMPLEMENTED IN LET YET!
Falldown	 
  How does the particle move? 0 = solid, gas, or energy particle, 1 = powder, 2 = liquid.
Flammable	 
  Does it burn? 0 = no, higher numbers = higher "burnage". Something like 20 is WOOD, while C-4 is 1000. Some are a few   thousand for almost instant burning.
Explosive	 
  Does it explode? 0 = no, 1 = when touching fire, 2 = when touching fire or when pressure > 2.5. Yes, those are the      only options, see FIRE.cpp or somewhere in Simulation.cpp to modify how they work
Weight	 
  Heavier elements sink beneath lighter ones. 1 = Gas. 2 = Light, 98 = Heavy (liquids 0-49, powder 50-99). 100 = Solid.   -1 is Neutrons and Photons
Temperature	 
  What temperature does it have when created? Temperature is in Kelvin (Kelvin = degrees C + 273.15). R_TEMP+273.15f      gives room temperature - SOON TO BE IMPLEMENTED
HeatConduct	 
  0 - no heat transfer, 255 - maximum heat transfer speed - SOON TO BE IMPLEMENTED
Description	 
  A short one sentence description of the element, shown when you mouse over it in-game
  
Update	 
  The update function
Graphics	 
  The graphics function, tod
