# Named areas

This mod gives names to different small'ish areas of the map, and adds interactions based on these areas. This document describes aims of the mod, the actual implementation at the time of the writing is completely missing.

## Description

### Areas

Areas are 1-7 tile sized portions of the map, each with their individual name. Two tiles of an area can be at most 2 tile away from each other.

All non-yield tiles are unnamed.

Name generation gives names to any mountains and mountain ranges. Then to all islands(islands are areas composed of less than 15 tiles). Then to all bays and peninsulas(coastal tiles included). Then to all lakes(lake areas compose of only lake tiles or tiles directly adjacent to that lake. Minimum of one each). Then to all deserts. Then to all valleys(passages through hill or mountain terrain, where there is a flat tile in the middle, touching two hill or mountain tiles which are separated by flat tiles). Then to all tundras, then to all plains, then to all grasslands.

In case of mountain ranges for example, single mountain range can be larger than just a single area. In this case, each individual named area still is going to only be 1-7 tiles large, and the whole mountain range simply consists of multiple areas.

### City settling

Only one civilization may claim a tile from any one area. Settler cannot settle on tiles whose area has been claimed by another civ, and you cannot expand to or purchase tiles whose area has been claimed already. I'll use term "Weakly claimed" to describe scenario where one civilization has control of an area a tile is in, but it does not have had its city borders yet expand to control that tile.

### Areas swapping owners

If an area swaps ownership, then all other civilizations lose their tiles on that area. Exception is made for districts and wonders, which remain under the ownership of the city that created them.

### War

If during war one civ is the only one to have military units on an area, this civ has occupied this area. The previous owner loses ability to work any tiles in this area, and new owner can either expand their city borders to this area, or settle a new city in this area. This gives half the warmonger penalties associated with taking a city.

### Trading

Areas are directly tradable in the trade screen. Trading an area gives for the buyer a weak claim of the area for 15 turns, which they can capitalize upon by settling a city, or expanding their existing borders.

### City growth

Each area receives immigration from nearby, populated areas based on the sum of appeal of all the tiles, and the sum of food on the area of emigration. This appears as small bonus to food for the city that owns that area.

### Missions

Each area type has score for how "culturally similar" they are. Mountain ranges, oceans etc totally separate the people, while grasslands act as connectors. Your people will want to expand onto connected areas. Not doing so will reduce amenities in connected cities for both civs, but the civ with higher culture output gets reduced amount of negative amenities. Declaring a war, or having an alliance reduces the negative amenities from this mechanic by 75%. Having a declaration of friendship reduces negative amenities by 25%

### Casus Belli

With Feodalism unlocks new Casus Belli, "Declare War of Forward Settling", which reduces the cost of declaring war and taking over areas other civ controls, but has significantly higher cost for capturing cities.
