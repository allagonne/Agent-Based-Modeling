# Agent-Based-Modeling - space colonization
# ask me for the .nlogo model

## WHAT IS IT?

The goal of this project is to simulate with NetLogo (v6.2) a space colonization of humans, starting from Earth, into the Milky Way.

## HOW IT WORKS

At setup, there are 1 colony = Earth and n ships (defined by ships_per_colony slider)
Every ship goes in a random direction and settle at the next tick on next pixels. During that time, colony_destruct_risk and ship_destruct_risk are asked if colonies and ships self-destructed, and colonies are asked if they want to expand (expansion_willingness) : if so, they create n new ships (defined by ships_per_colony slider) that would expand mankind. 
Note that ships won’t settle and die if they go to a out-of-galaxy area (black patchs) or a already-colonized area (blue patchs).
The model stops at 1001 ticks.

## HOW TO USE IT

Change the parameters, load the setup and click on go
On the left, we would have the setup and go buttons, and also a few sliders :
-	Ships_per_colony : number of ships sent into space by every colony at every tick, if the expansion willingness is achieved. Goes from 0 to 10
-	Colony_destruct_risk : the risk for every colony (including Earth) to be destructed at every tick (auto-nuclear destruction, planet collision with asteroids, global warming…). Goes from 0 to 1
-	Ship_destruct_risk : (similar to the previous slider, but for ships) the risk for every ship to be destructed at every tick. Goes from 0 to 1
-	Expansion_willingness : Willingness for every colony (including Earth) to expand. If the condition is not satisfied, the colony would randomly “pass” for 1 tick, and the expansion willingness is asked 1 tick later (if the colony survived). Goes from 0 to 1

On the right, we would have a graphic metric :
-	Nb of colonies : number of colonies (exactly, number of pixels colonized) in the whole galaxy


## THINGS TO NOTICE

(suggested things for the user to notice while running the model)

## THINGS TO TRY

If we take small values for our 4 parameters (ships_per_colony 1/colony_destruct_risk 0.07/ship_destruct_risk 0.1/expansion_willingness 0.1), often (80% of the times), the model would not survive a few ticks, but sometimes the simulation would make a long time to perform a big expansion, and then the number of colonies would increase exponentially after more than 200 ticks. 

We can see that the model is really dependent on the parameters : an increment of 0.01 of, let say, “colony_destruct_risk” would leave us with much rare cases of expansion : more than 90% of the models would result in no expansion.
With much higher number of parameters, we can find “holey” galaxies, with lots of uncolonized zones in the galaxy. I personally find it very interesting that we obtain some kind of a maximum limit 


## EXTENDING THE MODEL

-	We are not alone : we could simulate other civilizations with other colors for ships and colonies, and simulate if there are peaceful (they won’t attack our civilization), or hostile (they would attack, and we would have war zones and a risk to lose some colonies). It would be interesting to see if they can live together, and if so, with different spatial zones or totally mixed populations, or if only 1 civilization would survive, and why (do they send more ships into space? Did they start from a better place into the galaxy?...)
-	Time : 
o	we could simulate the time by making a new slider “speed of ships”, and the expansion would depend on it. Also, a time window is 1 tick, and we considered that ships go from 1 pixel to another in this tick. 
o	The probability that ships or colonies self-destruct is considered by 1 tick too, so  we could take a different time window and fix a precise time-window (for ex 1 tick = 1000 years), that probability would also change. 
o	If we have ships that go at 1/100th of the speed of light (it is already very fast) and we choose a time window of 1000 years for 1 tick, we would need 50 ticks to go from 1 pixel to the next one!
-	Galaxy catastrophy : We also can simulate accidents inside of the galaxy : super-novae risk and black-hole risk for example. 
-	Human density : in this project, we considered only 1 colony per pixel. But as we said, there are about 10 million suns per pixel, and many unhabitable worlds in that. We could increase the density of humans in every pixel, so that if a specific colony is destructed, there remains some human presence in this pixel, and we can keep the patch with blue color. 


## NETLOGO FEATURES

None ; see the code for deep understanding

## RELATED MODELS

None

## CREDITS AND REFERENCES

Arnaud Llagonne
https://github.com/allagonne/Agent-Based-Modeling
