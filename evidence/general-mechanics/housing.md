---
search: false
---

# Housing

**Main Page:**

{% page-ref page="../../general-mechanics/housing.md" %}

## Tree Mechanics

### Tree Chopping Memory Mechanics

By: mol\#3280  
Added: 6/6/2021  
[Discussion](https://tickettool.xyz/direct?url=https://cdn.discordapp.com/attachments/838678429137633311/851309968694837268/transcript-tree-chopping-memory.html)

**Finding:**  
The game can only remember the 10 most recently-struck trees at a time. After the 11th tree is hit, the 1st tree's state is wiped from the memory and can be harvested again. However, if a previously harvested tree is struck again BEFORE this, it will be moved back into the sequence as the most recently updated item. Therefore, a loop in the following order where each number represents a specific tree will generate no wood on the second partial loop: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11. This is because trees 2-11 have become the recently updated set in memory, and only 1 has been dropped and reverted to "harvestable" state. In a typical 11 tree loop, hitting tree 1 again would provide wood, then remove the most recent last tree \(tree 2 in this case\) from memory. Partial harvests also count the same as full harvest or re-harvest.

**Evidence:**  
[Partial harvest evidence & 11 tree loop](https://imgur.com/a/WAz7Ubk) [Hitting tree 2 before 1 on second loop proves minimum loop is 11](https://imgur.com/mzky3xy), only the 11th tree is reset, and updating mechanics.

**Significance:**  
There is no quick method to reset tree resources beyond hitting an 11th tree and removing the 10th-previously-harvested tree from the memory. Aside from logging out of the game, these mechanics are key to quick farming of a targeted type of tree. Fast traveling has no effect, nor does entering a domain, nor does waiting several minutes. To keep farming trees efficiently, the loop must avoid all 10 trees already in memory. Adding a buffer of an additional 1 or 2 trees into the loop can help prevent accidentally updating depleted trees in memory and wasting time. Additionally, if your loop contains mixed tree types, you can exploit the partial harvest finding to farm one type faster by only striking the less-desired trees one time each before moving on.

### Temporary Skill Targets: Enabling Unholy Harvesting Methods

**By:** mol\#3280, wiremash\#0433, Aluminum\#5462  
**Added:** 6/6/2021  
[Discussion](https://tickettool.xyz/direct?url=https://cdn.discordapp.com/attachments/839914390328573963/851314539345215509/transcript-marking-non-enemies-for-skill-hits.html)

**Findings:**  
Attacks that shake untouched trees, including enemy attacks, can allow them to be harvested using a small number of Elemental Skills in a short window. We explored this to find several things.

* Shaking a tree marks it as a target for a wider variety of skills. Some attacks, like Mona's E, can only shake already-marked trees, and do nothing.
* All physical damage sources & an odd assortment of character skills \(Jean's E, Kaeya's Q\) can shake/mark
* Marks last a very short time
* Some skills and Overloads can harvest. Characters like Bennett and Xingqiu can harvest using E skills, while Razor can harvest with E only if he uses Overload. 

**Evidence:**  
Summary post with multiple videos here [https://imgur.com/a/RnevAeW](https://imgur.com/a/RnevAeW)

**Significance:**  
Attacks are not equal in terms player-environment interaction. Most skills can never harvest nor shake tress; some can shake trees, others can harvest directly, while others can harvest indirectly via Overloading burning grass. Most importantly for combat, damage sources appear to be treated differently depending on the character, attack, and reaction source. Overloading via E to harvest a marked tree works for Razor and Beidou, but not Xiangling or Fischl's elemental arrow. Overload seems to work on burning grass but not self-overloads. Dealing phys damage with Xinyan harvests using a Normal Attack, but only shakes during her Burst. More broadly, the game appears to be conserving resources by limiting the player's kit unless certain enabling actions are taken. After enabling these attacks, the game shuts them down after a short window. Enemies appear to be permanently enabled for all attacks, but the player must fight enemies within a specific area, otherwise they will teleport back and reset.

### Lumberjack Tier List

**Contributors:** Aluminum\#5462, Green sabre\#0540, Kourinn\#6001, mol\#3280, Steph\#3614, JenjenJL\#6582, Greyhound\#7836  
**Added:** 6/6/2021  
[Discussion](https://tickettool.xyz/direct?url=https://cdn.discordapp.com/attachments/836973979108769822/851323163400208404/transcript-lumberjack-tier-list.html)

[Link to Tierlist](https://docs.google.com/spreadsheets/d/1Q4HKzkaw7YFNZyIJSjRINZJonFe1kiDwz1dEbpcZiNk/edit#gid=937070148)

Summary of Results, most efficient units for tree chopping:

* Xingqiu \(only if you manually time their attack string, spam clicking won't work\)
* Keqing
* Rosaria
* Xiao

## Wood Daily Drop Limit

**By:** Creonalia\#2818  
**Added:** 5/21/2021  
[Discussion](https://tickettool.xyz/direct?url=https://cdn.discordapp.com/attachments/842601710391787551/845506814519148574/transcript-2k-wood-daily-cap.html)

**Finding:** You can only collect 2,000 of any specific wood per day. This limit resets at server reset and cannot be reset by relogging/teleporting.

**Evidence:**

* Inventory before and after farming wood over 3 days: [https://imgur.com/a/tNZP68q](https://imgur.com/a/tNZP68q)
* Evidence that player cannot collect more bamboo, but can collect other wood: [https://youtu.be/f\_eQfp1FWLM](https://youtu.be/f_eQfp1FWLM) 
* Same for pine wood: [https://youtu.be/yh4PodfeX7c](https://youtu.be/yh4PodfeX7c)
* Hitting cap and testing teleport and logout/login \(and showing that neither reset the cap\): [https://youtu.be/pE-vHLpum6Q](https://youtu.be/pE-vHLpum6Q)
* Collecting pine wood after server reset \(marked by new daily commission quest at 0:12\): [https://youtu.be/9WrYqapBFkU](https://youtu.be/9WrYqapBFkU) 

Note that although I did need to teleport to get wood after reset, teleporting alone does not reset the cap, as shown above.

**Significance:** Useful for players to know if they're farming a massive amount of wood.
