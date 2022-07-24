# Contribs

_Contribs_ are optional code snippets and systems contributed by
the Evennia community. They vary in size and complexity and
may be more specific about game types and styles than 'core' Evennia.
This page is auto-generated and summarizes all contribs currently included.

All contrib categories are imported from `evennia.contrib`, such as

    from evennia.contrib.base_systems import building_menu

Each contrib contains installation instructions for how to integrate it
with your other code. If you want to tweak the code of a contrib, just
copy its entire folder to your game directory and modify/use it from there.

> Hint: Additional (potentially un-maintained) code snippets from the community can be found
in our discussion forum's [Community Contribs & Snippets](https://github.com/evennia/evennia/discussions/categories/community-contribs-snippets) category.

If you want to contribute yourself, see [here](../Contributing.md)!


## base_systems

_This category contains systems that are not necessarily tied to a specific
in-game mechanic but is useful for the game as a whole. Examples include
login systems, new command syntaxes, and build helpers._

```{toctree}
:maxdepth: 1

Contrib-AWSStorage.md
Contrib-Building-Menu.md
Contrib-Color-Markups.md
Contrib-Components.md
Contrib-Custom-Gametime.md
Contrib-Email-Login.md
Contrib-Ingame-Python.md
Contrib-Menu-Login.md
Contrib-Mux-Comms-Cmds.md
Contrib-Unixcommand.md
```


### Contrib: `awsstorage`

_Contrib by The Right Honourable Reverend (trhr), 2020_

This plugin migrates the Web-based portion of Evennia, namely images,
javascript, and other items located inside staticfiles into Amazon AWS (S3)
cloud hosting. Great for those serving media with the game.

[Read the documentation](./Contrib-AWSStorage.md) - [Browse the Code](evennia.contrib.base_systems.awsstorage)



### Contrib: `building_menu`

_Contrib by vincent-lg, 2018_

Building menus are in-game menus, not unlike `EvMenu` though using a
different approach. Building menus have been specifically designed to edit
information as a builder. Creating a building menu in a command allows
builders quick-editing of a given object, like a room. If you follow the
steps to add the contrib, you will have access to an `edit` command
that will edit any default object, offering to change its key and description.

[Read the documentation](./Contrib-Building-Menu.md) - [Browse the Code](evennia.contrib.base_systems.building_menu)



### Contrib: `color_markups`

_Contrib by Griatch, 2017_

Additional color markup styles for Evennia (extending or replacing the default
`|r`, `|234`). Adds support for MUSH-style (`%cr`, `%c123`) and/or legacy-Evennia
(`{r`, `{123`).

[Read the documentation](./Contrib-Color-Markups.md) - [Browse the Code](evennia.contrib.base_systems.color_markups)



### Contrib: `components`

__Contrib by ChrisLR 2021__

# The Components Contrib

[Read the documentation](./Contrib-Components.md) - [Browse the Code](evennia.contrib.base_systems.components)



### Contrib: `custom_gametime`

_Contrib by vlgeoff, 2017 - based on Griatch's core original_

This reimplements the `evennia.utils.gametime` module but with a _custom_
calendar (unusual number of days per week/month/year etc) for your game world.
Like the original, it allows for scheduling events to happen at given
in-game times, but now taking this custom calendar into account.

[Read the documentation](./Contrib-Custom-Gametime.md) - [Browse the Code](evennia.contrib.base_systems.custom_gametime)



### Contrib: `email_login`

_Contrib by Griatch, 2012_

This is a variant of the login system that asks for an email-address
instead of a username to login. Note that it does not verify the email,
it just uses it as the identifier rather than a username.

[Read the documentation](./Contrib-Email-Login.md) - [Browse the Code](evennia.contrib.base_systems.email_login)



### Contrib: `ingame_python`

_Contrib by Vincent Le Goff 2017_

This contrib adds the ability to script with Python in-game. It allows trusted
staff/builders to dynamically add features and triggers to individual objects
without needing to do it in external Python modules. Using custom Python in-game,
specific rooms, exits, characters, objects etc can be made to behave differently from
its "cousins". This is similar to how softcode works for MU or MudProgs for DIKU.
Keep in mind, however, that allowing Python in-game comes with _severe_
security concerns (you must trust your builders deeply), so read the warnings in
this module carefully before continuing.

[Read the documentation](./Contrib-Ingame-Python.md) - [Browse the Code](evennia.contrib.base_systems.ingame_python)



### Contrib: `menu_login`

_Contribution by Vincent-lg 2016. Reworked for modern EvMenu by Griatch, 2019._

This changes the Evennia login to ask for the account name and password as a series
of questions instead of requiring you to enter both at once. It uses Evennia's 
menu system `EvMenu` under the hood.

[Read the documentation](./Contrib-Menu-Login.md) - [Browse the Code](evennia.contrib.base_systems.menu_login)



### Contrib: `mux_comms_cmds`

_Contribution by Griatch 2021_

In Evennia 1.0+, the old Channel commands (originally inspired by MUX) were
replaced by the single `channel` command that performs all these functions.
This contrib (extracted from Evennia 0.9.5) breaks out the functionality into 
separate Commands more familiar to MU* users. This is just for show though, the 
main `channel` command is still called under the hood.

[Read the documentation](./Contrib-Mux-Comms-Cmds.md) - [Browse the Code](evennia.contrib.base_systems.mux_comms_cmds)



### Contrib: `unixcommand`

_Contribution by Vincent Le Geoff (vlgeoff), 2017_

This module contains a command class with an alternate syntax parser implementing
Unix-style command syntax in-game. This means `--options`, positional arguments
and stuff like `-n 10`. It might not the best syntax for the average player
but can be really useful for builders when they need to have a single command do
many things with many options. It uses the `ArgumentParser` from Python's standard
library under the hood.

[Read the documentation](./Contrib-Unixcommand.md) - [Browse the Code](evennia.contrib.base_systems.unixcommand)






## full_systems

_This category contains 'complete' game engines that can be used directly
to start creating content without no further additions (unless you want to)._

```{toctree}
:maxdepth: 1

Contrib-Evscaperoom.md
```


### Contrib: `evscaperoom`

_Contribution by Griatch, 2019_

A full engine for creating multiplayer escape-rooms in Evennia. Allows players to
spawn and join puzzle rooms that track their state independently. Any number of players
can join to solve a room together. This is the engine created for 'EvscapeRoom', which won
the MUD Coders Guild "One Room" Game Jam in April-May, 2019. The contrib has no game
content but contains the utilities and base classes and an empty example room.

[Read the documentation](./Contrib-Evscaperoom.md) - [Browse the Code](evennia.contrib.full_systems.evscaperoom)






## game_systems

_This category holds code implementing in-game gameplay systems like
crafting, mail, combat and more. Each system is meant to be adopted
piecemeal and adopted for your game. This does not include
roleplaying-specific systems, those are found in the `rpg` folder._

```{toctree}
:maxdepth: 1

Contrib-Barter.md
Contrib-Clothing.md
Contrib-Cooldowns.md
Contrib-Crafting.md
Contrib-Gendersub.md
Contrib-Mail.md
Contrib-Multidescer.md
Contrib-Puzzles.md
Contrib-Turnbattle.md
```


### Contrib: `barter`

_Contribution by Griatch, 2012_

This implements a full barter system - a way for players to safely
trade items between each other in code rather than simple `give/get`
commands. This increases both safety (at no time will one player have 
both goods and payment in-hand) and speed, since agreed goods will 
be moved automatically). By just replacing one side with coin objects,
(or a mix of coins and goods), this also works fine for regular money 
transactions.

[Read the documentation](./Contrib-Barter.md) - [Browse the Code](evennia.contrib.game_systems.barter)



### Contrib: `clothing`

_Contribution by Tim Ashley Jenkins, 2017_

Provides a typeclass and commands for wearable clothing. These 
look of these clothes are appended to the character's description when worn.

[Read the documentation](./Contrib-Clothing.md) - [Browse the Code](evennia.contrib.game_systems.clothing)



### Contrib: `cooldowns`

_Contribution by owllex, 2021_

Cooldowns are used to model rate-limited actions, like how often a
character can perform a given action; until a certain time has passed their
command can not be used again. This contrib provides a simple cooldown
handler that can be attached to any typeclass. A cooldown is a lightweight persistent
asynchronous timer that you can query to see if a certain time has yet passed.

[Read the documentation](./Contrib-Cooldowns.md) - [Browse the Code](evennia.contrib.game_systems.cooldowns)



### Contrib: `crafting`

_Contribution by Griatch 2020_

This implements a full crafting system. The principle is that of a 'recipe',
where you combine items (tagged as ingredients) create something new. The recipe can also
require certain (non-consumed) tools. An example would be to use the 'bread recipe' to
combine 'flour', 'water' and 'yeast' with an 'oven' to bake a 'loaf of bread'.

[Read the documentation](./Contrib-Crafting.md) - [Browse the Code](evennia.contrib.game_systems.crafting)



### Contrib: `gendersub`

_Contribution by Griatch 2015_

This is a simple gender-aware Character class for allowing users to
insert custom markers in their text to indicate gender-aware
messaging. It relies on a modified msg() and is meant as an
inspiration and starting point to how to do stuff like this.

[Read the documentation](./Contrib-Gendersub.md) - [Browse the Code](evennia.contrib.game_systems.gendersub)



### Contrib: `mail`

_Contribution by grungies1138 2016_

A simple Brandymail style mail system that uses the `Msg` class from Evennia
Core. It has two Commands for either sending mails between Accounts (out of game)
or between Characters (in-game). The two types of mails can be used together or
on their own.

[Read the documentation](./Contrib-Mail.md) - [Browse the Code](evennia.contrib.game_systems.mail)



### Contrib: `multidescer`

_Contribution by Griatch 2016_

A "multidescer" is a concept from the MUSH world. It allows for
creating, managing and switching between multiple character
descriptions and is a way for quickly managing your look (such as when 
changing clothes) in more free-form roleplaying systems. This will also 
work well together with the `rpsystem` contrib.

[Read the documentation](./Contrib-Multidescer.md) - [Browse the Code](evennia.contrib.game_systems.multidescer)



### Contrib: `puzzles`

_Contribution by Henddher 2018_

Intended for adventure-game style combination puzzles, such as combining fruits
and a blender to create a smoothie. Provides a typeclass and commands for objects 
that can be combined (i.e. used together). Unlike the `crafting` contrib, each 
puzzle is built from unique objects rather than using tags and a builder can create 
the puzzle entirely from in-game.

[Read the documentation](./Contrib-Puzzles.md) - [Browse the Code](evennia.contrib.game_systems.puzzles)



### Contrib: `turnbattle`

_Contribution by Tim Ashley Jenkins, 2017_

This is a framework for a simple turn-based combat system, similar
to those used in D&D-style tabletop role playing games. It allows
any character to start a fight in a room, at which point initiative
is rolled and a turn order is established. Each participant in combat
has a limited time to decide their action for that turn (30 seconds by
default), and combat progresses through the turn order, looping through
the participants until the fight ends.

[Read the documentation](./Contrib-Turnbattle.md) - [Browse the Code](evennia.contrib.game_systems.turnbattle)






## grid

_Systems related to the game world's topology and structure. This has
contribs related to rooms, exits and map building._

```{toctree}
:maxdepth: 1

Contrib-Extended-Room.md
Contrib-Mapbuilder.md
Contrib-Simpledoor.md
Contrib-Slow-Exit.md
Contrib-Wilderness.md
Contrib-XYZGrid.md
```


### Contrib: `extended_room`

_Contribution - Griatch 2012, vincent-lg 2019_

This extends the normal `Room` typeclass to allow its description to change 
with time-of-day and/or season. It also adds 'details' for the player to look at 
in the room (without having to create a new in-game object for each). The room is 
supported by new `look` and `desc` commands.

[Read the documentation](./Contrib-Extended-Room.md) - [Browse the Code](evennia.contrib.grid.extended_room)



### Contrib: `mapbuilder`

_Contribution by Cloud_Keeper 2016_

Build a game map from the drawing of a 2D ASCII map.

[Read the documentation](./Contrib-Mapbuilder.md) - [Browse the Code](evennia.contrib.grid.mapbuilder)



### Contrib: `simpledoor`

_Contribution by Griatch, 2016_

A simple two-way exit that represents a door that can be opened and
closed from both sides. Can easily be expanded to make it lockable, 
destroyable etc. 

[Read the documentation](./Contrib-Simpledoor.md) - [Browse the Code](evennia.contrib.grid.simpledoor)



### Contrib: `slow_exit`

_Contribution by Griatch 2014_

An example of an Exit-type that delays its traversal. This simulates
slow movement, common in many games. The contrib also
contains two commands, `setspeed` and `stop` for changing the movement speed
and abort an ongoing traversal, respectively.

[Read the documentation](./Contrib-Slow-Exit.md) - [Browse the Code](evennia.contrib.grid.slow_exit)



### Contrib: `wilderness`

_Contribution by titeuf87, 2017_

This contrib provides a wilderness map without actually creating a large number
of rooms - as you move, you instead end up back in the same room but its description 
changes. This means you can make huge areas with little database use as
long as the rooms are relatively similar (name/desc changing).

[Read the documentation](./Contrib-Wilderness.md) - [Browse the Code](evennia.contrib.grid.wilderness)



### Contrib: `xyzgrid`

_Contribution by Griatch 2021_

Places Evennia's game world on an xy (z being different maps) coordinate grid.
Grid is created and maintained externally by drawing and parsing 2D ASCII maps,
including teleports, map transitions and special markers to aid pathfinding.
Supports very fast shortest-route pathfinding on each map. Also includes a
fast view function for seeing only a limited number of steps away from your
current location (useful for displaying the grid as an in-game, updating map).

[Read the documentation](./Contrib-XYZGrid.md) - [Browse the Code](evennia.contrib.grid.xyzgrid)






## rpg

_These are systems specifically related to roleplaying
and rule implementation like character traits, dice rolling and emoting._

```{toctree}
:maxdepth: 1

Contrib-Dice.md
Contrib-Health-Bar.md
Contrib-RPSystem.md
Contrib-Traits.md
```


### Contrib: `dice`

_Contribution by Griatch, 2012_

A dice roller for any number and side of dice. Adds in-game dice rolling
(`roll 2d10 + 1`) as well as conditionals (roll under/over/equal to a target)
and functions for rolling dice in code. Command also supports hidden or secret
rolls for use by a human game master.

[Read the documentation](./Contrib-Dice.md) - [Browse the Code](evennia.contrib.rpg.dice)



### Contrib: `health_bar`

_Contribution by Tim Ashley Jenkins, 2017_

The function provided in this module lets you easily display visual
bars or meters as a colorful bar instead of just a number. A "health bar"
is merely the most obvious use for this, but the bar is highly customizable
and can be used for any sort of appropriate data besides player health.

[Read the documentation](./Contrib-Health-Bar.md) - [Browse the Code](evennia.contrib.rpg.health_bar)



### Contrib: `rpsystem`

_Contribution by Griatch, 2015_

A full roleplaying emote system. Short-descriptions and recognition (only
know people by their looks until you assign a name to them). Room poses. Masks/disguises
(hide your description). Speak directly in emote, with optional language obscuration
(words get garbled if you don't know the language, you can also have different languages
with different 'sounding' garbling). Whispers can be partly overheard from a distance. A 
very powerful in-emote reference system, for referencing and differentiate targets 
(including objects).

[Read the documentation](./Contrib-RPSystem.md) - [Browse the Code](evennia.contrib.rpg.rpsystem)



### Contrib: `traits`

_Contribution by Griatch 2020, based on code by Whitenoise and Ainneve contribs, 2014_

A `Trait` represents a modifiable property on (usually) a Character. They can
be used to represent everything from attributes (str, agi etc) to skills
(hunting 10, swords 14 etc) and dynamically changing things like HP, XP etc. 
Traits differ from normal Attributes in that they track their changes and limit
themselves to particular value-ranges. One can add/subtract from them easily and
they can even change dynamically at a particular rate (like you being poisoned or
healed).

[Read the documentation](./Contrib-Traits.md) - [Browse the Code](evennia.contrib.rpg.traits)






## tutorials

_Helper resources specifically meant to teach a development concept or
to exemplify an Evennia system. Any extra resources tied to documentation
tutorials are found here. Also the home of the Tutorial World demo adventure._

```{toctree}
:maxdepth: 1

Contrib-Batchprocessor.md
Contrib-Bodyfunctions.md
Contrib-Evadventure.md
Contrib-Mirror.md
Contrib-Red-Button.md
Contrib-Talking-Npc.md
Contrib-Tutorial-World.md
```


### Contrib: `batchprocessor`

_Contibution by Griatch, 2012_

Simple examples for the batch-processor. The batch processor is used for generating 
in-game content from one or more static files. Files can be stored with version 
control and then 'applied' to the game to create content.

[Read the documentation](./Contrib-Batchprocessor.md) - [Browse the Code](evennia.contrib.tutorials.batchprocessor)



### Contrib: `bodyfunctions`

_Contribution by Griatch, 2012_

Example script for testing. This adds a simple timer that has your
character make small verbal observations at irregular intervals.

[Read the documentation](./Contrib-Bodyfunctions.md) - [Browse the Code](evennia.contrib.tutorials.bodyfunctions)



### Contrib: `evadventure`

_Contrib by Griatch 2022_

A complete example MUD using Evennia. This is the final result of what is
implemented if you follow the Getting-Started tutorial. It's recommended
that you follow the tutorial step by step and write your own code. But if
you prefer you can also pick apart or use this as a starting point for your
own game.

[Read the documentation](./Contrib-Evadventure.md) - [Browse the Code](evennia.contrib.tutorials.evadventure)



### Contrib: `mirror`

_Contribution by Griatch, 2017_

A simple mirror object to experiment with. It will respond to being looked at.

[Read the documentation](./Contrib-Mirror.md) - [Browse the Code](evennia.contrib.tutorials.mirror)



### Contrib: `red_button`

_Contribution by Griatch, 2011_

A red button that you can press to have an effect. This is a more advanced example 
object with its own functionality and state tracking.

[Read the documentation](./Contrib-Red-Button.md) - [Browse the Code](evennia.contrib.tutorials.red_button)



### Contrib: `talking_npc`

_Contribution by Griatch 2011. Updated by grungies1138, 2016_

This is an example of a static NPC object capable of holding a simple menu-driven
conversation. Suitable for example as a quest giver or merchant.

[Read the documentation](./Contrib-Talking-Npc.md) - [Browse the Code](evennia.contrib.tutorials.talking_npc)



### Contrib: `tutorial_world`

_Contribution by Griatch 2011, 2015_

A stand-alone tutorial area for an unmodified Evennia install.
Think of it as a sort of single-player adventure rather than a
full-fledged multi-player game world. The various rooms and objects
are designed to show off features of Evennia, not to be a
very challenging (nor long) gaming experience. As such it's of course
only skimming the surface of what is possible. Taking this apart 
is a great way to start learning the system.

[Read the documentation](./Contrib-Tutorial-World.md) - [Browse the Code](evennia.contrib.tutorials.tutorial_world)






## utils

_Miscellaneous, optional tools for manipulating text, auditing connections
and more._

```{toctree}
:maxdepth: 1

Contrib-Auditing.md
Contrib-Fieldfill.md
Contrib-Random-String-Generator.md
Contrib-Tree-Select.md
```


### Contrib: `auditing`

_Contribution by Johnny, 2017_

Utility that taps and intercepts all data sent to/from clients and the
server and passes it to a callback of your choosing. This is intended for 
quality assurance, post-incident investigations and debugging.

[Read the documentation](./Contrib-Auditing.md) - [Browse the Code](evennia.contrib.utils.auditing)



### Contrib: `fieldfill`

_Contribution by Tim Ashley Jenkins, 2018_

This module contains a function that generates an `EvMenu` for you - this
menu presents the player with a form of fields that can be filled
out in any order (e.g. for character generation or building). Each field's value can 
be verified, with the function allowing easy checks for text and integer input, 
minimum and maximum values / character lengths, or can even be verified by a custom 
function. Once the form is submitted, the form's data is submitted as a dictionary 
to any callable of your choice.

[Read the documentation](./Contrib-Fieldfill.md) - [Browse the Code](evennia.contrib.utils.fieldfill)



### Contrib: `random_string_generator`

_Contribution by Vincent Le Goff (vlgeoff), 2017_

This utility can be used to generate pseudo-random strings of information
with specific criteria.  You could, for instance, use it to generate
phone numbers, license plate numbers, validation codes, in-game security 
passwords and so on. The strings generated will be stored and won't be repeated.

[Read the documentation](./Contrib-Random-String-Generator.md) - [Browse the Code](evennia.contrib.utils.random_string_generator)



### Contrib: `tree_select`

_Contribution by Tim Ashley Jenkins, 2017_

This utility allows you to create and initialize an entire branching EvMenu
instance from a multi-line string passed to one function.

[Read the documentation](./Contrib-Tree-Select.md) - [Browse the Code](evennia.contrib.utils.tree_select)







----

<small>This document page is auto-generated. Manual changes
will be overwritten.</small>