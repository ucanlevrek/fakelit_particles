# fakelit_particles
Scatter Fake Lit Particles Aling Geometry (HDA)

I've only used this HDA in Houdini. So it might not work well with game engines, I will work on that soon.

Lighting the particles without them creating shadows to one another was useful for me to create a still image of a stock statue model that I've found online.

Then the HDA was the way to go to proceduralize the system.

With a for loop I collect the positions and colors of lights specified in OBJ level HDA. 
Then with the given geo by user it scatters points along geometry and deletes the ones that are not seen by any light regarding the angle limit
(means that if the angle between Normal of the point and the light exceeds limit, it deletes the point)

After that, the shading control is given with ramping the angle between normal and light. It is art directable as it is a ramp controlled shading technique.

The scaling can also be controlled with this angle if wanted. The shade bias is a lerp controller with scale with/without shading. 

Shaded scale can also be controlled through a ramp in HDA.
