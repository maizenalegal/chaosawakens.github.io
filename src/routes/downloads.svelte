<script>
    import semver from 'semver';
    import Title from '$lib/components/Title.svelte';

    let downloads = [
        //STABLE

        {
            version: '0.9.0.0',
            mcVersion: '1.16.5',
            branch: 'stable',
            changelog: `
                    - Added corn and tomato crops work *and* generate in the world. <br>
					- Added tube worms. <br>
					- Added Advancements. <br>
					- Ant and termite nests now spawn and function! Added crystal termite nest. <br>
					- Illusioners can now spawn in village raids! <br>
					- Giants now have some AI! <br>
					- You can trade for some Chaos Awakens items from villagers! Try a farmer, butcher, fletcher or a wandering trader, you may get lucky. <br>
					- Added spawn eggs for some vanilla mobs. The illusioner, the giant, the wither and the ender dragon. <br>
					- Added 7 new variants of Ent(for every vanilla wood type), for your Ent-y needs! <br>
					- Added 7 new variants of Ent Tree dungeons and updated the trap! Gotta see 'em all! <br>
					- Added Wasps and their hives. Also added a "nest block" that is a decorative bees nest. <br>
					- Added the Stinkbug and the Dead Stinkbug item. <br>
					- Ore generation rebalances! <br>
					- Added nether ruby ore. Now you can find rubies in Nether lava pockets. <br>
					- Royal guardian boots now give slow falling only when shifting. <br>
					- Added apple, cherry and peach trees with delicious fruits! <br>
					- Added dupe tree wood, currently has no function! <br>
					- Added ender pearl and eye of ender blocks! <br>
					- Added big bertha and the blade, the guard and the handle! (currently unobtainable) <br>
					- Added battleaxe and queen scale battleaxe! (currently unobtainable) <br>
					- Added ultimate fishing rod! (doesn't work properly yet) <br>
					- Added moth scale, royal guardian and queen scale armors! (currently unobtainable) <br>
					- Added miners dream! The mines are mineier! Added moldy wood planks and mining lamps. <br>
					- Added fossilised wtf, scorpion, wasp and piraporu. Only the wasp is usable. <br>
					- Added queen scale, ender dragon scale, mantis claw, moth scales, nightmare scale, vortex eye and triffid goo! (Only the ender dragon scale is obtainable)<br>
					- Added some coins. <br>
					- Added random teleport block! <br>
					- Added custom tooltip descriptions. <br>
					- Changes to village mania. Fruit trees and crops spawn here and more mob spawning! <br>
					- Changes to mining dimension. Stalagmite valley biome! <br>
					- Added extra config options. <br>
					- You can now breed enchanted golden apple cows if you enable a config option. <br>
					- You can make zombie, skeletons, creepers and the ender dragon drop their mob heads or disable it with a config option. <br>
					- You can make the ender dragon place a dragon egg after each death instead of only the first death. <br>
					- Bug fixes! <br>
					- <i>Lore intensifies!</i> You can disable tooltips if you want to, they exist now. <br>
					- Some nice updated textures! <br>
					- And a lot more!`
        },
        {
            version: '0.9.0.1',
            mcVersion: '1.16.5',
            branch: 'stable',
            changelog: `
                    - Fixed ultimate gear being uncraftable. <br>
					- Netherite ingots no longer can be used to craft ultimate gear, only platinum can. <br>
					- Fixed hercules beetle and stink bug animations. <br>
					- Read 0.9.0.0 changelog.`
        },
        {
            version: '0.9.0.2',
            mcVersion: '1.16.5',
            branch: 'stable',
            changelog: `
                    - Peacock and queen scale boots now cause feather falling only when you press shift. Be advised the slow fall lasts for 3 seconds! <br>
					- Village mania is now fixed! Go explore some villages and kill some robos. <br>
					- Dirt no longer spawns in the stalagmite valley biome in the mining paradise. <br>
					- Ent trees no longer spawn in village mania, crystalworld or mining paradise. <br>
					- Caves do not spawn in the village mania. <br>
					- Fixed not being able to start servers with the mod installed. <br>
					- Read 0.9.0.0 and 0.9.0.1 changelogs.`
        },
        {
            version: '0.9.0.3',
            mcVersion: '1.16.5',
            branch: 'stable',
            changelog: `
                    - Fixed crash when trying to use Royal Guardian Armor on an Anvil. <br>
					- Fixed crash when attempting to use the Ent Spawn Egg. <br>
					- Stink bug now gives nausea when attacked. <br>
					<b>PATCH:</b> <br>
					- Fixed crash on startup. <br>
					- Added some tags. Fixes not being able to use custom logs and planks for vanilla recipes that use them like sticks. <br>
					- Apple Cows can now sometimes spawn with a new fancy texture! Happy Halloween!`
        },
        {
            version: '0.9.0.4',
            mcVersion: '1.16.5',
            branch: 'stable',
            changelog: `
                    <b>Items</b> <br>
					- Spawn Eggs for the Ents have been separated. Each Ent has its own spawn egg now. <br>
					- Added the Poppy Sword. Also gives the poison effect. <br>
					- Poison Sword now gives Confusion. I mean why did it give every effect except the one the mob it came from gives. lol <br>
					- All foods that give good effects now give bad effects instead. (Except the item below) <br>
					- Hot Flaming Cheetos have been added to Chaos Awakens. <br> <br>
					<b>Blocks</b> <br>
					- Ant Infested Ores now show up as the ore in The One Probe UI instead of the Infested Ores. <br>
					- Ant Nest Blocks now only spawn ants if a player is nearby and if there aren't many ants nearby. Ant nests don't spawn ants if there is rain on the block above it. Ant Nests spawn more common in Red Ant and Termite Dimensions. <br>
					- Cherry Cobblestone was added to the mod. IF you light it on fire you get Cherry Fire. <br>
					- Standing in Cherry Fire or on a Cherry Campfire you get Regeneration and Health Boost. <br>
					- Cherry Lanterns and Cherry Torches are in the mod. Based on the Cherry Fire. <br>
					- Separate Fossilised Ent Fossils. There is now a fossil for all 8 Ents. <br> <br>
					<b>Structures</b> <br>
					- A structure called the ultimate house has been added to Chaos Awakens. The structure has a basement with some ultimate ores. You could call this an Ultimate Basement. <br> <br>
					<b>Entities</b> <br>
					- A feature from the last update that was forgotten in the changelog was that Golden Apple Cows and the Enchanted Golden Apple Cows give off sparkle particle effects. <br>
					- Apple Cows have new animations now. The Enchanted Golden Apple Cow has a better glint now. <br>
					- Ants seem to be a little bigger now and drop more exp. <br>
					- Ants seem to teleport you to the wrong dimension. Oops! who messed up the teleporter. <br>
					- Ents are 80% cuter. Ents have shrunk to a very small size. <br>
					- Some villager trades that are in the mod were updated a bit. Wandering Traders, Farmers, Fletchers and Fisherman now give more items. <br> <br>
					<b>Advancements</b> <br>
					- Added an Advancement for killing Ants. They seem big enough for an advancement. <br>
					- Added an Advancement for obtaining the Poppy Sword. Why was the Rose Sword even in Orespawn... <br>
					- Fixed All Armor Advancement requiring Moth Scale Armour which is unobtainable. <br>
					- Shiny Cows advancement can now be gotten by breeding Enchanted Golden Apple Cows. <br> <br>
					<b>Dimensions</b> <br>
					- Teleporting to the Crystal World now requires an empty inventory. You can disable this in the config. <br> <br>
					<b>Commands</b> <br>
					- Added the "/chaosawakens" command. Syntax includes "website", "discord", "github", "wiki", "reddit" and "version". <br> <br>
					<b>Chat</b> <br>
					- Typing "April Fools!" in chat will make you drop any items in your inventory. Clumsy!`
        },
        {
            version: '0.10.0.0',
            mcVersion: '1.16.5',
            branch: 'stable',
            changelog: `
                    <b>From April Fools Update | Anything mentioned in the April Fools 0.9.0.4 Changelog but not listed here is not in this version.</b> <br>
					- Spawn Eggs for the Ents have been separated. Each Ent has its own spawn egg now. <br>
					- Poison Sword now gives Confusion. I mean why did it give every effect except the one the mob it came from gives. lol <br>
					- Ant Infested Ores now show up as the ore in The One Probe UI instead of the Infested Ores. <br>
					- Ant Nest Blocks now only spawn ants if a player is nearby and if there aren't many ants nearby. <br>
					- Ant Nests do not spawn ants if there is rain on the block above it. <br>
					- Ant Nests spawn more common in Red Ant and Termite Dimensions. <br>
					- Separate Fossilised Ent Fossils. There is now a fossil for all 8 Ents. <br>
					- A feature from the last update that was forgotten in the changelog was that Golden Apple Cows and the Enchanted Golden Apple Cows give off sparkle particle effects. <br>
					- Apple Cows have new animations now. The Enchanted Golden Apple Cow has a better glint now. <br>
					- Some villager trades that are in the mod were updated a bit. Wandering Traders, Farmers, Fletchers and Fisherman now give more items. <br>
					- Fixed All Armor Advancement requiring Moth Scale Armour which is unobtainable. <br>
					- Shiny Cows advancement can now be gotten by breeding Enchanted Golden Apple Cows. <br>
					- Teleporting to the Crystal World now requires an empty inventory. You can disable this in the config. Teleporting out of the Crystal Dimension does not require an empty inventory. <br>
					- Added the "/chaosawakens" command. Syntax includes "website", "discord", "github", "wiki", "reddit" and "version". <br> <br>

					<b>IMPORTANT:</b> <br>
					- AttributeFix is now required.
					- Geckolib 3.0.77 is the required version of Geckolib.

					<b>Blocks:</b> <br>
					- Apple Log and Block of Platinum textures were changed. <br>
					- Added Skywood and Ginkgo Wood. <br>
					- Added Buttons, Fences, Fence Gates, Pressure Plates, Signs, Slabs, Stairs and Trapdoors for all woods from this mod. <br>
					- Peach Leaves now have their colour. Adding colour to the grey things in life. <br>
					- Added Salt Block. If ants walk on this block they will die. <br>
					- Added Ruby Ore in Blackstone. This has caused a rename for Nether Ruby Ore to Netherrack Ruby Ore. <br>
					- Gate Blocks no longer make loud anvil sounds when being dissipated. <br>
					- Leaves drop their fruit, saplings and sticks now. <br>
					- Uranium Ore no longer explodes. <br>
					- Crystal Furnace now requires Crystal Energy to be the fuel source it uses. <br>
					- Added Gate Blocks for all Vanilla Woods, Chaos Awakens Woods and Mushrooms. <br>
					- Gate Blocks have a new cool top texture! <br>
					- Updated Crystalworld Blocks, so they do not X-Ray in the Overworld. They also connect with each other. <br>
					- Added the Cyan Rose, Red Rose and Paeonia, the nostalgia is strong with this one. <br>
					- Added Potted Plants for all Chaos Awakens Flowers and Saplings. <br>
					- Added Radish and Lettuce Plants. <br>
					- Mining Level to break some Ores and Blocks have been updated. <br>
					- Gate Blocks and the Nest Blocks in Wasp Nests can now be obtained. <br>
					- Added Dense Grass Block, Dense Dirt and Dense Red Ant Nest. The Grass Blocks and Ant Nests for the Mining Paradise. <br>
					- Added Dense Grass, Tall Dense Grass, Thorny Sun, Blue Bulb, Purple Bulb, Pink Bulb. All are Plants for the Mining Paradise. <br>
					- Added Crystal Grass, Tall Crystal Grass Crystal Growths and Crystal Flowers. <br>
					- Added Leaf Carpets to all Vanilla and Chaos Awakens Leaf Blocks. <br>
					- Added Robo Blocks, Lamps and Pillars. (Slabs, Stairs and Walls!) [Unobtainable in Survival] <br>
					- Added Marble and Limestone and their Polished, Brick (Cracked and Mossy), Pillar and Chiseled variants. (Slabs, Stairs and Walls!) <br>
					- Added Bricks and Cracked Bricks for all Terracotta Colours. (Slabs, Stairs and Walls!) <br>
					- Lower DZ Ore Spawning rates in the overworld in case the overworld DZ ores are enabled. <br>
					- Updated the loot tables of copper, platinum, silver and tin. They no longer just drop their ores. <br> <br>

					<b>Items:</b> <br>
					- Amethyst, Titanium Ingot and Uranium Ingot textures were changed. <br>
					- Updated the Ultimate Pickaxe, Ultimate Axe, Ultimate Shovel and Ultimate Bow Textures. <br>
					- Ultimate Armour Model texture while being worn has been immensely updated. <br>
					- Queen Scale Armour now has enchantments by default just like Royal Guardian Armour. <br>
					- Added the Attitude Adjuster. Go EXPLODE some Mobs. <br>
					- Added the Slayer Chainsaw. Bye, Bye Wood. <br>
					- Battle Axe, Queen Scale Battleaxe have a new model when held. <br>
					- Added the Royal Guardian Sword. <br>
					- Added Mobzilla Scale Armour <br>
					- Added the Aluminium Nugget. <br>
					- Added Reach to the Attitude Adjuster, Battle Axe, Big Bertha, Prismatic Reaper, Queen Scale Battle Axe, Royal Guardian Sword and Slayer Chainsaw <br>
					- Removed Tree Seeds. <br>
					- Added Water Dragon Scale. <br>
					- Ultimate Gear Recipes now require Uranium and Titanium from Chaos Awakens and not just the forge:ingots/uranium and forge:ingots/titanium tags. Some other mods have these materials being much easier to get. It was kind of broken lol. <br>
					- Fixed Glint appearing on pre-enchanted tools after using a grindstone on them. <br>
					- Removed all Golden Foods except for the Plant ones. Added Golden Beetroot and Golden Baked Potato. <br>
					- Removed Silver, Gold and Platinum Coins. <br>
					- Added Venison and Cooked Venison. <br>
					- Added Crystal Carrots, Crystal Beetroot and Crystal Potatoes. <br>
					- Ultimate Apple is actually Ultimate now. Texture and Recipe updated. Also Updated its effects. <br>
					- Emerald Tools now all come pre-enchanted with Silk Touch just like the pickaxe. <br>
					- Ultimate Stuff comes enchanted with Unbreaking 3 instead of Unbreaking 2. Fixed/Changed other Enchantments as well. <br>
					- Rock Fish can no longer be eaten. They are still found in the Food Creative Tab. <br>
					- Nutrition and Saturation have been updated on a bunch of foods. <br>
					- Mining Level of some tools have been upped. <br>
					- Ultimate Shovel and Ultimate Axe right click abilities are now also 3x3 just like the Ultimate Hoe. <br>
					- Added the Critter Cage. It is not throwable, you just right-click the entity. There is an entity tag to blacklist entities from being picked up. The entity tag is "chaosawakens:critter_cage_blacklisted". Shows enchanted if you pick up an enchanted mob. <br>
					- Miners Dream can now break more blocks. <br>
					- Added Beetroot on a Stick, Crystal Beetroot on a Stick and Golden Beetroot on a Stick. <br>
					- Big Hammer not launches entities up based on their knockback resistance. Entities with a high knockback resistance will not go up as far as entities with low knockback resistance. <br> <br>

					<b>Entities:</b> <br>
					- Added the Bird. Has multiple texture variants. <br>
					- Added Carrot Pig, Golden Carrot Pig, Enchanted Golden Carrot Pig and Crystal Carrot Pig. You can put a saddle on them and ride them. <br>
					- Added a Crystal Gator. Has multiple texture variants. <br>
					- Added the Dimetrodon. Spawns in the Stalagmite Valley. Has multiple texture variants. <br>
					- Added the Green Fish, Rock Fish, Spark Fish, Wood Fish and Lava Eel. <br>
					- Added the Frog. Spawns in Swamps. If a frog is named "Froakie" it will become Blue. If a frog is spawned in the nether it will always be a hostile black frog. Has multiple texture variants. <br>
					- Added the Gazelle. Has multiple texture variants. <br>
					- Added the Robo Pounder. <br>
					- Added the Whale. <br>
					- Added drops for many of the entities above. You can view their drops using Just Enough Resources. <br>
					- Entities like the Ents, the Hercules Beetle and the Wasp now attack entities back if the entity attacks them first. <br>
					- Dark Oak Ent now drops a Cornflower. <br>
					- Jungle Ent can now drop Cocoa Beans. <br>
					- Fixed Spruce Ent dropping Oak Wood, it also drops Mossy Cobblestone now <br>
					- Removed vines from Oak Ent Loot Table. <br>
					- Updated Ent Models and Textures. Fixing various texture stitching issues as well. <br>
					- Enderman no longer spawn in the Crystal Dimension. <br>
					- Robo Warrior sometimes shoots Explosives now. <br>
					- Emerald Gator had a complete model and texture revamp. Also, Baby Emerald Gators can now happen by breeding two adults with any vanilla raw fish. <br>
					- Robo Entities now have a Layer that glows in the dark. <br>
					- Wandering Trader can now sell Triffid Goo making Battle Axe and Attitude Adjuster craft-able. <br>
					- Ants and Termites now die instantly in water. <br>
					- Ants and Termites now die instantly if they step on salt blocks. <br>
					- Ants and Termites no longer drop xp. <br>
					- Updated the message when clicking the Unstable and Brown Ants. It should now be more obvious that these dimensions have not been added yet. <br>
					- Enchanted Golden Apple Cow and Enchanted Golden Carrot Pig now breed non-enchanted versions if the enchanted animal breeding config is disabled. <br>
					- Add Wasp Ambient Sound. Protect your ears! <br>
					- Ranged Robo Entities will try to keep distance from the Player. <br>
					- All Apple Cow Variants will become their Carrot Pig Variant when struck by lightning. <br>
					- Robo Entities Only spawn if the block they spawn on can see the sky. (So they do not spawn inside the Mansion) <br>
					- Rabbits spawn the correct variants in Village Desert (Sandy Coloured One) and Village Snowy (White and White with Black Spot Ones). <br>
					- A Rabbit named "Oreo" will have a custom texture. Just like the already existing "Toast" Easter egg as well as the "Froakie" Easter egg on the new frog mob. <br>
					- Illusioner can now also drop a Totem of Undying. <br> <br>

					<b>Fossils:</b> <br>
					- Added a new block called the Copper Defossilizer. Can only defossilize stone and gravel fossilised mobs. <br>
					- Added a new block called the Iron Defossilizer. Can defossilize any fossilised, frozen or crystallized mobs. Is 4 times slower than the Copper Defossilizer. <br>
					- When right-clicking either Defossilizer the Interact with Defossilizer Statistic on the Statistics menu will be increased. <br>
					- Added a separate Creative Tab for Fossils. Upon launch of the game the icon for the Creative Tab has the chance to be either the Copper Defossilizer or the Iron Defossilizer. <br>
					- Added a new item called Aluminium Power Chip. <br>
					- Added Fossils for Many, Many Creatures. Normally going by the name "Fossilized (Mob Name)", If they are in ice it is "Frozen (Mob Name)" and if they are in Kyanite they are "Crystalised (Mob Name)". <br>
					- Fossils are no longer made into spawn eggs through the Crafting Table. <br>
					- To get Fossils you must now get a Defossilizer and when opening it you will see 3 input slots and the output slot. <br>
					- The top input slot is for the fossil. <br>
					- The bottom left input slot requires a water bucket (lava bucket for nether fossils). <br>
					- The last input slot requires the Aluminium Power Chip. <br> <br>

					<b>Advancements:</b> <br>
					- Robo Slayer Advancement now requires killing the Robo Pounder. <br>
					- Go Fish Advancement now requires killing the Green Fish. <br>
					- Fixed All Armors Advancement being unobtainable. Moth Scale Armour is no longer required. <br>
					- Added Advancement for obtaining a Defossilizer. <br> <br>

					<b>Misc:</b> <br>
					- The /chaosawakens command can now be used with /ca instead. <br>
					- A new syntax option for the /chaosawakens command is locate. This works like the vanilla locate command but only shows the structures from this mod and without the mod id. You can type /ca locate wasp_dungeon instead of /locate chaosawakens:wasp_dungeon. <br>
					- Changed enableEnchantedGoldenAppleCowBreeding config option to enableEnchantedAnimalBreeding. <br>
					- Support for Flammability and Compostability have been added for any items/blocks that need it. <br>
					- Spawn Eggs can not be used on a Spawner in Survival. There is a Config option to change this. <br>
					- Made more Blocks/Items into Fuel Sources. <br>
					- Added Separate Stats for interacting with the Crystal Crafting Table and Crystal Furnace. They no longer use interact with Crafting Table and Furnace Statistics in the Statistics menu. <br>
					- Attitude Adjuster explosion is customizable in the config just like the Freakin' Ray Gun and Thunder Staff explosions. <br>
					- Structures can now be disabled with the config. <br> <br>

					<b>World Generation:</b> <br>
					- Added Bamboo and Cocoa Beans to Jungle Ent Tree Chest Loot. <br>
					- Stalagmite Valley now spawns giant patches of Andesite and Gravel. <br>
					- Fixed Stronghold appearing in dimensions. <br>
					- Villagers are way more common in the Village Mania now. Mansions and Igloos also spawn here sometimes. <br>
					- Teleporting under bedrock when right-clicking ants should now be fixed. <br>
					- Corn and Tomato Plants are a bit less common. <br>
					- Strawberry bushes can spawn in forests. <br>
					- You can enter the Crystal World with items in your inventory if you are in creative. <br>
					- Fixed Warped Ent Dungeon containing Water Buckets instead of Lava Buckets in the Trap. <br>
					- Added Fog and Particles to Crystal World. <br>
					- The Crystal World was revamped with new plants.
					- Renamed Mining Biome to Dense Mountain and was completely revamped with new grass and dirt blocks and new plants. You look at this biome at night. It looks beautiful at night. <br>
					- Mineshafts can now spawn in the Mining Paradise. <br>
					- Fixed some vegetation in the Village Mania dimension. Acacia Trees actually generate in the Savanna. <br> <br>

					<b>Integration: (All mod names mentioned here have a link to their curseforge page.)</b> <br>
					- Added Defossilizer compatibility with <a href="https://www.curseforge.com/minecraft/mc-mods/jei">JEI</a> so you can see the recipes. The Defossilizers also have Information pages when viewing the recipes or uses of them. <br>
					- Added <a href="https://www.curseforge.com/minecraft/mc-mods/the-one-probe">The One Probe</a> compatibility so if you see a mob that has multiple textures The One Probe will say which variant it is and the id associated with the texture. <br>
					- Ant Infested Ores now show up as the ore they look like while using <a href="https://www.curseforge.com/minecraft/mc-mods/jade">Jade</a>. Just like the support that was added for The One Probe to do this in the April Fools Update. <br>
					- Added <a href="https://www.curseforge.com/minecraft/mc-mods/just-enough-resources-jer">Just Enough Resources</a> support for Ore World Generation settings. Ores that are disabled in the config do not show their World Generation Settings. <br>
					- Items that give effects are now shown in <a href="https://www.curseforge.com/minecraft/mc-mods/just-enough-effect-descriptions-jeed">Just Enough Effect Descriptions Effects</a> that show up in Just Enough Items if the mod is installed.`
        },
        {
            version: '0.10.0.1',
            mcVersion: '1.16.5',
            branch: 'stable',
            changelog: `
                    - Fixed a critical bug where you would crash if you hit any non-living entity with a weapon that has reach. <br>
					- Add recipe for the Slayer Chainsaw. <br>
					- For all the features of 0.10.0.0 see the changelog below this one.`
        },
        {
            version: '0.10.0.2',
            mcVersion: '1.16.5',
            branch: 'stable',
            changelog: `				
            - Fixed Critter Cage Default Filled Texture. <br>
			- Reverted the Uranium Texture to the old better one. <br>
			- Fixed a crash on servers with the extended reach tools.`
        },

        //ALPHA

        {
            version: '0.1',
            mcVersion: '1.16.5',
            branch: 'alpha',
            changelog: `
                    - Added Emerald Sword, Pickaxe, Shovel, Axe and Hoe. <br>
                    - Added Emerald Helmet, Chestplate, Leggings and Boots. <br>
					- Added Amethyst and Ruby. <br>
					- Added Untextured Tigers Eye, Titanium, Titanium Nugget, Uranium, Uranium Nugget and Aluminium. <br>
					- Added Untextured Ruby Block, Tigers Eye Block, Titanium Block, Uranium Block, Aluminium Block.`
        },
        {
            version: '0.2',
            mcVersion: '1.16.5',
            branch: 'alpha',
            changelog: `
                    - Added Amethyst Ore, Ruby Ore. <br>
					- Added Untextured Tigers Eye Ore, Titanium Ore, Uranium Ore and Aluminium Ore. <br>
					- Added Amethyst Sword, Pickaxe, Shovel, Axe and Hoe. <br>
					- Added Amethyst Helmet, Chestplate, Leggings and Boots. <br>
					- Added Ruby Sword, Pickaxe, Shovel, Axe and Hoe. <br>
					- Added Untextured Ruby Helmet, Chestplate, Leggings and Boots. <br>
					- Added Untextured Tigers Eye Sword, Pickaxe, Shovel, Axe and Hoe. <br>
					- Added Untextured Tigers Eye Helmet, Chestplate, Leggings and Boots.`
        },
        {
            version: '0.3',
            mcVersion: '1.16.5',
            branch: 'alpha',
            changelog: `
                    - Added Titanium Ore and Uranium Ore Textures. <br>
					- Added Amethyst Block, Ruby Block, Titanium Block and Uranium Block Textures. <br>
					- Added Titanium Ingot and Uranium Ingot Textures. <br>
					- Added Titanium Nugget and Uranium Nugget Textures. <br>
					- Added Ruby Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Updated Amethyst and Ruby Textures. <br>
					- Updated Amethyst Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Updated Amethyst Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Updated Ruby Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Updated Emerald Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Updated Emerald Helmet, Chestplate, Leggings and Boots Textures.`
        },
        {
            version: '0.4',
            mcVersion: '1.16.5',
            branch: 'alpha',
            changelog: `
                    - Added Aluminium Ore Textures. <br>
					- Added Tigers Eye Block and Aluminium Block Textures. <br>
					- Added Cooked Corndog, Raw Corndog, Cooked Bacon and Raw Bacon. <br>
					- Added Corn, Tomato, Lettuce, Cheese, Garden Salad and BLT. <br>
					- Added Aluminium Ingot Textures. <br>
					- Added Tigers Eye Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Ultimate Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Added Ultimate Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Thunder Staff. <br>
					- Added Tigers Eye Texture. <br>
					- Fixed Titanium, Uranium and Aluminium not having Ingot in their names.`
        },

        //BETA

        {
            version: '0.5',
            mcVersion: '1.16.5',
            branch: 'beta',
            changelog: `
                    - Added Ent. <br>
					- Added Tigers Eye Ore Texture. <br>
					- Added Tigers Eye Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Updated Tigers Eye Block, Titanium Block, Uranium Block and Aluminium Block Textures. <br>
					- Updated Titanium Ingot, Uranium Ingot and Aluminium Ingot Textures. <br>
					- Updated Titanium Nugget, Uranium Nugget Textures. <br>
					- Updated Tigers Eye Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Updated Tigers Eye Texture.`
        },
        {
            version: '0.6',
            mcVersion: '1.16.5',
            branch: 'beta',
            changelog: `
                    - Added Experience Sword. <br>
					- Added Experience Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Auto Enchants to Ultimate Set and Emerald Pickaxe.`
        },
        {
            version: '0.7',
            mcVersion: '1.16.5',
            branch: 'beta',
            changelog: `
                    - Added Creative Tabs. <br>
					- Added Cooked Peacock Leg, Raw Peacock Leg, Cooked Crab Meat and Raw Crab Meat. <br>
					- Added Strawberry, Peach, Radish, Radish Stew, Cherries Butter and Salt. <br>
					- Added Green Fish, Rock Fish, Wood Fish, Spark Fish and Lava Eel. <br>
					- Added Strawberry Seeds, Cherry Seeds, Apple Tree Seeds, Peach Seeds, Corn Seeds, Lettuce Seeds and Radish Seeds. <br>
					- Added Ultimate Bow. <br>
					- Added Nightmare Sword, Poison Sword, Rat Sword, Fairy Sword and Big Hammer. <br>
					- Added Prismatic Reaper. <br>
					- Added Salt Ore, Red Ant Infested Ore and Termite Infested Ore. <br>
					- Added Fossilised Ent, Fossilised Hercules Beetle, Fossilised Ruby Bug, Fossilised Emerald Gator. <br>
					- Added Gate Block and Ent Dungeon Wood. <br>
					- Added Ent Dungeon. <br>
					- Added Ent, Red Ant, Brown Ant, Rainbow Ant, Unstable Ant, Termite, Hercules Beetle, Ruby Bug, Emerald Gator, Robo Sniper, Beaver, Apple Cow and Golden Apple Cow. <br>
					- Added Iron Golem and Snow Golem Spawn Eggs. <br>
					- Added Ant Nests and Termite Nests. (UNUSED) <br>
					- Updated Cooked Corndog, Raw Corndog, Cooked Bacon and Raw Bacon Textures. <br>
					- Updated Corn, Tomato, Lettuce, Cheese and BLT Textures. <br>
					- Updated Ultimate Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Updated Lava Eel Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Updated Lapis Lazuli Helmet, Chestplate, Leggings and Boots Textures.`
        },
        {
            version: '0.7b',
            mcVersion: '1.16.5',
            branch: 'beta',
            changelog: '<u><b>UNKNOWN CHANGES</b></u>'
        },
        {
            version: '0.8',
            mcVersion: '1.16.5',
            branch: 'beta',
            changelog: `
                    - Updated Amethyst Ore and Ruby Ore Textures. <br>
					- Added Copper Ore, Tin Ore, Silver Ore, Platinum Ore, Sunstone Ore and Bloodstone Ore. <br>
					- Added Copper Block, Tin Block, Silver Block, Platinum Block, Sunstone Block and Bloodstone Block. <br>
					- Added Pink Tourmaline Block, Cat's Eye Block, Crystal Grass Block, Kyanite Block. <br>
					- Added Pink Tourmaline Cluster, Cat's Eye Cluster and Crystal Energy. <br>
					- Added Budding Pink Tourmaline and Budding Cat's Eye <br>
					- Added Crystal Log, Crystal Wood, Crystal Wood Planks, Red Crystal Leaves, Green Crystal Leaves and Yellow Crystal Leaves. <br>
					- Added Crystal Crafting Table and Crystal Furnace. <br>
					- Added Crystal Apple. <br>
					- Added Golden Foods. <br>
					- Added Candy Cane and Ultimate Apple. <br>
					- Added Copper Lump, Tin Lump, Silver Lump and Platinum Lump. <br>
					- Added Pink Tourmaline Ingot and Cat's Eye Ingot. <br>
					- Added Pink Tourmaline Nugget and Cat's Eye Nugget. <br>
					- Added Dead Irukandji, Peacock Feather and Crystal Wood Shard. <br>
					- Added Irukandji Arrow, Skate String Bow and A Freakin' Ray Gun. <br>
					- Added Crystal Torch and Sunstone Torch. <br>
					- Added Copper Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Added Copper Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Tin Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Added Tin Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Silver Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Added Silver Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Platinum Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Added Platinum Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Peacock Feather Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Crystal Wood Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Added Kyanite Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Added Pink Tourmaline Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Added Pink Tourmaline Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Cat's Eye Sword, Pickaxe, Shovel, Axe and Hoe Textures. <br>
					- Added Cat's Eye Helmet, Chestplate, Leggings and Boots Textures. <br>
					- Added Instant Survival Shelter. <br>
					- Added Extra Small Zoo Cage, Small Zoo Cage, Medium Zoo Cage, Large Zoo Cage and Extra Large Zoo Cage. <br>
					- Added Robo Warrior, Enchanted Golden Apple Cow and Crystal Apple Cow. <br>
					- Ant Nests and Termite Nests now have Biome Dependent coloring. <br>
					- Item and Food Creative Tabs are now separate. <br>
					- Removed Ent Dungeon Wood.`
        },
        {
            version: '0.8b',
            mcVersion: '1.16.5',
            branch: 'beta',
            changelog: '<u><b>UNKNOWN CHANGES</b></u>'
        },
        {
            version: '0.8c',
            mcVersion: '1.16.5',
            branch: 'beta',
            changelog: '- Added Extreme Torch.'
        },
        {
            version: '0.8d',
            mcVersion: '1.16.5',
            branch: 'beta',
            changelog: '- Added Random Teleport Block.'
        },
    ]

    function compare(a, b) {
        var i, cmp, len;
        a = (a.version + '').split('.');
        b = (b.version + '').split('.');
        len = Math.max(a.length, b.length);
        for( i = 0; i < len; i++ ) {
            if( a[i] === undefined ) {
                a[i] = '0';
            }
            if( b[i] === undefined ) {
                b[i] = '0';
            }
            cmp = parseInt(a[i], 10) - parseInt(b[i], 10);
            if( cmp !== 0 ) {
                return (cmp < 0 ? -1 : 1);
            }
        }
        return 0;
    };

    downloads.sort(compare);
    downloads.sort((a,b) => (a.branch > b.branch) ? 1 : ((b.branch > a.branch) ? -1 : 0)).reverse();
    
</script>

<Title title='Downloads'/>

<h3>
	<a href="https://www.curseforge.com/minecraft/mc-mods/geckolib/">GeckoLib</a> and <a href="https://www.curseforge.com/minecraft/mc-mods/attributefix">AttributeFix</a> are required for the mod to function!
</h3>

<div class="versions">
    {#each downloads as download}
        <details>
            <!-- svelte-ignore a11y-label-has-associated-control -->
            <summary>
                {#if download.branch == 'stable'}
                    <a href="downloads/chaosawakens-{download.mcVersion}-{download.version}.jar">
                        <h3>ChaosAwakens - {download.mcVersion} - {download.version}</h3>
                    </a>
                {:else if download.branch == 'alpha'}
                    <a href="downloads/ChaosAwakensAlpha{download.mcVersion}v{download.version}.jar">
                        <h3>ChaosAwakens Alpha - {download.mcVersion} - {download.version}</h3>
                    </a>
                {:else}
                    <a href="downloads/ChaosAwakensBeta{download.mcVersion}v{download.version}.jar">
                        <h3>ChaosAwakens Beta - {download.mcVersion} - {download.version}</h3>
                    </a>
                {/if}
            </summary>
            <p>
                {@html download.changelog}
            </p>
        </details>
    {/each}
</div>

<style lang="scss">

	h3 {
		text-align: center;
	}

    details {
        user-select: none;
        width: 50%;
        margin: 30px auto;
        //border-style: solid;
        border-color: white;
        border-radius: 10px;
        box-shadow: 3px 3px 5px rgb(0, 0, 0);
        background-color: rgba(0, 0, 0, 0.50);

        &[open] {
            summary:after {
                content: "➖";
            }
        }

        summary {
            display: flex;
            cursor: pointer;
            background-color: rgba(0, 0, 0, 0.50);
            padding: 30px;
            justify-content: space-between;

            h3 {
                color: rgb(255, 255, 255);
            }

            &:after {
                content: "➕";
            }

            &::-webkit-details-marker {
                display: none;
            }
        }

        p {
            color: rgb(150, 150, 150);
            padding: 30px;
        }
    }
</style>