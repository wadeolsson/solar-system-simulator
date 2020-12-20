# Things we need


## Functions:
- Need a function to calculate force of gravity between two entities
- Need function to calculate forces on craft from many entities
- n-body problem or 3-body problem with sun, craft, and whatever body we are closest to (ignoring moons)

## Models:
- Model of solar system with sun at (0,0)
- Mass of craft

## Parameters:
- Initial positions of planets
- Equations for elliptical orbits of planets 

## Algorithm
- Initialize
  - Initialize solar system
  - Advance to certain date
- Launch vehicle
- Simulate
  - pick first target from list (will be a sequence of destinations like moon, earth, moon, venus, mercury, earth, moon, mars, jupiter, saturn, neptune, uranus, pluto)
  - for each target:
    - do this until the craft reaches its destination (e.g., Mars)
      - At each time step:
        - move all objects and craft forward on their trajectories
        - calculate new directions and speeds of all objects 
        - calculate distance from next target
        - if we are getting further away then, switch to next target

## Dynamic attitude adjustment
After a gravity assist, we must predict the angle of attack for the next maneuver. If coming off of a gravity assist we are off the angle, we will need to spend some delta-v to adjust course. 
