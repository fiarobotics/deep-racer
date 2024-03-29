# Input parameters
The reward function input parameters (params) are passed in as a dictionary object, specifying a given state (params["x"], params["y"], params["all_wheels_on_track"], params["distance_from_center"], etc.) the agent is in and a given action (params["speed"] and params["steering"]) the agent takes. You manipulate one or more of the input parameters to create a customized reward function most appropriate for your solution.


## all_wheels_on_track
boolean

A boolean flag to indicate if the vehicle is on-track or off-track. The vehicle is off-track (False) if all of its wheels are outside of the track borders. It's on-track (True) if any of the wheels is inside the two track borders.

## x
float

Location in meters of the vehicle center along the x axis of the simulated environment containing the track. The origin is at the lower-left corner of the simulated environment.

## y
float

Location in meters of the vehicle center along the y axis of the simulated environment containing the track. The origin is at the lower-left corner of the simulated environment.

## distance_from_center
float [0, ~track_width/2]

Distance from the center of the track, in unit meters. The observable maximum displacement occurs when any of the agent's wheels is outside a track border and, depending on the width of the track border, can be slightly smaller or larger than half of track_width.

## is_left_of_center
boolean

A Boolean flag to indicate if the vehicle is on the left side to the track center (True) or on the right side (False).

## heading
float (-180, 180]

Heading direction in degrees of the vehicle with respect to the x-axis of the coordinate system.

## progress
float [0, 100]

Percentage of the track complete.

## steps
integer

Number of steps completed. One step is one (state, action, next state, reward tuple).

## speed
float [0.0, 8.0]

The observed speed of the vehicle, in meters per second (m/s).

## steering_angle
float [-30, 30]

Steering angle, in degrees, of the front wheels from the center line of the vehicle. The negative sign (-) means steering to the right and the positive (+) sign means steering to the left.

## track_width
float

Track width in meters.

## waypoints
List of (float, float)

An ordered list of milestones along the track center. Each milestone is described by a coordinate of (x, y).

## closest_waypoints
(integer, integer)

The zero-based indices of the two neighboring waypoints closest to the vehicle's current position of (x, y). The distance is measured by the Euclidean distance from the center of the vehicle.


