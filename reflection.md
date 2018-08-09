# Effects of the P, I, D components
* The **P** coefficient governs the ability to correct error, i.e. steer back to the center of the road. The bigger the P, the faster it corrects the error, and the easier to overshoot. Especially when the speed is high, large P just throws the car off the road.
* The **D** coefficient counters overshooting, i.e. it counter steers the car as error drops. As **D** increases, the cars turns slower.
* The **I** coefficient is supposed to counter system bias (drift), but there's barely any in the project's case.

Their effects are mostly within my expectation, and it's amazing to see how changing them affects the performance in the simulator.

# How the P, I, D coefficients were chosen
* I set **I** to 0 because there's no drift in the car in the simulator, so setting it would just introduce noise.
* I picked **P** by fixing the throttle, and manually increased it when the car missed the sharp turns, and decreased it when the car overshot off the road.
* I picked **D** by first setting **I** so that the car could make the turns, but overshot in the more straight sections, then increasing **D** until the car always stayed on the road.
