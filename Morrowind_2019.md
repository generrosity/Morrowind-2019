This is a changing guide. While complete, it is still very open to changes and new sections.

# Morrowind 2019: Thastus Edition

The [README](https://github.com/Tyler799/Morrowind-2019/blob/master/README.md), License and other info can be found in the rest of the repo. If you want to discuss this guide, we have a [Discord](https://discord.me/mwmods) channel called #thastus.

## Table of Contents

* [1.0 Introduction](#introduction)
   * [1.1 Before We Begin](#before-we-begin)
   * [1.1 Regarding Open Morrowind (OpenMW)](#regarding-open-morrowind)
   * [1.2 Regarding Mods With BEthesda Archives (.BSA)](#regarding-mods-with-bethesda-archives)
   * [1.3 Regarding Mod Organizer 2](#regarding-mod-organizer-2)
   * [1.4 Regarding Russian Websites](#regarding-russian-websites)
   * [1.5 Regarding Bump mapped mods](#bump-mapped-mods)
   * [1.6 Regarding MWSE](#MWSE---The-Morrowind-Script-Extender)
   * [1.7 Regarding Atlasing](#Atlasing---What-It-Is-And-Installation-Concerns)
   * [1.8 Regarding Mlox and Sorting Mods](#Regarding-Mlox-and-Sorting-Mods)
* [2.0 Non-Graphical Mods](#non-graphical-mods)
   * [2.1 Baseline Installation and Boilerplate](#baseline-installation-and-boilerplate)
   * [2.2 Patches, Fixes and Otherwise](#patches-fixes-and-otherwise)
   * [2.3 Official Bethesda Plugins](#official-bethesda-plugins)
   * [2.4 Dialogue Mods](#dialogue-mods)
   * [2.5 User Interface](#user-interface)
       * [2.5.1 Dialogue Font](#Dialogue-Font)
       * [2.5.2 HD Video Screen Replacers](#HD-Video-Screen-Replacers)
       * [2.5.3 Splash Screen Replacers](#Splash-Screen-Replacers)
   * [2.6 Major Mods To Be Aware Of](#major-mods-to-be-aware-of)
* [3.0 Graphical Mods Begin](#graphical-mods-begin)
   * [3.1 Mesh fixes and improvements](#mesh-fixes-and-improvements)
   * [3.2 Nature Texture & Mesh Replacers](#nature-texture--mesh-replacers)
       * [3.2.1 Want plants To Not "Bend" Or "Grow" Towards You?](#want-plants-to-not-bend-or-grow-towards-you)
   * [3.3 Graphic Herbalism Finisher](#Graphic-Herbalism-Finisher)
   * [3.4 Weather](#weather)
   * [3.5 Architecture Replacers](#architecture-replacers)
   * [3.6 Miscellaneous Replacers](#miscellaneous-replacers)
   * [3.7 Creature Replacers](#creature-replacers)
   * [3.8 Heads & Bodies](#heads--bodies)
   * [3.9 Clothing replacers](#clothing-replacers)
   * [3.10 Weapons](#weapons)
   * [3.11 Armor](#armor)
   * [3.12 Animations](#animations)
* [4.0 Conclusion and Wrapping Up](#conclusion-and-wrapping-up)
   * [4.1 Testing Your Setup](#testing-your-setup)
   * [4.2 MGE XE Setup](#mge-xe-setup)
   * [4.3 Cleaning Mods](#cleaning-mods)
   * [4.4 Creating A Multipatch](#creating-a-multipatch)
* [5.0 Aftercare](#aftercare)
   * [5.1 Updating Masters, Syncing and Repairing your Saves](#updating-masters-syncing-and-repairing-your-saves)
   * [5.2 Load Order](#load-order)
* [6.0 Misc Other Info](#misc-other-info)
   * [6.1 Other Mods](#other-mods)
   * [6.2 Screenshots](#screenshots)
   * [6.3 Contributors](#contributors)

# Introduction

## Before We Begin

**You must have an official copy of the base game! Pirated/torrented copies will *not* work!** You need an official CD, the Steam version, or the GOG version. This isn't just hearsay, this is true of every Bethesda game Morrowind and forward. All mod tools (LOOT/BOSS, Mod Organizer, Wyre Bash, MWSE/OBSE/SKSE, xEdit, etc) and even many mods themselves just don't work properly on unofficial copies of the game. The exact reasoning is fairly technical in explanation, but it's not an anti-piracy measure, it's just a fact of the game engine and how tools hook in. I'm not inherently anti-piracy, I actually think it has a lot of value for several reasons. However, for the sake of this guide, if you don't have an official copy you can expect everything to break. You likely won't even be able to start the game properly. As a veteran player of the series, **I offer exactly 0 help if you don't have an official copy**.

**You should always read the mod page or glance through the readme of any mod we're downloading**, so you'll at least be aware of what you're getting and what your options are. Mod are, above all else, personal preference. Knowledge is power!

### Regarding Open Morrowind

Open Morrowind ([OpenMW](https://openmw.org/en/)) is an open-source engine created by fans for Morrowind. It performs significantly better than Morrowind's original engine, while also fixing many bugs and issues the original had while offering enhancements and new functionality - like multiplayer support.

While many of the mods here may be compatible with OpenMW, many are not. Do not attempt to follow this guide with OpenMW! It is an amazing accomplishment by the community, but this guide is not attuned to it.

### Regarding Mods With Bethesda Archives

Mods with archives (.BSA files) need to be added into the `Morrowind.ini` file. However, we have a tool to automate the process that can be found [here](http://download.fliggerty.com/download-58-633)

An example for handling it manually, using my_test_mod, which has a file called `neat.BSA`:

```INI
[Archives]
Archive 0=Tribunal.bsa
Archive 1=Bloodmoon.bsa
Archive 2=neat.bsa
```

NOTE: You must edit the `Morrowind.ini` inside your Mod Organizer profile that you're playing on for it to have any effect. Assuming you didn't rename it, it's under `Morrowind/Mod Organizer 2/Profiles/Default/Morrowind.ini`.

### Regarding Mod Organier 2 (MO2):

**Mod Organizer 2** is a mod organization tool, similar to Wyre Mash, Oblivion Mod Manager, Vortex, Kortex, Nexus Mod Manager or others. However, it is a far better tool than most of them and is the tool of choice for this guide. It makes maintaining massive, complicated load orders a breeze. 

If you would like an excellent tutorial series for using Mod Organizer 2, I recommend [this one](https://www.youtube.com/watch?v=ruq6hQIAvB8&list=PLlN8weLk86Xh3ue76x2ibqtmMramwQmHB) by Gamerpoets. You can also ask on the Mod Organizer 2 discord, [here](https://discordapp.com/invite/5tCqt6V), or even on the Skyrimmods discord if you like. 

All installation of mods (with minor exception, mainly for tools like MGE/MCP/Mlox) will be done with this tool, which has  had built-in support for Morrowind for some time now. It is highly recommended, as it allows you to very easily disable files/folders or mods, supports subfolders within mods, re-order mods or plugins and otherwise. It makes maintenance of a large mod list effortless, hence its heavy adoption in the Skyrim modding scene. (Do not substitute with NMM, Vortex or otherwise. Seriously. It *will* break things.)

With MO2 you will *never* need to reinstall a mod or the base game if it is used properly, no matter how badly you mess up. 

However: [Wrye Bash (Polemo's Fork)](https://www.nexusmods.com/morrowind/mods/45439/) is an *excellent* alternative. While a little less friendly at face value, it offers a similar ability to revert the game and mods to their base state upon revising your list. It's a fantastically made tool, and we'll be installing it anyways for some of its feature set. (Note: You *cannot* use both to manage mods - either one or the other. If you're following our MO2 steps, you'll only use Wrye to make multipatches and to clean mods. Installing mods through both *will* cause issues. Don't do it.)

Note that mods not on the nexus (like the various links to .ZIP or .7ZIP files) can be and should be installed via Mod Organizer 2 as well. It provides an "Install Mod From Archive" button in the top left that will handle this for you, with a couple exceptions I mention in the guide. 

Because we're using MO2, the order you install and enable mods is meaningless. You can change the order of mods in the left-hand pane and right-hand pane at any time. The left hand pane defines which files (like textures, sounds, meshes) will take priority, while the right pane defines which plugins (and thus which records) will take priority. 

Mod Organizer 2 has INI files for each profile you create. This means that if you try to edit files like Skyrimprefs.ini or otherwise, you will find they have no effect - unless you modify the ones inside MO2's profiles folders. MO2 also offers a button in the GUI to directly edit the INI files if you like. 

**Note**: When I say "Disable" regarding a file, I'm referring to the "HIDE" feature MO2 gives. If the guide says to "Disable" a file or folder, that means "HIDE" it. However, the original guide had a lot of "DELETE" wording. I simply find/replaced that with "DISABLE". There are likely many instances where with using MO2 disabling like the original guide suggested is unnecessary - just let another mod take priority. However, I have no way of knowing immediately which disables would be pointless, so I'm leaving them in for now

**Warning**: Do *not* enable "Automatic Archive Invalidation" when using Mod Organizer 2 for Morrowind profile. This is needed for a bug introduced in Oblivion. However, if used in Morrowind it *will* break things like Distant Land generation. 

**"NO GAME DATA AT TOP LEVEL** is common for many Morrowind mods. All this means is that the folder structure of the mod is not exactly what Mod Organizer 2 is expecting. MO2 provides a small tutorial on this warning and the fix is very easy. Just expand the folder inside the warning, and look for the "Data Files" folder. Right click it and select "Set Data Directory", while will fix the warning. Some Morrowind mods however include patches in other directories in the mod, and for those we must manually un-zip the archive, move the relevant files, and then re-zip it and install via MO2 as normal. I will warn you when this needs to occur. 

### Regarding Russian Websites:

Some of the websites used in this guide are only in Russian. The ones that do should have a fairly obvious download button, but Chrome out-of-the-box offers a translate feature that may help you, and Firefox can also perform the translation via something [like this](https://addons.mozilla.org/en-US/firefox/addon/simple-translate/) or other, similar tools. 

For your own safety downloading files anywhere on the web (especially a site where you cannot easily read the text), I highly recommend you install a competent ad-blocker like [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/). 

### Bump-mapped mods:

A lot of links in this guide will have bump map versions available, especially once we hit the architecture section. I don't know all the technical details of it, but bump mapping in Morrowind isn't quite like what you'd expect it to be. It's often very shiny looking, sometimes plastic-y, and it can make things look very bright depending on the reflection texture used. This is fine for metals and wet looking plants (it looks great on mushrooms, in my opinion), but can sometimes look a little weird on architecture. That means, if you ever have a choice between getting a bump map or no bump map version, the choice is 100% yours. If you do download a bump map version and decide you don't like it, you can get rid of the bumps by deleting the meshes that were included in the mod, and you can also disable the normal maps (usually they have `_nm` or `_n` at the end of their filename) if you want to save space.

### MWSE - The Morrowind Script Extender:

Momentarily in this guide, we'll have you install MWSE. Based on the name alone, many of you will realize this is similar to the projects OBSE and SKSE, though it is maintained by a completely different team.

Here is a short summary of what it is:

>The Morrowind Script Extender adds new functionality to the scripting language of Morrowind, allowing for new features to be implemented into the game. 

It comes with its own updater, and the latest versions are distributed on their Discord, which the mod page links to. 

MWSE, along with MWSE-LUA, offers amazing functionality in the game that was previously completely impossible.

However, as with most things script-related, this does mean hard-incompatibility with OpenMW. As stated earlier, if you plan on using OpenMW with the guide, no support is offered. However if you do, realize that MWSE and any MWSE mods will be off-the-table if you do so and keep that in mind as you move forward. 


### Atlasing - What It Is And Installation Concerns:

This description from the Project Atlas page sums up what and why fairly nicely:

>Vanilla Morrowind has objects split into different shapes each using its own unique texture. This is bad for performance and is one of the game's primary FPS bottlenecks. Each shape (even within a single mesh file) requires its own draw call. There are close to 5,000 different textures in Morrowind's data; many of which are very similar or outright identical and some meshes are split into more than 75 different shapes. Merging those meshes into a single shape which references a single texture atlas is the ideal situation for game performance.

In essence, atlasing just means: Turn many textures or meshes into *one* thing to make the game run better.

However, there is a catch.

Several mods (Project Atlas Included) provide you with Atlased versions of some textures or meshes. That's great on its own. But what happens if you have several re-textures or some mesh improvements *after* the Atlased versions? In this case, the Atlased version will do nothing. As well, these Atlases don't cover everything in the game to start with.

How can we remedy this?

Project Atlas some with batch scripts (.bat) that generates Atlased textures for *one specific area*, if you put it in a folder with all of the textures that it needs. In a normal non-MO2 or Wrye install, we could just move the .bat file into our `Textures` folder and we'd be golden. However...that won't work here in a virtualized environment.

What is the solution? Well, you could dig through and find whatever is currently winning texture-wise for all of the texture files needed by that area. Then, copy them all into some temporary folder, drop the .BAT in, and move the result into its own mod. For obvious reasons, this is super impractical, both for us to write as instruction as well as for you to perform. Not only that, you'd need to re-do this process over if you re-ordered, deleted or added any mods that touched those textures.

We're looking into better solutions at the moment, and any thoughts are appreciated. However, for the moment, we're skipping out on this. That means if you choose to use Atlased versions for mods, just be aware that if there's a conflict down the line you may not get the performance boost you thought you would. 

### Regarding Mlox and Sorting Mods:

For those of you coming from other titles, you may be familiar with tools such as BOSS or LOOT. Morrowind existed prior to those tools, and the one that came to prominence was [Mlox](https://github.com/mlox/mlox/releases/). While it is not perfect and the masterlist is highly out-of-date with modern mods and load orders, it is likely still the best tool. Support for Morrowind is work-in-progress by the LOOT team, but frankly not many of them play Morrowind and few community members have contributed to it so it's at a standstill.

Mlox has many warnings which you should safely ignore. If you want to edit it yourself, you can find its masterlist in ```AppData\Local\mlox\mlox\mlox_base.txt```. 

# Non-Graphical Mods

## Baseline Installation and Boilerplate

Note: MO2 can't handle the installation of this section, and will warn you accordingly.

1. Wipe any previous install, any tools, folders, etc. Everything must be clean.

2. Install the game, preferably not in Program Files for technical reasons to do with Windows permissions. If using steam, you can find information about this [here](https://support.steampowered.com/kb_article.php?ref=7418-YUBN-8129)

Make sure to run the game *at least once* to make sure it's registered on your computer properly.

If you are using the GOTY edition, no patches are necessary. If you have some ancient disc version, the Tribunal patch is [here](http://download.zenimax.com/elderscrolls/morrowind/patches/tribunal_v1.4.1313.exe) and the Bloodmoon patch is [here](http://download.zenimax.com/elderscrolls/morrowind/patches/Bloodmoon_v1.6.1820.exe).

3. Download the latest Morrowind Code patch. You must download the base [here](http://www.nexusmods.com/morrowind/mods/19510/) and then over-write its files with the 2.5b4 patch [here](https://www.nexusmods.com/morrowind/mods/26348).

Extract it in your game directory and run 'Morrowind Code Patch.exe'. Read through the patches, but the most important ones should be checked already. You might be interested in some of the game mechanic changing options--toggle sneak is great! For a modern install, make sure to check 'Bump/reflect map local lighting' under Graphics changes. If you want to download HD cutscene replacers, check 'Hi-def cutscene support' under Mod related features. If you want to try a sound overhaul mod later (like Morrowind Acoustic Overhaul) make sure to check 'Scripted music uninterruptible' and 'Separate axe inventory sounds'.

4. Timeslips' EXE optimizer has been removed for this guide, determined to be essentially ineffectual. (Though not harmful, from what I can tell)

5. Manually installing the 4GB patch is no longer required, as it has been rolled into Morrowind Code Patch as of a recent version. However, running it against MGEXEGui.exe may improve its performance when generating distant land. The patcher can be downloaded [here](https://www.ntcore.com/4gb_patch.php)

6. Download the latest version of MGE XE. Its mod page can be found [here](https://www.nexusmods.com/morrowind/mods/41102) and the development version (like MCP) was previously hosted [here](https://www.nexusmods.com/morrowind/mods/26348). This comes with an optional plugin `XE Sky Variations.esp`, that will randomize the sky colour and sunrise/sunset every day. It requires high quality sky scattering enabled, and MWSE enabled. Use it if you want.

(As of writing this guide, the mod page has the newest version, Skunk Works' copy is older (despite having a higher version number). Check both first though, as it could change!)

Consider patching it with the 4GB patch if distant land generation takes too long when you get to that step.

MGE XE used to come with MWSE 2.0, but now includes alpha 2.1 as part of the installer and updater. Some mods require the alpha version (2.1) to work properly. You can find the latest MWSE downloads here: [here](https://nullcascade.com/mwse/mwse-dev.zip).
New versions of MWSE 2.1 come out daily/weekly, and it comes with a MWSE-Update program that will download any new alpha version, if available. Visit the Morrowind Modding Discord under #MWSE for more information. To report issues, visit the Discord channel or their [GitHub project](https://github.com/MWSE/MWSE/issues).

Extract it into your install folder (the folder with Morrowind.exe in it)--not the data folder! This should result in MGEXEgui ending up in the same folder as Morrowind.exe.

Run MGEXEgui, choose your resolution and settings from the first tab (don't forget to click the Auto FOV button). I don't recommend messing with shaders at this time, and don't even bother clicking on the Distant Land tab; that's going to be one of our final steps. The In-Game tab lets you edit some .ini settings easily. Choose whatever you want. For lighting settings, use the following (from Knots' [old guide](https://vsrecommendedgames.fandom.com/wiki/Morrowind_Modding)):
Quadratic 2.619
Linear 1.0
Constant 0.382

7. Download mlox. You should get the latest version of it from [here](https://github.com/mlox/mlox/releases/) (They migrated away from Sourceforge some time ago)

mlox is the Morrowind equivalent of LOOT or BOSS, and it needs to go into its own folder in your Morrowind install. Mine is in `Morrowind\mlox`. Run the application and hit "update load order". You should get into the habit of doing this after you install mods that require an .esp to be activated. **NOTE:** Mlox often refuses to work properly the first time, or sometimes intermittently. At this point in the install, it has a green 'already optimized' warning scrolled offscreen. Just re-start your computer, it'll work again.

mlox is currently highly out of date, even using version 1.0. It suggests the Morrowind Patch Project (despite those links no longer working) and has other outdated information. However, it does form a good baseline and has some information still relevant you can at least look into if it warns you.

Alternatively, there is some work to support Morrowind by the LOOT team [here](https://github.com/loot/morrowind) and contributions are highly welcome.

9. Install [Wrye Mash - Polemos' Fork](https://www.nexusmods.com/morrowind/mods/45439/)

This is a powerful tool that will allow us to handle conflict resolution, cleaning saves, updating masters and otherwise.

To do this, first download the "Manual Installation Archive"

Then, extract it. The contents (`Data Files` and the Wyre program folder `Mopy`) should be put into your `Morrowind` directory, so that the Data files merges with the vanilla `Data Files` folder.

NOTE: YOU MUST RUN WRYE ONCE MANUALLY BEFORE RUNNING IT INSIDE MO2.

An installer will pop up. Point it to Morrowind's folder and Mlox if you like, and the "Mod Archives" can just be any random folder, doesn't matter which one. It'll be ignored later anyways.

10. Download [TES3CMD](https://github.com/john-moonsugar/tes3cmd/releases)

This is a powerful command-line tool that allows you to determine which mods need cleaning and clean them, reducing crashes, broken mods and otherwise.

HOWEVER: DO NOT ATTEMPT TO JUST CLEAN YOUR ENTIRE LOAD ORDER! Some mods *will* break upon being cleaned. I personally, carefully went through the mods and determined (mainly through their readme's) which plugins could not be safely cleaned. I will instruct you on which plugins to clean later in this guide.

Install it by putting it in the `Data Files` folder.

8. Download [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194)
(The latest dev versions can be found on the MO2 Discord, but as of writing this, 2.2.1 is perfectly fine for Morrowind use)

Extract it so that the `Mod Organizer 2 (Archive)` folder is inside your Morrowind installation folder.

Then, go ahead and run Mod Organizer.exe. It should pop up asking you about a couple things. You'll want to choose a "PORTABLE" install (unless you're much more familiar with MO2 and know what you're doing) and when it asks you about which game you want to manage, navigate to the `Steam/steamapps/common/Morrowind` folder.

It should look like [this](https://i.imgur.com/WWbBKJZ.png)

Under the dropdown for "Morrowind" is where other executables can be put. You won't need to do this much for Morrowind. However, you'll notice that in that dropdown MGE XE has already been placed! Hurrah!

However, you'll also want to add Mlox and Wrye Bash to that list, so that they can actually see what mods you have installed. (I'm not doing to delve too far into how to use MO2 in this guide, there's a million resources on that already)

Now when you need to run MGE XE, Mlox and Wrye, do it through MO2. MGE XE may ask for elevation, that's perfectly normal. If you want to avoid that error message, you can set it to run as administrator on your own.

Congratulations, you've completed the baseline installation for Morrowind!

**Before you continue:** I would highly recommend launching the game for a second time. You knew it worked vanilla, now you should test and make sure it works with all this boilerplate work you've done. If it does, you can go on to installing mods.

At this point you can take a 'clean' backup of the Morrowind game directory.

## Patches, Fixes and Otherwise

A note before we start installing mods:

MO2 allows you to use the "Download with Manager" option on the nexus pages that have it, then you can double click to install. Feel free to use this to save time. Of course, MO2 can install archives one at a time using the second to leftmost top button with a CD on it. Once installed, you can enable the mod and its plugins (ESPs) by ticking a mod's checkbox in the left hand pane **or** by selecting several mods in the left-band-pane, right clicking one of them, and selecting "enable selected".

If the version number shows up in red as you begin installing mods, I recommend that you right click them and hit "Ignore Update". This will happen due to some mod authors having poorly laid out versioning for their mods, making a mod show up as "out of date" despite you just installing it. This isn't harmful in any way, but if you do this *now* then when you hit "Check all for updates" in the future you'll actually have a pretty good idea if any of your Nexus mods have updates available. Very useful! Later we you do detect updates you will need to RightClick and select 'Visit on Nexus' to redownload, install, and 'replace'.

1. You may be familiar with projects like the Unofficial Patches for Oblivion and Skyrim. Morrowind *sort of* has its own versions of these in the form of two options: the Morrowind Patch Project and the Patch for Purists. The MPP makes a lot of balance-related changes some players feel is untrue to the original experience. Thus, currently most players recommend the Patch for Purists which you can get [here](https://www.nexusmods.com/morrowind/mods/45096/)

(Note: Mlox, due to being old and outdated, will complain because you don't have the Patch Project installed. If this bothers you, you can remove this message by going into Mlox_base.txt, and removing the section for the Patch Project. It will not longer message you about it, which is nice.)

2. Go ahead and get the following mods:

* [Texture Fix 2.0](http://mw.modhistory.com/download-90-10353) - Repairs landscape seams
* [Texture Fix Extended](https://www.nexusmods.com/morrowind/mods/46018)
* [Texture Fix - Bloodmoon 1.1](http://mw.modhistory.com/download-90-10388) - Repairs landscape seams on Solstheim. (You'll need to disable this mod if you choose to install Solstheim - Tomb of the Snow Prince later in this guide)
* [Bloated Caves](http://www.nexusmods.com/morrowind/mods/43141/) - Adds bloatspores (a plant) to Morrowind. Bloatspores were included in the game files but not placed in the world.

One of the following:
* [Delayed Dark Brotherhood Attack Add-On 2.0](http://mw.modhistory.com/download-90-7300) - Delays the Tribunal main quest from staring until certain "immersive" requirements are met. Does NOT work with Rebirth!
* [Dark Brotherhood Delay - Player's Choice](https://www.nexusmods.com/morrowind/mods/46533) - Delays the Tribunal main quest from starting until either a level condition is met, or you've completed the main quest depending on what option you choose. Does work with Rebirth. 

## Official Bethesda Plugins

Bethesda made several official plug-ins for Morrowind. Unfortunately, they have some problems. While you can download their vanilla versions individually, it's recommended to instead download a patch version of all of them. (You can easily disable the plugins you dislike in MO2)

There are two main options for fixed version of these addons:

- [Unofficial Morrowind Official Plugins Patched](https://www.nexusmods.com/morrowind/mods/43931) - This is the most up-to-date option that comes with compatibility patches for various big mods. You need the main file and optionally "Merged and Compatibility versions for UMOPP" as well. I personally recommend the optional compatibility merged file as it gives you wider compatibility with other mods you might use in the future. If you do use it, choose the "`UMOPP Compatibility Merged` in the BAIN installer. Remember to disable the main package plugins if you are using the merged version. If for some reason you don't want to use specific addons, you shouldn't use the merged version and just load the *Compatibility ESPs* after the main package.

- [WHReaper's Morrowind Official Plugins](http://download.fliggerty.com/download-13-1079) ([Mirror](https://web.archive.org/web/*/http://download.fliggerty.com/file.php?id=1079)) - Some of the folders have optional components, usually with higher res textures, glow maps, or normal maps. Feel free to install all of the optional folders. To install, you'll need to download the archive, merge any optional folders into their parent mod folder, and then pack them into .7Zip or .zip files, which you then can install via MO2 as normal)

You can read about the official add-ons [here](http://www.uesp.net/wiki/Morrowind:Official_Plug-ins)

## Dialogue Mods

1. First and foremost you should get the [LGNPC](http://lgnpc.org/downloads)

Download the LGNPC bundle. You should install all of the mods. A few notes:

* If you download the "all in one" it is indeed not properly archived for installation. It also includes old versions of several of the mods. You'll need to extract it, then delete the archives inside for the older copies, then install each individually. My recommendation is just to skip the "all in one" and download the latest versions of each individually.
* If you want to avoid wereguars, skip LGNPC Pelagiad. It's one of their earliest mods and it really shows.
* Make sure to read LGNPC Soul Sickness Patch's readme. It's optional, so decide on your own if you want it or not.
* The plugin "LGNPC_SecretMasters_MCA5.esp" is only relevant if you have Morrowind Comes Alive. If you do not, make sure to right click the "Secret masters" mod and turn this ESP from "Available ESPs" to "Optional ESPs", or just make it hidden.
* The Soul Sickness patch comes bundled with Pax Redoran, and does not need to be installed separately.

2. Get the Less Generic modules. These give the main quests of Morrowind, Tribunal and Bloodmoon the LGNPC treatment and are fantastic. It does tend to make some of the quests a little trickier, though.

* [Less Generic Nerevarine](http://www.nexusmods.com/morrowind/mods/23335/)
* [Less Generic Tribunal Restored](https://www.nexusmods.com/morrowind/mods/44819) (This is a fixed version of Less Generic Tribunal that doesn't need several patches)
* [Less Generic Bloodmoon](http://www.nexusmods.com/morrowind/mods/23346/) - Comes with one patch for users of Thirsk Expanded, and one patch for users of **both** Thirsk Expanded and Children of Morrowind, and finally the main plugin. Make sure to enable the main plugin, and one of the two patches if appropriate. (For reference, this guide installs neither TE nor CoM)

3. A few extra mods to add even more to the dialogue of the game:
* [Django's Dialogue](http://www.nexusmods.com/morrowind/mods/37328/)
* [Nastier Camonna Tong](http://www.nexusmods.com/morrowind/mods/22601/)
* [What Thieves Guild?](http://mw.modhistory.com/download-87-13858)

## User Interface

- [Ultimate Icon Replacer](https://www.nexusmods.com/morrowind/mods/36948/). This replaces all Morrowind object/inventory icons with better icons. Mods you install further down the line will take priority over some of these.

* Alternatives, for potions and scrolls you may want [Potions and Scrolls](http://mw.modhistory.com/download-35-2339). Take a look at the screenshots of both and decide for yourself. If you do want "Potions and Scrolls" just load it directly after Ultimate Icon Replacer. Note this is in ACE archive format which MO2 can't directly open, nor can 7zip which it is based upon. Bitzipper, WinRar, Bandizip, PeaZip and PowerArchiver will all open it, at which point you would re-pack the mod as a .7zip or .zip to install it via MO2. 

- [JiFFY Morrowind UI Revamped](http://www.nexusmods.com/morrowind/mods/43922/?). This UI mod was chosen in particular because of how much it revamps, and it looks nice to boot. Choose between Dark or Classic, pick your crosshair and choose any size options. I went with 50% smaller crosshair and 25% smaller cursor, but you can and should try all the sizes in game to see which you prefer. Optionally for those avid readers, this mod includes the mod "Scroll Daedric Alphabet". This mod gives you a key to read the Daedric characters on spell scrolls. Lastly, don't forget to make the necessary changes to your .ini.

- [Spell Scroll Text Overhaul](https://www.nexusmods.com/morrowind/mods/42936) gives unique Daedric text to all spell scrolls, making them far more interesting to read if you added Scroll Daedric Alphabet in the JiffyUI install.

- [UI Expansion](https://www.nexusmods.com/morrowind/mods/46071) - Expands UI functionality with searching, filtering, and more visual feedback.	Has compact and expanded views. A very nice mod. 

### Dialogue Font

Get your dialogue font mods of choice:

* Start with [Better Dialogue fonts](http://www.nexusmods.com/morrowind/mods/36873/), which makes the standard Morrowind font (Magic Cards) higher resolution. Consider the mods below afterwards if you wish.

* [MORRA BUF - MORe ReadAble Bigger UI Fonts](http://www.nexusmods.com/morrowind/mods/42934/) - This is an alternative to Better Dialogue Font if you dislike the "Magic Cards" font. Take note of the .ini changes you'll need to do.

### HD Video Screen Replacers

Get any or all of these if you like:

* [HD Intro Cinematic - English](http://www.nexusmods.com/morrowind/mods/39329/) - Make sure to pick the right one for your resolution, and only get this if you picked the proper option in MCP. To install, you need to rename the movie file to `mw_intro.bik` after installing it via MO2.
* [Morrowind Bethesda Logo HD Makeover](http://www.nexusmods.com/morrowind/mods/42352/) - If you have 'skip intro movie' turned on in MGE XE, there's no point to downloading this. In order to install, you'll need to make a folder called `Video` and drop the `bethesda logo.bik` file into it.
* No references to other ingame video replacement yet.

### Splash Screen Replacers

Choose either 

* one mod that replaces BOTH the main menu AND the loading screens (1 total)
* one mod that JUST replaces the main menu AND another mod that JUST replaces the loading screens (2 total)

Mods that replace JUST the main menu:

* [2015 Main Menu Background Replacers](http://www.nexusmods.com/morrowind/mods/43923/) - These look absolutely gorgeous, and in most cases would be the ones I would recommend first when it comes to the main menu. Only choose one.

* [Animated Main Menu for Morrowind](http://www.nexusmods.com/morrowind/mods/43341/) - This is a really pretty main menu. The downside is that it's a 300 mb file. I personally don't want to waste that much space on the main menu, but if you don't care about that this may be a good option.

Mods that replace JUST the loading screens:

* [Concept Art Based Loading Screens](http://www.nexusmods.com/morrowind/mods/43603/) - For splash screens, this would be my personal recommendation. If you like the look of the primary replacer but can't stand the Russian writing, you may enjoy this.

* [Fresco Splash Screens](https://www.nexusmods.com/morrowind/mods/45680) - This is a set of 14 splash screens showing off Tyddy's frescoes. They are very vanilla friendly and quite minimalistic. Editors personal choice.

* [Morrowloading](http://www.nexusmods.com/morrowind/mods/44364/) - If you want splash screens with tidbits of information, like in Oblivion and Skyrim. Note that the screenshots used by this mod differ occasionally from how your game will look following this guide.

Mods that replace both:

* [HD Concept-art Splash Screen and Main Menu](http://www.nexusmods.com/morrowind/mods/43081/) - Skip this if you absolutely can't stand the Russian writing on the splash screens, but the screens look amazing enough that you should overlook it. To install, you'll just need to set the "Data Files" section as the Data directory when installing via MO2, then it works fine.

* [Morrowind Screens Redone](https://www.nexusmods.com/morrowind/mods/46259) - An English alternative to the above, based on the same concept art. Looks a bit different, compare their images and decide yourself.

## Major Mods To Be Aware Of

The following mods are optional to install, but have compatibility patches listed in the mesh/texture replacers we'll soon be downloading, so I'm listing them here. Read up on them and decide if you want to use them or not.

* [Tamriel Data](http://www.nexusmods.com/morrowind/mods/44537/?) - This is a requirement for the below mod. Download the HD version.
* [Tamriel Rebuilt](http://www.nexusmods.com/morrowind/mods/42145/?) - One of the biggest mods in Morrowind and still a work in progress, but it adds a huge chunk of playable landscape (mainland Morrowind). This guide does not offer support for Tamriel Rebuilt as it is a massive overhaul and touches nearly everything in the base game. A few of the mods listed here do have patches expressly for TR but not all of them do - run TR with this guide at your own risk. 
* [Graphic Herbalism - MWSE Edition](https://www.nexusmods.com/morrowind/mods/46599) - By default, plants in Morrowind act as containers: when you activate them, the container interface opens and you can remove any ingredients that might be present 'inside' the plant. Graphic Herbalism MWSE is an updated version of an old mod that makes plants act more like plants; activating the plant picks it, you automatically get the ingredients, and the plant changes in the world to show it has been picked. Think Skyrim plants. Ignore the `GH Patches and Replacers` file, that needs to be later. Note the Atlas mod is suggested being installed before this mod.
* [Glow in the Dahrk](https://www.nexusmods.com/morrowind/mods/45886/) is essentially a replacement for WinDoors Glow. Highly recommended.

(I personally chose the High-res and rays options, and left the rest off)

However: If you want to use it you *must* have MWSE alpha 2.1 or later. It will not work with 2.0!

# Graphical Mods Begin

## Mesh fixes and Improvements

* [Morrowind Optimization Patch](https://www.nexusmods.com/morrowind/mods/45384) - Improves performance by optimizing meshes.
* [Project Atlas](https://www.nexusmods.com/morrowind/mods/45399) - Improves performance by merging meshes into a single shape, reducing draw calls significantly for the same visual quality. Now is a compbined download - select all BAIN options except ASL Urns. (Dunmeri urns will cover this). As the mod is still in Alpha, the Discord suggested Mod order is Optimization Patch>Glow in the Dahrk>Project Atlas (with GitD patches>Mesh & Texture replacers>Graphic Herbalism MWSE
* [Better Meshes plus Optimization](http://www.nexusmods.com/morrowind/mods/38170/?)
* [Dwemer Mesh Improvement](http://www.nexusmods.com/morrowind/mods/43101/?)
* [Mesh Improvements Optimized](http://download.fliggerty.com/download-56-1088)
* [RR Mod Series - Better Meshes](http://www.nexusmods.com/morrowind/mods/43266/?) - Get the RR - Better Meshes V1.2 file, `Fix for misc_com_metal_plate_05`, `Fix for artifact_bittercup_01` and `Fix for misc_dwrv_artifact60`. Before installing, disable `meshes/m/misc_com_pillow_01` from the main mod. 
* [MOAR Mesh Replacers](http://www.nexusmods.com/morrowind/mods/44057/?)

For the `ATL BC Mushrooms`, make sure to choose just `00 Core - Smoothed Meshes`.

For the Velothi and Imperial mods, you'll need to go into the `Extras` folder, then into the `GITD` folder and copy the meshes folder next to the mods main `Meshes` folder, if you are using the mod Glow in the Dahrk. 

## Nature Texture & Mesh Replacers

This is by far going to be the most complicated part of the guide so hold on to your butts.

* [Morrowind Visual Pack](http://mw.modhistory.com/download-56-6990) ([Alternate Download](https://www.nexusmods.com/morrowind/mods/44311)) - This is our base mod. It replaces a lot of stuff that still isn't touched by modern mods, mostly because they're not really used often enough to think about replacing. Most of the textures will be overwritten.

### Bitter Coast Region

* [Connary's Bitter Coast](http://www.fullrest.ru/files/connarysbittercoast)
* [Apel's Bitter Coast Retexture](http://www.nexusmods.com/morrowind/mods/42661/?)

Feel free to start the game and check out Seyda Neen if you'd like, but we're not done and the Bitter Coast landscape will be changing more later as we add tree, plant and new landscape textures.

### Connary Packs

While we're at it, lets get a few more Connary packs. Some of this stuff will end up overwritten later; that's fine.

* [Connary's Grazelands](http://www.fullrest.ru/files/connarysgrazelands)
* [West Gash](http://www.fullrest.ru/files/connaryswestgash)
* [Webs](http://www.fullrest.ru/files/connaryswebs)
* [Caves](http://www.fullrest.ru/files/connaryscaves)

### Rocks

Time for rocks. Download the following:

* [Correct UV rocks v1.4](https://www.nexusmods.com/morrowind/mods/46104)
* [WIP Smooth Correct UV Rocks](http://forums.bethsoft.com/topic/1514660-alternatives-to-on-the-rocks/?p=23908143)
* [Ore Rock Retexture ORR](http://mw.modhistory.com/download-56-12942)
* [correctUV Diverse Ore veins v1.0](http://mw.modhistory.com/download-56-13484)

### Waterfalls

Test each waterfall mod quickly by starting the game, pressing `` ` `` to go into the console, typing `COC "Vivec, Puzzle Canal, Level 1"`, hitting enter, and leaving through the grate ahead of you.
* [Better Waterfalls](https://www.nexusmods.com/morrowind/mods/45424) - Best looking ones out there. Editors personal choice. Be sure to grab the [Waterfalls Tweaks](https://www.nexusmods.com/morrowind/mods/46271) for better compatibility.
* [Waterfalls Bump mapped](http://www.nexusmods.com/morrowind/mods/42405/?) - Author's personal choice.
* [Dongle's Waterpack Bumpmapped](http://www.nexusmods.com/morrowind/mods/42317/?) - Some may like how these look.

### Fire and Smoke

* [Apel's Fire Retexture](http://www.nexusmods.com/morrowind/mods/42554/?)
* [Vurt's Lava and Smoke](http://www.nexusmods.com/morrowind/mods/28519/?) - Just choose the "SMOKE" option in the BAIN installer. (Though you could choose the others, they'll be lower priority than lava mods we'll be installing later and thus shouldn't come into effect)

### Trees

#### Bitter Coast Trees

* [Vurt's Bitter Coast Trees II](http://www.nexusmods.com/morrowind/mods/37489/?)
* [Vurt's Bitter Coast Trees II - Remastered and Optimized](https://www.nexusmods.com/morrowind/mods/46418) - Fixes a good deal of Vurt's Bitter Coast Trees II and improves their performance. You no longer need the BC Trees Collision fix or the Bitter Coast folder of Vurt's Tree Fix by Greatness7. This is a patch so you will need to place it just bellow the original mod in your load order.

#### Grazeland Trees

* [Vurt's Grazelands Trees I](http://www.nexusmods.com/morrowind/mods/35368/?)

* [Vurt's Grazeland Trees II](http://www.nexusmods.com/morrowind/mods/37038/?) 

Pick the one you like best. I prefer the first option, and I use the palms free version. Make sure to move **one** of the ESPs out of the Optional section using MO2, depending on which you want.

#### Ascadian Isles Trees

Use only one of the following two mods:

* [Remiros' Ascadian Isles Trees 2](https://www.nexusmods.com/morrowind/mods/45779) - If you care about optimization, this should be your preferred choice of trees for this region. They are not only better for performance, but also more vanilla friendly.
* [Vurt's Ascadian Isles Trees Replacer II](http://www.nexusmods.com/morrowind/mods/37249/?) - These are not optimized and will have a medium impact on your performance in Ascadian Isles. They also require patching to correct some mesh problems. However some might prefer them over Remiros trees. Make sure to get the newer file (10a).

If you've chosen to go for the Vurt option you'll need to install this fix: 

* [Vurt's Trees Fix by Greatness7](https://www.dropbox.com/s/rwtjc7stx1gbeje/VurtsTreesFix.7z?dl=0) - Install the meshes from the `Ascadian Isles` folder only. Leafy West Gash can be disabled if you're following this guide as we used different trees. Only use the Grazelands folder if you're using Grazelands II. You'll need to re-pack these, as they aren't correctly archived. In each folder, all the .NIF files should be in a `Meshes/f` folder. Make sure to set them up that way and re-pack them, then install as normal.

#### Mournhold Trees

The following two are the recommended tree replacers for the Mournhold region. They are well optimized and quite beautiful. I would recommend merging these two mods into one called "Vurt's Mournhold Trees". If you noticed that they contain some duplicate textures that's fine, just overwrite them.

* [Vurt's Mournhold Trees II](http://www.nexusmods.com/morrowind/mods/35400/?)

* [Vurt Mournhold Dead Trees](https://www.nexusmods.com/morrowind/mods/45770)

Alternatively you can choose CptJoker's Flora Redux:

* [Mournhold Flora Redux](https://www.nexusmods.com/morrowind/mods/45805) - Highly-detailed trees and grass textures for Mournhold. These should be very performance heavy as they have a whopping 10 times more detail then vanilla trees, use them only if your rig can handle it. Get the "MFR - Trees" or "MFR - Alternative" file.

#### Solstheim Trees

* [Vurt's Solstheim Tree Replacer II](http://www.nexusmods.com/morrowind/mods/37856/?) - Make sure to also download the "Fixed Collision" patch. You can install this patch seperately, just make sure to move its files into a `/Meshes/f` folder, or drop them into that folder from the original mod. Be sure to install the following fix as well:
* [Vurt's Solstheim Tree Replacer II Fix](https://www.nexusmods.com/morrowind/mods/45941) - Fixes `Meshes/f/Flora_tree_BM_snow_01.nif`

#### West Gash Trees

For the West Gash trees, you have two options. Vurt's look nicer, in my opinion, but Vanilla-friendly West Gash is MUCH more... well, vanilla friendly. Only use ONE of the mods offered below.

- [Vanilla-friendly West Gash Tree Replacer](http://www.nexusmods.com/morrowind/mods/44173/?) - As with the Ascadian Isles trees, this should be your preferred choice of trees for this region due to problems Vurt's trees tend to have. I recommend using the darker leaf texture found in the `extras` folder.

* [Vurts Leafy West Gash II](http://www.nexusmods.com/morrowind/mods/37400/?) - Make sure to get the newer file. Do NOT download the bridge rope textures.

### Plants

* [Underwater Static Replacer](http://mw.modhistory.com/download-56-11998)
* [Better Barnacles](http://www.nexusmods.com/morrowind/mods/43605/?)
* [Plant life retexture](http://www.nexusmods.com/morrowind/mods/37947/?)
* [Bloatspore retexture](http://www.nexusmods.com/morrowind/mods/42384/?) - We already have a better bloatspore mesh, so just get the 'simple retexture' file. Unless you REALLY want bump/glow mapped bloatspores for some reason, but you'll have a less smooth bloatspore as a result.
* [flora_bush_01 replacer](http://www.nexusmods.com/morrowind/mods/42941/?) - Get the 1.3 file, and I highly recommend grabbing the 1k texture optional file because 2k textures for a bush is a little overkill. Make sure to look through your options. I used the flowerless version of the mesh with browner bark. If you do decide to change anything, make sure to follow the instructions closely and rename the files properly.
* [Trama Bump mapped](http://www.nexusmods.com/morrowind/mods/43015/?) - If you like bump-mapped mods.
* [Hackle-lo Fixed](http://www.nexusmods.com/morrowind/mods/42784/?)
* [Comberry Bush and Ingredient Replacer](http://www.nexusmods.com/morrowind/mods/42586/?) - The EXTRAS option contains another option which includes vanilla style textures. I recommend it.
* [Improved Kwama Eggs and Egg Sacs](http://www.nexusmods.com/morrowind/mods/43555/?) - Technically not a plant, but they work the same way plants do. The install is a little complicated if you're doing it manually. If you want the full package (bump maps + animation) get `00` + `01` + `03`. If you don't want bump maps but do want the animation, get `00` + `02`. For a no frills retexture, just get folder `00`.
* [Fire Fern Plant and Ingredient Retexture](http://www.nexusmods.com/morrowind/mods/43568/?)

* [Better flora](https://mega.nz/#!HwpRRRZQ!IKYOhTxBrfEATUXGltYNsESBZs_Y-CZRQ4zq2bM8duo)  - We're just after the meshes from this mod, but the original had collisions for all the flower meshes. I've fixed that in this version. You do need to disable four files from `meshes\o`), and those are the three kreshweed .nifs and the marshmerrow .nif. If you don't like spinning flowers, you might want to disable the gold kanet meshes as well, as the flowers will rotate when you move your camera. If you want to use them, you'll either need to make them a separate mod, or just pull them into the `meshes` folder with the rest of the mod and re-pack it.

Original mod this was based on can be found [here](http://www.nexusmods.com/morrowind/mods/43288/) (Do not download this)

* [Ascadian Isles Plants](http://www.nexusmods.com/morrowind/mods/36810/?) - If you'd like, install these. I personally don't like the way they look in-game, I think they stick out too much. You might want to skip the comberry bush meshes and textures if you prefer Pherim's (which we already installed). Your choice. If you'd like to use the flowers but want to skip the bush, simply disable the following files before copying into your installation:

```
Meshes\f\flora_comberry_01
Meshes\n\ingred_comberry_01
```

You should disable the entire `Meshes\Gherb` folder.

* [EKM Corkbulb Retexture](http://www.nexusmods.com/morrowind/mods/43809/?)
* [EKM Vanilla-Based Ash Grasses](http://www.nexusmods.com/morrowind/mods/43836/?)

### Solstheim Textures

* Temporarily removed

### Landscape Textures

* [Tyddy's Landscape Textures](http://www.fullrest.ru/files/tyd_landscape-texture_compilation_1/files) - Make sure to download the HQ version along with the UHQ (ultra-high-quality) addon.

**OR** 

* [Vanilla Land](https://www.nexusmods.com/morrowind/mods/45953)

Vanilla land is generally thought of as better looking and more compatible visually with vanilla style textures. However, Tyddy's are strictly higher-resolution in many cases.

There are a total of only 11 textures out of hundreds that are covered by Tyddy but not by Vanilla Land, so using both doesn't serve much purpose at the moment.

### Want plants to not "bend" or "grow" towards you?

I hate this effect. It's in Ozzy's grass, and much more minor in Vurt's grass. Turns out, it's very easy to fix.

In `XE Common.fx` replace

    return saturate(0.02 * h) * (harmonics * displace + stomp);

with

    return saturate(0.02 * h) * (harmonics * displace);

Ta-da! Effect removed!

## Graphic Herbalism Finisher

For those of you using the new Graphic Herbalism - MWSE, you'll need to go back to its mod page [here](https://www.nexusmods.com/morrowind/mods/46599) and download `GH Patches and Replacers`. Install it, and choose the options `00`, `01` (Pherim's) and `12` (Atlas BC Mushrooms Smoothed). If you used the animated Kwama earlier, you should also take `04` or `05`. That should cover everything this guide installs, but if you install those other mods instead of ones in the guide or on top of the guide, you should take those options as well.

If you took Trama Bump-mapped, you'll need option `17` as well. 

## Weather

### Skies

* [Skies .IV Resource Pack](https://www.nexusmods.com/morrowind/mods/43311/?tab=files) - Disable/Hide `ashcloud.nif` and `raindrop.nif`.
* [Alternate Skies](http://www.nexusmods.com/morrowind/mods/42629/?) - Make sure to download the second main file 'Alternate Skies'. The first one is just a single night sky texture, not the whole mod. 
* [New Starfields](https://www.nexusmods.com/morrowind/mods/43246?) - This mod is improperly packaged. Instead of a BAIN installer with options for each version, it requires a bit more leg work. First, download it and check through the provided screenshots, or look at them on the mod page. You'll note (confusingly) that sometimes multiple versions will have only a single screenshot. Once you've decided on one, re-name that file (for example `tx_stars_06.dds`), to `tx_stars.dds`. Then, create a `Textures` folder, place it inside, and delete everything aside from that `Textures` folder. Then, re-pack and install as you would normally. (Sorry for this, I know it's annoying)

### Moons

- If you want a lore friendly moon re-texture take a look at [Lorkhan's Lunar Legacy](https://www.nexusmods.com/morrowind/mods/45718).
- If you want moons that look like they once contained life, try [Dying Worlds](http://www.nexusmods.com/morrowind/mods/43023/?).
- If you want moons that more closely resemble their appearances in the later games, download Skies v3 (Legacy) from the Skies .IV [mod page](https://www.nexusmods.com/morrowind/mods/43311/?tab=files) and install the moon textures from there instead (you only need to copy the content of the Moons folder).

## Architecture Replacers

Hopefully this will be slightly less complicated than the nature section. Something to keep in mind: if a section mentions bump mapping, you CAN safely ignore/skip the bump map mod and use only the textures listed if you want to. Bump mapping doesn't always look great in Morrowind. If, as you're going along, you actually prefer the look of one of the bump-mapped mods instead of my suggestion (meaning Lougian's textures instead of Tyddy's, most of the time), feel free to use the bump map textures instead and skip my recommendation. The ones I picked are closer to vanilla Morrowind, but that doesn't mean it's to everyone's taste.

1. Windows. No longer required, Glow in the Dahrk handles this great now. You can look at getting texture replacements, but look at them beforehand first and ask around a bit.

2. Imperial architecture and shacks.
* [Bump-mapped AOFs Imperial Housing](http://www.nexusmods.com/morrowind/mods/42407/?) - Install options 1 and 3 in the BAIN installer.
* [Bump-mapped Imperial Housing Fixed Filter Mode](https://www.dropbox.com/s/sjsxdkuy46d136k/Bump-mapped_AOFs_Imperial_Housing-fixed_Filter_Mode.7z) - Fixes issues with the meshes from the last step. Again, skip this if you don't want bump maps. Only choose the first option in the BAIN installer. (Ignore WinDoors glow option)
* [Imperial Houses and Forts Retexture](http://www.nexusmods.com/morrowind/mods/43940/?) - This is the actual texture pack we'll be using. HQ is 2k, MQ is 1k. Get the optional Bump Mapped files if you're using those.
* [Dragon Statue Replacer](http://www.nexusmods.com/morrowind/mods/43218/?) - I used Option 3. Also incorrectly archived, you'll need to download it manually and extract it, then you can use MO2 to install one of the .rar files from there.
* [Apel's Lighthouse Retexture](http://www.nexusmods.com/morrowind/mods/42532/?) - Get the version you want, bumps or no bumps.
* [Shacks, Docks and Ships](http://www.nexusmods.com/morrowind/mods/43520/?)
* [Tydz Small Mods](http://www.nexusmods.com/morrowind/mods/44028/?) - Specifically, the Gnisis Fort Roof file. It's a very small change, so feel free to skip it if you want. Also incorrectly packaged. You'll need to extact it, drop the `x` folder into a `Meshes` folder and then re-pack it.

3. Hlaalu.

Choose between the following three options. Compare the screenshots from both modpages and see what looks more visually appealing to you. They are similar enough, so if in doubt just get Aesthesia for it's more 'vanilla' look.

* [Aesthesia - Hlaalu textures](https://www.nexusmods.com/morrowind/mods/46009) - Slightly more vanilla friendly option, includes custom meshes and all textures are uniformed under either 1k (MQ) or 2k (HQ) standard. However the textures appear more blurry then in Arkitektora.
* [Hlaalu - Arkitektora Vol.2](https://www.nexusmods.com/morrowind/mods/46246) - Appears more sharper and goes in a bit of a different direction then Aesthesia. Contains no custom meshes and textures resolutions are mixed. Remember to grab the texture replacer for project atlas in the optional files section. Download the version that's in the same quality as the textures you downloaded.
* [Static's AoF Hlaalu Atlased](https://www.nexusmods.com/morrowind/mods/46022) - An Atlas'd version of AnOldFriend's [Hlaalu Retextured](https://www.nexusmods.com/morrowind/mods/28061) by StaticNation. Signiciantly less vanilla-friendly that the other options, but may be a welcome change of pace to some. 

4. Redoran
* [Redoran Bump mapped](http://www.nexusmods.com/morrowind/mods/42406/?) - A note on these: they use extremely high poly meshes. If you're already struggling to top 30 FPS in exteriors, you should pass on these.
* [Redoran Bump mapped fixes](https://mega.nz/#!qkY2gRJI!VSHQoMctyzL9X2qGYXMC2qqN7kHmu2kzsF--nwBJR2Y) - You only need these if you're using bump maps, obviously.
* [Redoran - Arkitektora Vol.2](https://www.nexusmods.com/morrowind/mods/46235) - An improved version of Redoran - Arkitektora. Completely over-writes all files from the original, so that mod is not needed, only this one. Remember to grab the texture replacer for project atlas in the optional files section. Download the version that's in the same quality as the textures you downloaded.

5. Telvanni
* [Telvanni Mesh Improvement](http://www.nexusmods.com/morrowind/mods/42343/?) - If you're bump mapping, nearly everything here will be overwritten. If you're only using textures, grab this.
* [Telvanni Bump Maps](http://www.nexusmods.com/morrowind/mods/42431/?) - Just get the Interiors WIP, it includes all files from the Exteriors as well.
* [Telvanni Arkitektora](http://www.nexusmods.com/morrowind/mods/43530/?) - Has a few problems, easy to fix.

```
1) disable textures\tx_metal_silver.
2) If you're only using the textures, you'll need to download the Bump Maps file anyway and get the bark_01_nm texture and put it in your `textures` folder.
3) If you're using bump mapping, disable meshes\x\ex_t_manor_01 and meshes\x\ex_t_manor_02, use the ones from Telvanni Bump Maps instead.
```

* [Telvanni Fireplace Replacer](http://www.nexusmods.com/morrowind/mods/43232/?)
(Has an alternate look you can choose instead in the `Alternate` folder=, if you like)

6. Vivec & Velothi

Choose one of the following two:

* [Vivec and Velothi - Arkitektora Vol.2](https://www.nexusmods.com/morrowind/mods/46266) - Remember to grab the texture replacer for project atlas in the optional files section. Download the version that's in the same quality as the textures you downloaded.
* [Vivec-Velothi Retextured V3](https://www.nexusmods.com/morrowind/mods/32886) - A bit lower res in many areas, also not Atlas'd so if you're on a lower end machine you may want the other option. However, some vastly prefer the style here.

Then take all of these:

* [Set in Stone](http://www.nexusmods.com/morrowind/mods/21377/?)
* [One True Faith](http://www.nexusmods.com/morrowind/mods/43810/?)
* [Ministry of truth Bump mapped](http://www.nexusmods.com/morrowind/mods/42921/?) - If you don't want bump maps, the only file you need is `textures\tx_moon_base_01`.
* [Sewers Arkitektora](http://www.nexusmods.com/morrowind/mods/43144/?) - There are pictures showing the difference between the versions in the user uploaded images area.
* [Concept Art Ghostfence Replacer](http://www.nexusmods.com/morrowind/mods/43316/?) - Optional, because it IS a departure from the vanilla game. However, it looks great and it's based on concept art. Your choice.

7. Dwemer & Mournhold
* [Connary's Old Mournhold](http://www.fullrest.ru/files/connarysoldmournhold/files)
* [The Mourning of Bamz-Amschend](http://mw.modhistory.com/download-56-11888) - Only three of these textures are better than what we have: `tx_coilcopper00`, `tx_coilcopper01` and `tx_coilcopper02`. Grab only those three files and disable the rest. This is optional, because the textures in question are just 4x magnified vanilla textures.
* [The Clockwork City](http://mw.modhistory.com/download-56-12886)
* [Clockwork City Reborn](http://www.nexusmods.com/morrowind/mods/38369/?) - These textures are less vanilla friendly than the ones above, but in my opinion look much nicer. Use either this OR the previous mod, not both.
* [Green Marble Mournhold](http://mw.modhistory.com/download-64-11859) - Use the alternate walls but not the alternate roof.
* [Full Dwemer Retexture](http://www.nexusmods.com/morrowind/mods/44264/?) - This also covers armor, weapon and creature textures. Grab the "Only Architecture" archive of your preference for now. MQ is 1024, HQ is 2048.

7. Daedric Ruins
* [Daedric Ruins Retexture](http://www.nexusmods.com/morrowind/mods/39125/?)
* [Daedric ruins bump mapped](http://www.nexusmods.com/morrowind/mods/43318/?) - If you want bump mapping.
* [Daedric Ruins Arkitektora](http://www.nexusmods.com/morrowind/mods/43486/?) - Get the bump map patch if you're using the bump-mapped mod from above.
Feel free to choose between Lougian and Tyddy's packs, if you prefer Lougian's then by all means don't get Tyddy's. Tyddy's is closer to vanilla, as usual.

8. Miscellaneous Architecture Pieces
* [Stronghold Retexture](http://www.nexusmods.com/morrowind/mods/43948/?) - Get the vanilla friendly floor tiles if you want it. However, if you do, it will need to be un-packed, all textures moved into a `textures` folder and then re-packed to install properly with MO2.
* [Connary's 6th House](http://www.fullrest.ru/files/connarys6thhouse/files)
* [Road Marker retextured](http://www.nexusmods.com/morrowind/mods/28311/?) - Incorrectly archived. You'll need to unzip it and move the textures into a `Textures` folder, then re-zip it and install as normal.
* [Banners retextured](http://www.nexusmods.com/morrowind/mods/21405/?) - Some of these will be overridden by Django's Tapestries
* [Arukinn's Better Banner Signs and Signposts](http://www.nexusmods.com/morrowind/mods/41658/?)
* [Signposts Retextured](http://www.nexusmods.com/morrowind/mods/42126/?) Optional, as they are lower res than Arukinn's, but if you want signposts readable in English this is what I would recommend. Download the Tamriel Rebuilt patch if using TR.

```
Q: What about Bloodmoon?
A: Bloodmoon textures were actually covered in nature when we downloaded STOTSP. Remember, STOTSP is a massive overhaul of Solstheim's entire landscape. You do NOT need to activate the .esm if you only wanted to use it as a texture/mesh replacer.
```

## Miscellaneous Replacers

For things that don't really fit in any other section. If some of this seems too tedious to you, feel free to skip it. Some of this is pretty nitpicky...

1. Book mods
* [Arukinn's Better Books and Scrolls](http://www.nexusmods.com/morrowind/mods/43100/?)

Alternative: [Illy's Dirty Books](https://download.fliggerty.com/download-11-715)


* [Melchior's Magnificent Manuscripts](https://www.nexusmods.com/morrowind/mods/45626) - Has an extra folder (`patches`) that offers compatibility with the mod [Book Jackets](http://mw.modhistory.com/download-56-10464). Un-pack the mod, merge the `patches` folder contents in, and re-pack if you'd like that.

2. [Papill6n's various graphic things.](http://www.nexusmods.com/morrowind/mods/39122/?) Grab the following in the BAIN installer:

```
Awning woven
Bellow and canvaswrap
Bridge rope brown
Fabric on the imperial altar - more vanilla
Kneeling stool - Get the texture only, we have a better mesh
Logo crate
Loom
Ropes - only tx_rope_heavy_01
Ropes woven + hammock's pillow
Rusted metal
Siltstrider - We'll be installing Vurt's silt strider soon.
Soulgems - Take a look at the included screenshot, you'll want to know what they look like for later.
Spinningwheel + spool
Tribunal required
```

Note that "tribunal required" actually has 3 sub-packages. You'll need to open the mods in your `MODS` folder in MO2, then take the contents of each of those 3 folders and drag them into the main mod. It should be obvious which 3. You can delete the .jpg files, don't need them anymore.

3. Qarl's mods. The following mods were made by Qarl but uploaded by someone else on fullrest.
* [Plates](http://www.fullrest.ru/files/Plate_Items/files)
* [Bowls](http://www.fullrest.ru/files/Bowl_Items/files)

4. Other, less complicated to install mods
* [Connary's Fine Vials](http://www.fullrest.ru/files/connarysfinevials/files) - Optionally, disable the "icons" folder if you prefer the ones from Ultimate Icon Replacer instead. Also: disable `tx_rustedmetal00.dds` and `tx_rustedmetal10.dds`, Morrowind Visual Pack has better versions of these.
* [Connary's Mixed Pottery](http://www.fullrest.ru/files/connarysmixedpottery/files) - disable the mottled texture and pewter 1 texture.
* [AOF Containers](http://www.nexusmods.com/morrowind/mods/32427/?) - disable `meshes\m\misc_com_bucket_01`.
* [Small Mods by Wolli](http://www.nexusmods.com/morrowind/mods/42453/?) - Just get Darker Crates to match AOF's barrels.
* [Better Kegstands](http://www.nexusmods.com/morrowind/mods/37708/?)
* [Apel's Various Things - Sacks](http://www.nexusmods.com/morrowind/mods/42558/?) - Bump mapped or not, it's your choice. Has an optional patch on the Nexus page for Animated Containers, if you use it.
* [Dahrk Mods by Melchior](http://www.nexusmods.com/morrowind/mods/43528/?) - Get Detailed Brooms.
* [Dunmer Lanterns Replacer](http://www.nexusmods.com/morrowind/mods/43219/?) - Make sure to look at the images and choose the textures you want.
* [EKM Vanilla-Based Paper Lanterns](http://www.nexusmods.com/morrowind/mods/43837/?)
* [AST beds texture replacer](http://www.nexusmods.com/morrowind/mods/21970/?) - We only want the chair mesh, the rest will be overwritten with the next mod.
* [Illy's Bedspreads](http://www.nexusmods.com/morrowind/mods/43565/?) [Wayback link](https://web.archive.org/web/*/http://download.fliggerty.com/file.php?id=1108)
* [Illy's Hot Pots](https://download.fliggerty.com/download--1054)
* [AST redware texture replacer](http://www.nexusmods.com/morrowind/mods/21981/?)

One of the following:

* [Improved Better Skulls](https://www.nexusmods.com/morrowind/mods/46012) - In the BAIN installer, select "Data files" and "Fixed Skeletons". If you want, download the optional file "Skeletons Atlased" for atlased skeleton textures. If you do so, make sure to choose option 01 "Improved Better Skull Textures (Connary)". 
* [Bone Items](http://tesall.ru/files/file/1633-bone-items/) 

Moving on:

* [Dunmeri Urns Aestetika](http://www.nexusmods.com/morrowind/mods/43541/?) - Get either the simple retexture or the bump map file, you don't need both.

**NOTE**: If you are using the non-bump-mapped version, it's missing `tx_urn_01_nm.dds`. You have a couple options to remedy this:

1: Use the bump-mapped version instead

2: Download both, and copy the missing file from the bump-mapped version over to the non-bump-mapped version

3: Download just the non-bump-mapped version, and copy `tx_urn_01.dds`, and re-name it to `tx_urn_01_nm.dds`

* [Cart Cloth Retexture CCR](http://www.nexusmods.com/morrowind/mods/21837/?) - I prefer the normal version.
* [Propylon Pillar Retexture PPR](http://www.nexusmods.com/morrowind/mods/19600/?) - Get either PPR_Glow or PPR_Normal, then get the PPR_Index Addon.
* [Soulgem Ingredient Retexture SIR](http://www.nexusmods.com/morrowind/mods/19467/?) - If you have both expansions (you should!) then pick SIR_TBandBM_v3 to download. Disable the Stahlrim texture or load this mod just prior to Tyd Landscape Texture Compilation, so that its Stahlrim texture takes precedence.
* [Ingredients Mesh Replacer](http://www.nexusmods.com/morrowind/mods/44067/?) - You'll need to extract the archive, copy the compatibility mesh folder over and over-write the files from the main mod, then re-pack and install as normal.
* [Crabmeat Ingredient Replacer](http://www.nexusmods.com/morrowind/mods/43387/?)
* [Django's Rugs and Tapestries](http://www.nexusmods.com/morrowind/mods/36872/?)
* [Detailed Tapestries](http://www.nexusmods.com/morrowind/mods/22551/?)
* [Shiny Septims](http://www.nexusmods.com/morrowind/mods/42113/?) - I get the dulled version.
* [Pherim's Silverware Repolished](https://www.nexusmods.com/morrowind/mods/46385) - Take 00 Data Files and the 2K Atlas option.
* [Better Blood Morrowind](http://www.nexusmods.com/morrowind/mods/33426/?)
* [Flash's Minor Retextures](http://www.nexusmods.com/morrowind/mods/44322/?) - Contains 2 files. 1 is an alternate Blood texture if you dislike BBM's. It also has a Mist retexture, which you should definitely get.
* [Skeleton and Metal Sparks blood retexture](http://www.nexusmods.com/morrowind/mods/43359/?)
* [Improved Cavern Clutter](https://www.dropbox.com/sh/l1660o8fg664bii/AABLfGQtcBsb0jfTsftnBZ-ca/Improved%20Cavern%20Clutter?dl=0) - Download as zip. You'll want to disable the three wood_weathered and rope_heavy textures after installing.
* [Insanity's Potion Replacer](http://tesalliance.org/forums/index.php?/files/file/1402-insanitys-potion-replacer/) - You'll need an account to download these.
* [Insanity's Soul Gem Replacer](http://tesalliance.org/forums/index.php?/files/file/1397-insanitys-soul-gem-replacer/) - Again, you'll need an account. If you like the look of these soul gems better than Papill6n's, go ahead and get them, overwriting your existing meshes. If you like the ones you already have, you might want to download it anyway, as Papill6n's didn't include a retexture of grand soul gems. If you just want the grand soul gems from this mod, get only the following files: `meshes\m\misc_soulgem_grand` and `textures\tx_soulgem_grand`.
* [Insanity's lowres](https://mega.nz/#!T4pB3TCY!wQ3okENYSVv8T2PpHW5jxPiPkbOGrlXBP7ODVglGsDA) - Insanity's replacers are really high resolution for such small objects, especially in an old game like Morrowind. If you'd like, you can get these resized textures instead. You'll still need the original mods for the meshes! Also, if you're only using the grand soul gem, make sure to disable the other textures in the `soulgems` folder, as you don't need them.
* [Long Live The Glassware](http://www.nexusmods.com/morrowind/mods/44016/?) - disable `tx_metal_strip_02`.
* [Long Live The Limeware](http://www.nexusmods.com/morrowind/mods/44045/?)
* [R-Zero's Random Retextures](http://www.nexusmods.com/morrowind/mods/44025/?) - Get the following: "Chimney Smoke", "Iron Towershield" and "Quill".

## Creature Replacers

1. Let's start off with our base. We're starting off with Darknut's suite of textures.
* [Darknut's Creature Textures](http://www.nexusmods.com/morrowind/mods/43420/?)
* [Darknut's Creature Textures addendum](http://www.nexusmods.com/morrowind/mods/43441/?)
* [Darknut's Creature Textures TB](http://www.nexusmods.com/morrowind/mods/43421/?)
* [Darknut's Creature Textures BM](http://www.nexusmods.com/morrowind/mods/43422/?)

2. Connary made some good creature retextures.
* [Storm Atronach](http://www.fullrest.ru/files/connarysstormatronach/files)
* [Skeleton](http://www.fullrest.ru/files/connarysskeleton/files)
* [Lich](http://www.fullrest.ru/files/connaryslichking/files)
* [Kwama](http://www.fullrest.ru/files/connaryskwama/files)
* [Imperfect](http://www.fullrest.ru/files/connarysimperfect/files)
* [Bonewalker](http://www.fullrest.ru/files/connarysbonewalker/files)
* [Daedroth](http://www.fullrest.ru/files/connarysbaddaedroth/files)

3. And now for other replacers
* [Correct UV Mudcrabs](http://www.nexusmods.com/morrowind/mods/42130/?) - Not strictly a retexture, but does improve visuals. I chose the "regular" option rather than smoothed. No screenshots exist to compare the two, but you can test this easily yourself by installing it twice (once for each option) and test enabling/disabling them in-game to see what looks better. [TODO]
* [Guars Aendemika](http://www.nexusmods.com/morrowind/mods/42521/?)
* [Kagouti Aendemika](http://www.nexusmods.com/morrowind/mods/42523/?)
* [Alit Aendemika](http://www.nexusmods.com/morrowind/mods/42520/?)
* [Ash Vampire Reworked](http://www.nexusmods.com/morrowind/mods/43633/?)
* [Cliffracer Replacer](http://www.nexusmods.com/morrowind/mods/43925/?)
* [Nix-Hound Replacer](http://www.nexusmods.com/morrowind/mods/43620/?)
* [Scamp Replacer](http://www.nexusmods.com/morrowind/mods/44314/?) - You (probably) don't need the PBR files, it's still a bleeding edge new feature in MGE XE. Get the Creeper replacer if you want. If you do, make sure to mark the german version of the ESP as "optional" instead of "available" in MO2, since it'll be automatically activated.
* [Luminous Atronachs](http://www.nexusmods.com/morrowind/mods/42613/?)
* [Vurt's Silt Strider Retexture](http://www.nexusmods.com/morrowind/mods/30696/?) - Don't use skin_01 and skin_03, we have fixed versions of those.
* [Netch Bump mapped](http://www.nexusmods.com/morrowind/mods/42851/?) - Get the main file and the optional file.
* [Unique Winged Twilights](http://download.fliggerty.com/download--743) - The .esp is unnecessary if you just want a replacer.
* [BB Dwarven Spectre](http://www.nexusmods.com/morrowind/mods/29671/?)
* [Better Almalexia](http://www.nexusmods.com/morrowind/mods/23388/?) - Comes with alternate pupil textures if you want. (You'll need to unpack/repack to add them). Also comes with a splash screen (`Splash_almalexia.tga`) you may want to disable if you feel it clashes with the existing splash screen replacers.
* [Azura Replacer](http://mw.modhistory.com/download-45-6053)
* [Vivec God Replacement Creature Edition](http://mw.modhistory.com/download-26-10946) - Feel free to look through the `extras` folder at your options.
* [Voiced Vivec and Yakety Yagrum](http://www.nexusmods.com/morrowind/mods/40994/?) - Not really a replacer, but it does involve 'creatures'.

We'll get a replacer for Dagoth Ur and dremora in the next step.

>Q: What about *insert other creature replacer here*?
>
>A: Dwemer will be installed in the next section. Otherwise, I don't know about it, or it didn't suit my taste. Here's a small list of mods I know about that didn't make the cut:

* Connary's other replacers - fullrest.ru
* Silt Strider Bump Mapped by Lougian - Nexus
* Psy's Golden Saint Replacer - MMH
* Divine Dagoth Ur - Nexus
* Spriggan Bump Mapped by Lougian - Nexus
* Kwama Forager Bump Mapped by Lougian - Nexus, specifically in his Various Little Mods
* Tyddy's Cliff Racer Aendemika - Nexus

## Heads & Bodies

1. Heads

  *Note that if you're using any of the head replacers linked here in conjunction with Tamriel Rebuilt the heads provided by TR will not be fully replaced because the mod assigns unique IDs to their heads.*
* [Westly's Pluginless Head and Hair Replacer](http://download.fliggerty.com/download-127-874)
* [Various tweaks and fixes](http://www.nexusmods.com/morrowind/mods/43795/?) - Specifically, Fixed Westly's Female Orc Heads and Fixed Westly's Barenziah Head.
* [Animation Fix for Westly's Heads](https://www.dropbox.com/s/d70l2lbjvm0xloo/WestlyHeadsAnimFix.zip?dl=0) - Does what it says on the tin
* [Pluginless Khajiit Head Pack](http://www.nexusmods.com/morrowind/mods/43110/?)
* [Pluginless Khajiit Head Pack Talk-Blink Fix](http://abitoftaste.altervista.org/morrowind/index.php?option=downloads&task=info&id=68&Itemid=50&-Pluginless-Khajiit-Head-Pack-Talk-Blink-Fix)

Argonians will be in the next step, don't worry.

2. Body replacers
* [Robert's bodies](http://www.nexusmods.com/morrowind/mods/43138/?) - Get the main file. Optionally, get Dagoth Ur OR Dagoth Ur (vanilla shaders), and RB Altmer Females, RB Bosmer Females, RB Orcish females. For the last three, you should look at the images section to see what they do; Westly's version is on the top, RB version is in the middle, and vanilla is at the bottom. The Orcish heads in particular are a drastic departure from Westly's heads, but they look more like the vanilla heads.

Robert's bodies is heavily incompatible with other mods, including later mods in this guide. I mention some workarounds, just keep that in mind. 

* OR [Install Better Bodies](https://www.nexusmods.com/morrowind/mods/3880)

Note that at the time this guide is being written, Khajiit meshes are nude. If seeing girl Khajiit nipples bother you, you should consider activating New Beast Bodies Khajit - Clean below, and make sure it overrides Robert's bodies. Also, it seems the nude meshes have been removed.

* [Unique Shadow Pack](http://mw.modhistory.com/download-10-6029) - This is a requirement for...
* [New Beast Bodies - Clean Version](http://mw.modhistory.com/download-10-10928) - You only need the argonian .esp and files. If you want to disable the khajiit meshes and textures, you can, but as long as you don't activate the Khajit bodies .esp, you'll be fine leaving them alone.
* [Want 'mature' Argonians?](http://mw.modhistory.com/download-10-11364)
* [Wey's Argonians](http://www.nexusmods.com/morrowind/mods/43766/?) - Get the optional darker mouths file if you wish. I use it.

An newer alternative to Wey's Argonians for those who feel it may stray too far from the vanilla style:

* [Improved Argonians](https://www.nexusmods.com/morrowind/mods/45918)

## Clothing Replacers

1. Clothes
* [Better Clothes](http://www.nexusmods.com/morrowind/mods/42262/?) - Get the non-installer version. Only activate ONE esp. If you want your Argonian females to have breasts lumps when clothed for some reason, choose the regular version. For flat Argonian females, activate the '\_nac' version.

Note: When opening Mlox, it will warn you that Better Clothes depends upon Better Bodies. This is not unwarranted, there will be clipping. You can ignore this if you like, or install Better Bodies instead of Roberts bodies. Alternatively: 

> 1) Get the [Robert's Bodies version of Better Clothes on Wolflore](http://wolflore.net/viewtopic.php?f=15&t=2086&sid=53e89d737b9bbe081c9946c8c0d11b37) (Requires an account, also that link may not be right)
> 2) Forgo Better Clothes and use something like Articus' clothes which are compatible with both Robert's and Better Bodies

* [Common Shirt Fix](https://www.dropbox.com/s/3kwi2ha2anpu7kw/BCFix.zip)
* [BC Shoes Fix](https://www.dropbox.com/s/usgjr6hwi53c6ma/BC%20Shoes%20Fix.zip)
* [Expensive Female Shirt Fix](http://mw.modhistory.com/download--14998) - Put this in your `meshes\BC` folder.
* [More Better Clothes](http://mw.modhistory.com/download-53-6647) - Get both the main file at the bottom of the page and the `MBC_ArmsFix`.
For the Arms fix, make sure to un-pack it and create a `Meshes/BC` folder, then drop those .nif files into it and re-pack it to install.
* [Better Clothes for Tribunal](http://mw.modhistory.com/download-87-11804)
* [Better Clothes Bloodmoon Plus](http://download.fliggerty.com/download-21-804) ([Wayback Link](https://web.archive.org/web/20161103154305/http://download.fliggerty.com/file.php?id=804))
* [BCBM Pants Fix](https://www.dropbox.com/s/lkxditr9gl3a92c/BCBM_Pants_Fix.zip)
* [Darknut's Better Clothes Textures](http://www.nexusmods.com/morrowind/mods/43423/?)

2. Accessories.
Note that some of this stuff (belts, rings, amulets) won't actually appear on your character model. It's mostly so your unique, fancy stuff will look cool when you painstakingly put it on shelves in your stronghold later.

* [Drakkmore's Plugginless Ring Replacer](http://download.fliggerty.com/download-136-1035) - Actually gives rings textures. Without this they'll all appear black in-game.
Alternative: [Unique Jewelry Redone](https://www.nexusmods.com/morrowind/mods/46151)

* [Unique Finery Replacer UFR](http://www.nexusmods.com/morrowind/mods/25725/?) - Activate the regular version. The robe mod we'll be using comes with a compatibility patch.

3. Robes
* [Better Robes](http://www.nexusmods.com/morrowind/mods/42773/?) - Make sure to also install the patches for Tamriel Rebuilt if you're using it (`TR` folder) and UFR. If you plan to use Animated Morrowind, download the separate patch for that as well.

If using the Tamriel Rebuilt patch, you'll need [this patch](https://www.nexusmods.com/morrowind/mods/44875) for that patch, since it crashes due to a Master reformat in 2015 that TR did. (However, note that this doesn't fix the issue with the TR-BR-Animated Morrowind combined patch, so you're kind of out of luck if using that)

* [Robe Overhaul](http://www.nexusmods.com/morrowind/mods/43748/?)
* [Various tweaks and fixes](http://www.nexusmods.com/morrowind/mods/43795/?) - Optionally, if you hate the glow effect that Robe Overhaul adds to some robes, you can download Blank Glow Maps for Robe Overhaul. You might also be interested in Pluginless NoGlow Lite, which removes the plastic-y looking 'enchantment' effect from all items in game.

## Weapons

There are likely a ton of unique/artifact weapon replacers I've missed. I was never very good at keeping track of weapon mods...
* [Darknut's Little Weapons Mod Complete](http://www.nexusmods.com/morrowind/mods/43418/?) - Has a `Textures/512` and a `Textures/1024` folder. You should be able to handle the 1K textures. In either case, you'll need to un-pack the mod and move all of whichever you choose (in my case 1K) out of the `1024` folder, and into the root `Textures` folder, and then re-pack.
* [Oriental Mesh Improvements](http://www.nexusmods.com/morrowind/mods/29906/?)
* [Crossbows](http://download.fliggerty.com/download-98-1010) - If you don't want the new crossbows, don't activate the .esps. You'll still get new meshes for the base game's crossbows. For TR users, note that this ESP is also set up requiring the old TR's ESP as a master, so it'll crash if you try to use it on modern TR installs.
* [Real Reflective Weapons - Iron](http://www.nexusmods.com/morrowind/mods/43077/?) - Install the base (`Data Files`) folder and the `bonus` folder.
* [Improved Weapon Meshes - Steel](http://www.nexusmods.com/morrowind/mods/43120/?) - Install `00` and `01`. You do not need the .esps.
* [Improved Weapon Mehses - Ebony](http://www.nexusmods.com/morrowind/mods/43484/?) - Install `00`. Install `01` if you want an Ebony Claymore in your game, you'll need the .esp. If you do so, note that it'll install two ESPs, one being German. Make sure to move it to the "Optional" section after installing.
* [Dwemer Armoury](http://www.nexusmods.com/morrowind/mods/43335/?) - Unfortunately, this isn't totally compatible with our armor mods, but the weapon meshes and a few of the armor meshes will show up in game.
* [Mehrunes Razor Replacer - Oblivion](http://www.nexusmods.com/morrowind/mods/23825/?)
* [True Trueflame](http://www.nexusmods.com/morrowind/mods/33432/?)
* [HopesFire Replacer Morrowind Edition](http://mw.modhistory.com/download-98-12378) - Has an `AltTextures` folder with an alternate texture for Hopesfire. You'll need to move the folder's contents into the `Textures` folder and over-write after installing if you wish to use it. (Or un-pack/repack)
* [Various little mods](http://www.nexusmods.com/morrowind/mods/43330/?) - Volendrung.
* [Pherim's Improved Weapon Meshes & Textures WIP](https://www.dropbox.com/sh/l1660o8fg664bii/AAAO3m96a4O4J4JOUOUBmFnFa/Improved%20Weapon%20Meshes%20%26%20Textures%20WIP?dl=0) - Download as .zip.
* [Spear-Staff Fix](http://www.nexusmods.com/morrowind/mods/43353/?) - An optional fix for the position where spears and staves are held. Use it if you want. If you do, you'll need the Real Reflective Weapons Iron, Improved Weapon Meshes Steel, and Improved Weapon Meshes Ebony files from the `Compatibility` folder, then drag them out and over-write their normal versions from the mod, and then re-pack and install as normal.

## Armor

* [Darknut's Armor Textures](http://www.nexusmods.com/morrowind/mods/43416/?) - Make sure to get the newest version.
* [Various little mods](http://www.nexusmods.com/morrowind/mods/43330/?) - Install Colovian helm and Dust adept helm.
* [Improved Armor Parts](https://www.dropbox.com/sh/l1660o8fg664bii/AAB-OssUyNu03Y5aGCO1Gav0a/Improved%20Armor%20parts?dl=0) - Download as .zip. First, disable the `Bloodmoon` folder; you already have that mesh. If you want a less bulky chitin pauldron, put that in `meshes\a`. Then go ahead and install the `meshes` and `texture` folder.
* [Various tweaks and fixes](http://www.nexusmods.com/morrowind/mods/43795/?) - Get Lougian's Colovian Helm fix.
* [HiRez Armors - Native Styles](http://forums.bethsoft.com/topic/1441431-relz-hirez-armors-native-styles-v2)
* Native HiRez fix [1](http://forums.bethsoft.com/topic/1441431-relz-hirez-armors-native-styles-v2/page-2#entry22297270), [2](http://forums.bethsoft.com/topic/1441431-relz-hirez-armors-native-styles-v2/page-2#entry23936622), [3](http://www.mediafire.com/file/sj9kg66x5cdq45l/tx_armor_EXC.dds/file) (Fixes missing `tx_armor_exc.dds`, just put it into the `textures` folder of whichever of these fixes mods has a `textures` folder)

* [Armor Retexture - Outlander Styles](http://www.nexusmods.com/morrowind/mods/44210/?) - Get the HQ version. You don't need to get the dragonscale armor textures. You should disable `tx_a_templar_helmet` before installing; we have better from Improved Armor Parts.
* [Full Dwemer Retexture](http://www.nexusmods.com/morrowind/mods/44264/?) - We already installed the architecture, now we need the 'Only armor, robots, and weapons' archive. Pick MQ (1024) or HQ (2048), your choice.

* [Better Morrowind Armor](http://www.nexusmods.com/morrowind/mods/42509/?) - This needs more detailed install instructions:

1) First, extract the archive. You need to activate the Better Morrowind Armor .esp, and optionally one DeFemm patch of your choice. A removes all female versions of cuirasses (no boob armor for females), O acts like the original game, R gives boob armor only to stretchy armor. 

2) You should use the DeFemm patches from [here](https://mega.nz/#!WgBQ2RRL!5CQU0ZIVvIv1vyUsutAr3gT-qMhRUU6E4KEvoE9AeOs). Just make sure to put it directly after the main mod, and only enable the ESPs you were using from the original mod. (In my case, I use `Better Morrowind Armor.esp` and `Better Morrowind Armor DeFemm(o).ESP`)

3) Install the patch for Hirez Armors - Native Styles V2. (Overwriting the main files in the mod folder)

4) If you're using the LeFemm official plugin for Bethesda, install the patch for that as well. That means DEACTIVATING the `[Official]LeFemm Armor.esp` included with WHReaper's Morrowind Official Plugins and using the `LeFemmArmor.esp` included with Better Morrowind Armor.

* [Daedric Lord Armor Morrowind Edition](https://www.nexusmods.com/morrowind/mods/44081) - Not only does this replace Daedric armor and gives bound armor a unique look, it acts as a replacer for Dremora as well. It's newer than Better Morrowind Armor and should load after it, so you'll get this nicer looking Daedric Armor in game.

* [Daedric Lord Armor Face of God](https://www.nexusmods.com/morrowind/mods/45037/) - A replacer for the Face of God, since the previous mod didn't cover it. 

* [Less Bulky Pauldrons](http://www.nexusmods.com/morrowind/mods/42566/?) - Optionally, you might like this. If you do decide to use it, make sure to use the the BAM & Native HiRez 2 files in the optional folder. To use them, create the folder `Data Files\Meshes\bam` inside the un-packed mod. Then, move the files from the `BAM & Native HiRez 2` into that `bam` folder, not the `a` folder like the rest of the mod's contents.

## Animations

* [Animation Compilation](http://www.nexusmods.com/morrowind/mods/43982/?) - Download the "Fixes by Greatness7" version.

# Conclusion And Wrapping Up

## Testing Your Setup

Aside from simply making sure the game opens and loads, there are several tools in place that will help you quickly get into game and search for anything that might have gone wrong.

The one we recommend is [Skip Tutorial](https://www.nexusmods.com/morrowind/mods/27266) being a relatively new and clean alternative to older mods like QuickChar and SilentCharGen. It lets you skip the early tutorial section and go right into making a character.

You can then also COC to various locations to do some walking around, such as:

`Clutter Warehouse - Everything Must Go!`
`ToddTest`
`Character Stuff Wonderland`
`Ken's Test Hole`
`Mark's Vampire Test Cell`
`Redoran Interior`
`Redoran Interior2`

Do you get any errors while loading? Any errors while moving around? Anything missing a texture, or look out-of-place? It's likely we missed something in the guide. Make sure to let us know via a Github issue!

## MGE XE Setup

If you have a toaster, you might want to skip most of this section. Run distant land as explained towards the end with default settings and see how the game runs for you first before trying out grass or any of the fancier light settings in the distant land tab. You might also try out shaders.

1. Before we begin, we need to download mod(s) related to grass. 
* [Aesthesia Groundcover - grass mod](https://www.nexusmods.com/morrowind/mods/46377/) - An excellent looking and performing grass mod to replace "Azura's Coast and Sheogorath - Grassmod" and "Morrowind grass mod combined v1.0"

Alternatively, you could use...
* [Vurt's Groundcover](http://www.nexusmods.com/morrowind/mods/31051/?) - If you want Ashlands grass, you'll need to download this as none was included in the previous download. Use EITHER the previous mod OR this one for the other regions, do NOT use both. Use Reeds and the optional Corals download if you want, they should work with Grass Mod Combined just fine.

For those of your with Tamriel Rebuilt, [Tamriel Rebuilt - Old Ebonheart Groundcover](https://www.nexusmods.com/morrowind/mods/45973) will enable Vurt's groundcovers to extend to Tamriel Rebuilt.

2. Some other MGE XE relevant mods.
* [Distant Mournhold](http://www.nexusmods.com/morrowind/mods/43255/?) - DO activate this .esp in your launcher.
* [PeterBitt's Small Mods](http://www.nexusmods.com/morrowind/mods/42306/?) - If you have a good computer and plan to use Per Pixel Lighting, get the Negative Lights Remover. Activate in your launcher.

3. Distant Land

First, make sure all the mods you're using are activated in the launcher (again, don't activate the grass mods in the launcher). Then, run MGEXEgui.

>1) Go into your Distant Land tab, and click on Distant land generator.
>
>2) Click 'Use current load order', then go through the list and activate Grass_AC&S, Vurt's Groundcover - The Ashlands (if you're using it), and either Ozzy's Grass packages (there are five total) or Vurt's Groundcover - BC, AI, WG, GL and Vurt's Groundcover - Solstheim. Also, activate the reeds module and the corals module if you're using those. Click continue.
>
>3) On the next few screens, change the settings only if you think it's necessary. If you're running a toaster you might want to turn your settings down. Be very conservative if you try to turn the settings up higher, as it CAN make your game run very slow. That said, re-running the distant land generator isn't too difficult. On the statics screen, make sure to read the tooltips for your options and set them accordingly.
>
>4) When your distant land generation is finally complete, you'll have a lot more options in MGE XE to play with. Most of these are self-explanatory. If you have a toaster, you probably shouldn't mess with the default settings much; instead, launch the game and see how it runs for you with the basic settings, and with shaders, before messing with anything here. If you have a beastly machine, try out Per-pixel lighting (make sure to use Negative Lights Remover.esp in this case), high quality exponential fog, and high quality atmosphere and distance coloring. And, of course, turn up your draw distance. I play with 10 visible cells.
>
>You will by default recieve a warning about 2 missing files - 'tx_ma_sandstone02.tga' and 'tx_lavacrust00.tga'. This is completely normal and is a fault with the vanilla Morrowind BSA - nothing you did. However, if these messages bother you and you want to be sure from a glance whether you have real issues when generating distant land [this mod](https://www.nexusmods.com/morrowind/mods/45588) provides dummies of those two files so the distant land generator doesn't complain.

4. Shaders

Click the shader setup screen on the General tab. If you're using the latest MGE XE beta, the shaders screen will be pretty easy for you. Pick your quality preset, adjust it how you want (turning on/off Depth of Field, using lower quality SSAO, etc.), and play. 

Optionally, you might want to take a look at [this water shader](https://www.nexusmods.com/morrowind/mods/45432).

5. Finally, and only when you're satisfied with your distant land generation, install [Lore-Friendly Ghostfence Texture](http://www.nexusmods.com/morrowind/mods/29206/?). Why is this step last? Because if you generate distant land with these textures in your folder, it makes the ghostfence look like it has holes in it. Stick with the vanilla textures for distant land generation. If you re-run your distant land generation later, try to remove the textures `tx_gg_fence_01` and `tx_gg_fence_02` from your `textures` folder first.

## Cleaning Mods

**Note:** Make a backup of ```Mod Organizer 2/Profiles/Your Profile Name Here (Likely 'Default')/Morrowind.ini```, as there is a bug that may occur during this step.

**NOTE:** DO NOT CLEAN MULTIPLE OF THESE MODS AT ONCE! It has been known to cause odd, errant behavior. Do not do it! Clean one at a time.

Several of the plugins in this list need to be cleaned. Here is the list of plugins that need to be cleaned, and do not have any warning about cleaning in their readme:

```
wl_SolstheimOverhaul_v1.esm
correctUV Ore Replacer 1.0.esp
What Thieves Guild.ESP
LGNPC_TelMora_v1_30.esp
LGNPC_Khuul_v2_21.esp
Less_Generic_Bloodmoon.esp
Less_Generic_Nerevarine.esp
LGNPC_SecretMasters_v1_30.esp
LGNPC_IndarysManor_v1_51.esp
LGNPC_PaxRedoran_v1_20.esp
Bloated Caves.esp
Apel's_Asura_Coast_Fix.esp
Vurt's BC Tree Replacer II.ESP
VoicedVivec.ESP
YaketyYagrum.ESP
Better Clothes_v1.1_nac.esp
UFR_v3dot2.esp
Better Morrowind Armor.esp
Illy's Hot Pots.ESP
Vurt's Grazeland Trees [Palms].esp
```

To actually clean, first open Wrye using MO2. Then, right click on a given plugin and hit "Clean with TES3CMD"

**POTENTIAL GAME-BREAKING BUG:** Wyre is ocassionally writing its log during this process into Morrowind.ini instead. **This breaks the game**. To fix it, you must find a backup of Morrowind.ini and use it to replace the (now broken) one in ``` Mod Organizer 2/Profiles/Your Profile Name Here (Likely 'Default')/Morrowind.ini```. That's why we made the backup earlier, just in case. 

## Creating A Multipatch

This is very easy. Open Wrye. At the top bar, go to "Misc" then "TES3CMD" then "Create Multipatch". It shouldn't take too long.

It will automatically be appended to the end of your load order. You're now good to go!

(Note: You must re-do this upon adding, removing or re-ordering mods)

# Aftercare

## Updating Masters, Syncing and Repairing your Saves

This should be done periodically with saves. You *must* do this anytime you add, remove or move a mod while in the middle of a playthrough.

The steps are as follows:

1. Open Wrye Mash (Polemo's Fork)
2. Go to the "Saves" Tab
3. Right click anywhere in the plugins list under "Masters" on the right side. A popup should appear asking you if you wish to edit the list. This will automatically perform an update of the masters.
4. Right click on the "Masters" column header, choose "Sync to Mod List"
5. Hit "Save" towards the bottom
6. Right click the save file, and hit "Repair All"

Perform this for each save you have.

All of your saves should appear Purple in the list now. For each save, all of its masters should appear in blue.

## Load Order

We currently do not have a reccommended load order for Morrowind 2019. Recommendations are welcome for this section!

# Misc Other Info

## Other Mods

Not satisfied with just a graphics overhaul? Here are some other mods you might want to try. Please, PLEASE read the mod pages for the following mods. Simply downloading and installing everything here could very well make your game laggy and/or unstable, especially if you don't use a proper load order. I do not play with all of the below mods myself anymore, but have played most of them in the past. Some I've never played at all, but they do come highly recommended and endorsed by the community.

0) I (Thastus) personally very much enjoy [Races Are More Fun](https://www.nexusmods.com/morrowind/mods/21875) and [Birthsigns are More Fun](https://www.nexusmods.com/morrowind/mods/17888)

If you enjoy H2H characters, the MGE XE version of the Opponent Fatigue Indicator can be found [here](https://www.nexusmods.com/morrowind/mods/44363)
(However, it does not scale with MGE XE gui size options. Considering re-making it myself using MWSE-LUA to do so very cleanly)

As well, I find [MCC leveler](https://www.nexusmods.com/morrowind/mods/44294) (inspired by GCC and MADD) to be the best leveling system for my personal tastes (Others certainly exist though).

(Includes optional state-based HP, optional state-based magicka regen, as well as just a better overall leveling system inspired by MADD and GCD, but far better than either. No micro-management required! No min-maxing needed!)

Finally, [IMMERSIVE RUN FIX](https://www.nexusmods.com/morrowind/mods/45947) makes running diagonally not faster. 

1) Want your sound overhauled as well as your graphics? You can try [Atmospheric Sound Effects](http://mw.modhistory.com/download-51-7148).

2) Are you used to newer Bethesda games where you swing your weapon and hit the enemy without miss chance? Is Morrowind absolutely ruined for you if your attacks miss when it clearly looks like they should hit? [Try this](http://forums.bethsoft.com/topic/1513002-rel-oblivion-like-combat-tweaks-part-of-men-project/).
*Disclaimer: I haven't tried this. But reading through the forum thread, it seems like a solid mod.*

3) Want to be a wizard? Here are some mods you might like.
* [Mastering Magicka](http://www.nexusmods.com/morrowind/mods/42269/?) - This mod is a complete overhaul of the magic system. You should read the mod page to learn more. If you think this mod does a little too much and want to pick and choose for yourself, keep reading.
* [Fair Magicka Regen](http://www.nexusmods.com/morrowind/mods/39350/?)
* [Raym's Simple Mana Regeneration](http://www.wolflore.net/viewtopic.php?f=108&t=1553.) - Use either this OR Fair Magicka Regen, not both. The difference between them is that Fair Magicka Regen is percent based, while Raym's is simpler and lighter on CPU/scripting. Don't use this OR Fair Magicka Regen if you're using Mastering Magicka.
* [Spell Cast Reduction](http://mw.modhistory.com/download-37-1406) - Another feature already included in Mastering Magicka.
* [Melian's Teleport Mod](http://mw.modhistory.com/download-21-6360) - Not only for wizards, this mod makes travelling around Vvardenfell a breeze by allowing you to have unlimited Mark locations.

4) Do you want to travel with a companion (or two)? Then here is, hands down, the best Morrowind companion mod: [Julan, Ashlander Companion](http://lovkullen.net/Emma/Kateri.htm) You might also be interested in [this](http://www.nexusmods.com/morrowind/mods/42780/?) to give Julan plus some other characters the fully red Dunmer eyes. There are some other companion mods for Morrowind, but none with the sheer amount of dialogue (or a quest directly tied to the main plot) as Julan.

5) Want harder dungeons?
* [Darknut's Greater Dwemer Ruins versions 1.1](http://www.nexusmods.com/morrowind/mods/43544/?) - A widely used and recommended overhaul of the Red Mountain citadels. It was mentioned in Knots' guide. It's incompatible with most anything that changes any of the final dunmer strongholds. Unfortunately, most of the compatibility patches for it only work with 1.0, which can be found [here](http://mw.modhistory.com/download-98-11646).
* [Sotha Sil Expanded](http://www.nexusmods.com/morrowind/mods/42347/?) - Trainwiz's epic mod that completely overhauls the final dungeon of the Tribunal expansion. Conflicts with anything changing Tribunal's final dungeon. Less Generic Tribunal MIGHT be fine, as I can't find anything saying otherwise, but I haven't made it far enough in the Tribunal story to test it with the newest version of LG Tribunal.

6) Want a mod that gives your character needs?
* [Necessities of Morrowind](http://mw.modhistory.com/download-53-12114) - For a long time, NoM was the only needs mod Morrowind had. NoM has several compatibility patches with various mods as a result. Seeing as it actually adds quite a bit to the world with food stalls, restaurants, wells, etc., if you plan to use NoM you should keep compatibility in mind. Alternatively, you could use the new mod The Bare Necessities instead, which strips out a lot of things NoM added (world changes, new items, cooking system) while keeping hunger, thirst and the need for sleep. You can find it [here](http://www.nexusmods.com/morrowind/mods/43365/?).

7) Want kids in your game?
* [Children of Morrowind](http://lovkullen.net/Emma/kids.htm) - If you want kids, or to play a teenager, in Morrowind, this mod is your only option. Because this mod adds NPCs and items to settlements all over Vvardenfell, you should keep an eye out for any compatibility patches if you use this mod. And one last thing, CoM was designed in a way to keep the children of the mod safe, meaning if you attack them, they'll teleport away before you can hurt them. This was a design decision on Emma's part, so if you don't like invincible kids, don't download the mod.

8) Want mods to add atmosphere or to give you a more immersive experience?
* [Mountainous Red Mountain](http://www.nexusmods.com/morrowind/mods/42125/?) - Makes Red Mountain much bigger, at the cost of breaking compatibility with any mod centered in and around Red Mountain. It's popular enough that there are compatibility patches for most popular mods. I believe there's a patch for Julan and another patch for Greater Dwemer Ruins 1.0.
* [Gondoliers](http://www.nexusmods.com/morrowind/mods/43291/?), [Boat](http://www.nexusmods.com/morrowind/mods/42270/?), [Silt Striders](http://www.nexusmods.com/morrowind/mods/42267/?). All by abot. Travel in real time instead of instantaneously!
* [Where are all birds going](http://www.nexusmods.com/morrowind/mods/43128/?) and [Water Life](http://www.nexusmods.com/morrowind/mods/42417/?), by the same wonderful guy who made the above mods, adds birds and aquatic creatures to Morrowind.
* [Animated Morrowind](http://abitoftaste.altervista.org/morrowind/index.php?option=downloads&task=info&id=39&Itemid=50) - Adds NPCs to the game with new and unique animations to make the world feel more alive.
* [Starfire's NPC Additions](http://mw.modhistory.com/download-90-13583) - Adds a ton more generic NPCs to the world to make it feel more lively, with a lot less 'getting destroyed by a high level vampire on the road to Pelagiad in the fucking DAYLIGHT' than Morrowind Comes Alive had. (I'm not bitter or anything.)

9) Are you an aspiring member of House Telvanni? The following mods might interest you, and as a bonus, they can all be used together

* [Uvirith's Legacy](http://download.fliggerty.com/download-35-884) - A major revamp of Tel Uvirith, your stronghold if you join and advance in House Telvanni. Make sure to use the RoHT addon from the addons folder if you plan to use Rise of House Telvanni (see below).

Using TR? [Here](https://www.nexusmods.com/morrowind/mods/44656) is a patch for it.

* [Building Up Uvirith's Legacy](http://mw.modhistory.com/download-47-11851) - This mod is a major revamp of Uvirith's Grave, which is the area surrounding Tel Uvirith. If you plan to use Uvirith's Legacy, this is the version of BuUG you should use.
* [Rise of House Telvanni](http://mw.modhistory.com/download-21-10664) - Further expands the Telvanni questline in a major way. Be warned there are some... special characters included in this. Do NOT get the compatibility addon! It's very out of date, use the one from Uvirith's Legacy instead!

>Q: What if I plan to join House Hlaalu or Redoran instead of Telvanni?
>
>A: If you plan to join House Redoran, you're in luck: you've already downloaded and installed the best major overhaul for Redoran around if you've followed this guide to the letter, and that would be the LGNPC suite. The LGNPC mods cover the entirety of House Redoran at this point in time, and a lot of their holdings, making a House Redoran playthrough a lot of fun. Also, the new mod [Bal Isra Rising](http://www.nexusmods.com/morrowind/mods/44329/?) overhauls the Redoran player stronghold. At this time it looks like it MIGHT have some compatibility issues with LGNPC Indarys. If you want to be totally safe, you could play the mod without LGNPC Indarys activated, or you could wait for a compatibility patch from the mod author. If you want to use both, it sounds like the worst case scenario is that you might have to use the console to go to the old version of Indarys Manor to talk to NPCs inside it for new dialogue.

If you're going to join House Hlaalu... well, unfortunately, at this time, there really is nothing I can recommend. There are a few mods that revamp Rethan Manor, but nothing really spectacular stands out. House Hlaalu is still a very vanilla experience.

11) Annoyed with how quickly vanilla torches go out? While you're at it, want them to put out more light? What about lanterns and candles? Try out [True Skyrimized Torches](http://www.nexusmods.com/morrowind/mods/43192/?).

12) Do you feel like you don't get enough benefits from being in a guild? Do you want more perks from joining the Temple or the Cult? Want to boss around your underlings after you become the Head of a House? You might like [Antares' Big Mod](https://arcimaestroantares.webs.com/antaresbigmod.htm).

13) Hate the limited capacity of chests and boxes? Want to get rid of that? [Ta-da](https://www.nexusmods.com/morrowind/mods/45698). Honestly, best mod addition I've added so far. So much hassle and annoyance saved.

## Screenshots

If you would like to see reference images of the finished install, or contribute your own screenshots to that public repository, head to our [Google Drive Gallery](https://drive.google.com/drive/folders/1pusVDmDBMwM1Si28W8wcvVd6aXukEIJr?usp=sharing).

## Contributors

This project wouldn't be possible without the help of all the amazing people I've met on the way. :)

* owlnical - for direct contribution to the Github repo, advice and helping to expand and continue the project into the future
* /u/Tiber-Septim - for long comments helping me to find areas to improve the project as they walked through the install process
* Corsair - for putting up with my annoying Discord questions and helping an immense amount from finding mods to understanding technical details of Morrowind modding
* yooksi - for doing an insane amount of work. The updater, tons of mod additions, lots of tweaking and testing, and likely putting in more hours than I have into the project.
* The many people from the Morrowind Modding Discord and /r/Morrowind subreddit who've helped me in many ways.

Thank you all for everything!
