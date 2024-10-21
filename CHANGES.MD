HUMANSPEED
- Human wander move speed. (Seconds needed move from one tile to next tile)
	- Increased from 7 to 10
	- Not very important, but slows down the civillans a bit
	- Part of the roughly 2x nerf to civillans speed

HUMANEVACUATIONSPEED
- Human evacuation run speed.  (Seconds needed move from one tile to next tile)
- I think this just means the speed humans move at when alerted by the helicopter
	- Increased from 1.6 to 3.0
	- Part of the roughly 2x nerf to civillans speed
	
HUMANPANICSPEED
- Human run-away-from-zombies panic speed.  (Seconds needed move from one tile to next tile)
	- Increased from 1.2 to 2.5 

ZOMBIESPEED
- Zombie default speed.   (Seconds needed move from one tile to next tile)
	- Increased from 1.55 to 3.5
	- Makes zombies alot slower. This is balanced by their larger numbers
	
## Map Size
```
While the game can fairly easily handle large maps with very minimal fps drop. However, large maps tend to look barron.
Large maps also just slow down the game, without any real benefit. The new maps should be bigger, but not mental.	

60x45 is about as big as you can go before it gets too big.
Minimum set to 40x25. Find out how it figures out the minimum?
```
GAME_CITYMINWIDTH
GAME_CITYMAXWIDTH

GAME_CITYMINHEIGHT
GAME_CITYMAXHEIGHT
- See above. REDO when actual numbers are decided

## Civillan Spawning
```
Game is optimised quite well despite being from 2011. Could run 10000 civillans at 30 fps, which really isn't that bad.
Normally, I get ~100 fps at 200 civillans.

Handles 3000 civilans at 70 fps
Handles 5000 civillans at 50fps.

3000 will be my maximum so its still runs somewhat well on other peoples toasters.
It does like to chuck a TOO MANY CIVS ON PERSONTILE error, but I don't know if that actually does anything
```
CITYPOP_LVL1 to 6
- See above. REDO when actual numbers are decided

SCIPOP_LVL1		
- See above. REDO when actual numbers are decided
- This should be the main thing that forces players to play higher difficulties.

GAME_CITYPOPULATIONCLAMP	
- Clamp the city size scalers to this max population.
	- Just set to the largest citys population (currently 3000)

## Helicopter Settings
```
```
STAT_HELI_LOADTIME_1 to 6
	- Delay between loading each passanger
		- Decreased from ~0.25 to 0.05 for all ranks to accomidate the increased survivor pool. 
		- This is a TEMP change, and will need to be ADJUSTED

UPG_HELICARRY_1 to 6
	- The amount of civillans the helicopter can hold.
		- All ranks x100 for debug purposed
		- This is a TEMP change, and will need to be ADJUSTED

HELI_LANDEDTIME
	- Heli: how long the heli waits on the ground.
		- Increased from 8.5s to 120s
			- This is for DEBUG reasons.
			- This is a TEMP change, and will need to be ADJUSTED

## Mercs
```
Need to figure out how many merc I want the player to have

```



## Zombie Spawning
```
The goal is to make it nearly impossible for the player to defeat the entire wave in the daytime.

The player should feel like they are on the backfoot in the vast majority of situations.

However, I can't make it infinite because that will make certain levels impossible. 

Also, Spawning a small trickle of zombies for a long time is a bad idea. 
It makes it really easy to spawn kill the zombies, and makes level 4 impossible because enough don't spawn in time.

This does make the game feel very artillery based, as they can wipe out massive hordes instantly.
```


ZED_SPAWNTIME
- Delay between each spawn wave (in seconds).
	- Decreased from 1.5 to 0.5 

ZED_SPAWNWAVES		
- How much zombies waves are spawned.
	- Increased from 8 to 100

ZED_SPAWNAMOUNT		
- How much zombies per wave.
	- Increased from 2 to 3


DAYTIME_SECONDS 
- Default seconds in one day.
	- Increased from 60 to 120 seconds	
	- Allows for more expression in that time, in exchange for no restarts


NIGHTTIME_SECONDS
- Default seconds in one night.											
	-Increased from 60 to 240 seconds
	- Once nighttime hits, you should die. You shouldn’t be able to survive.

TIMESCALE_MIN
TIMESCALE_MAX
- How much the player can speed up or slow down the game
- The min/max timescale (multiply by 100 to get value, i.e. "0.1" = 10% time scale)
	- Increased from 0.1, 5.0, to 1.0, 2.0
	- This makes the game realtime. The player cannot pause if things get rough

TIMESCALE_DEFAULT
- Default speed the game is at
	- Changed from 0.7 to 1.0 to match TIMESCALE_MIN
	

## Other
MAXKEYBOARDPANDISTANCE
- Camera: how fast you can pan with keyboard when fully zoomed out.
	- Increased from 700 to 4096. Makes moving around with a big map alot easier.
	- This is a TEMP change, and will need to be ADJUSTED
    
## Undocumented Changes
```
Stuff I need to get around to documening
```
MERCS_MAX
MERCS_MAX_PLUS
PARTYWAGON_MERCS
MERCS_AMT_ARTILLERY
MERCS_AMT_LANDMINE	
MERCS_AMT_DYNAMITE		
MERCS_AMT_BARRICADE		
MERCS_AMT_SNIPERS		
MERCS_AMT_INFANTRY		
MERCS_AMT_NECTAR		
UI_CONTROLBOX_BUTTONS	