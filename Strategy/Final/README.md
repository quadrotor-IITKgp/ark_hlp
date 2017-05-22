STRATEGY CODE:

1) ComputeDistance():
Computes the perpendicular distance of each bot bot inside the arena from then green line and pushes this distance and the corresponding bot id into a 'set' which keeps the distances in the ascending order.

2) FirstOperation():
Performs the tapping or bumping on the target bot on the basis of its current angle.

3) IsOutsideWhite():
Checks if the target bot is outside the green line.

4) t_plan():
This function searches which bot inside the 5m circle must be tapped or bumped. The calls the action().

5) action():
This performs the action on the surrounding bot depending on it's current direction.

6) retrieve_pose():
Updates the pose and twist of the current bot in the specified message.

tap_n_turn: class for the control's code for tapping the bot (work under progress)
fly_quad: tap_n_turn object (strategy working keeping all calls of this object commented out)

Problems:

1) Tapping of quad not working properly

2) A case: where a groundbot is inside the arena before assigning the target bot and the bot itself is made the target bot. But just after that it leaves the arena before any action can be performed on it. The code goes rogue if this happens!

Parallel programming to check if the target bot is inside the arena.
OR
Put a check for it to be inside the arena before it performs the operation on it, if outside, reset the strategy.  

In other cases working fine.
 