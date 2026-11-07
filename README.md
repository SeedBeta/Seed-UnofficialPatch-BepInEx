# Seed-UnofficialPatch-BepInEx

Welcome to the repo! <br>
06/11/26 - This ReadMe.MD is incomplete, I have more patches and fixes to add at the bottom, things will change!

There's not a lot here (yet), but as time goes on, I am working towards a working plugin. <br>

P.S: If you're from Klang, it'd be awesome if any of these patches are genuinely able to help

---

## Disclaimer

Although this is something made entirely in good faith to reduce frustrations
and improve the accessibility of the game, it's important to be clear:

> This isn't something approved for use, although there are no rulings or
> conditions directly against its use.
>
> **This is by no means green-lit for use or advertisement.**

You **could** be punished.  
You **could** be suspended.  
You **could** be outright banned.

The decision is entirely down to Klang and any relevant people involved in
the game's moderation.

**If you are even remotely unsure, do not use this.**

---

## To clear the air...

Just a note on a few things I'd like to mention:

### What is this?

This repo is nothing more than the changes required, this is just the plugin for Bepin
It interacts with Seed in real time, fixes a host of bugs, and improves certain functionality by instructing the game to use these patches in real-time

### Cheating, Modding & Detection

To be clear:
> This repo/plugin does not allow other mods to be created, nor cheats to be made.<br>
> It also does not allow people do things which the developers did not intend _(more on that below)_.

---
<details>
<summary><strong>Detection</strong></summary>
  Plugins, patches, and mods can be detected VERY easily.

- They **will** show up in memory crash dumps.
- They **will** display in any developer consoles or local logs.
- Bug reports **will** send this information to Klang.

I have no doubt that changes would be visible in the user's communications
to the server.

> _(Although I am unsure, as I have no plans to be digging through files like
> that.)_

If so desired, preventing this kind of patching/plugin would be quite easy.

</details>

---

<details>
<summary><strong>Cheating & Modding</strong></summary>

For the curious, the game is run using a
[client-server model](https://create.roblox.com/docs/projects/client-server)
_(This is something easy to understand if interested)_.

The client (your game) is nothing more than a way for you to interact with the
server and receive its outputs.

If it was modded to make your _"seedling teleport somewhere"_, or you
_"want to access something you otherwise couldn't"_, a mod/patch/plugin
couldn't _(and shouldn't)_ ever let you do that.

The game always needs to communicate with the server:

> _"Can I do this?"_
>
> In practice, you could change the question to a command:
> _"I would like to do this."_

Ultimately, this wouldn't work. The server is the one that makes the final
decision, and your game _must_ wait for the server's confirmation. There is
no other option.

If the client refuses to listen to the server, the client will likely
desynchronise, probably disconnect from the server with an error, or just
flat-out crash due to unexpected behaviour.

</details>

---

<details>
<summary><strong>How do cheaters... Cheat?</strong></summary>

It sure as hell isn't through modding in patches... Not really for a game like
Seed, anyway...

I'll put a little rant below explaining some of the ways cheats kind of work,
but I'm going to avoid too many details and intricacies.

<details>
<summary>A rant</summary>

Cheating can mean a whole bunch of different things. 
A mod _could_ be a cheat, but that doesn't mean every mod is one. 
Broadly speaking in the context of this repo, modifying the game client is very easy to detect, patching in-real time, even more so.

In my opinion, serious cheating, especially in a game like Seed, isn't done by modifying game files.

Sometimes it's macros running through a separate program, as it watches the game
for changes, then completing predetermined movements or selections to automate
tasks.

Other cheats might use separate software to interact with the game or intercept it's communcations.
Other times, cheats are run on an entirely separate machine, keeping the client 'squeaky clean' whilst the second machine is actually intercepting traffic and doing the 'cheating', it doesn't make them invisible, but it's how a lot of serious cheating in online games take place.
Particularly in high-stakes games and PVP...

I can't be bothered anymore.
This repo solely is intended to fix bugs and improve accessibility for others, not that I'm not denying there is a risk using it.

---

The point I'm trying to unravel is.

Mods are just a part of the puzzle that can genuinely make things better for people, or ruin games.
_'People shouldn't be able to change game files'_ Is a totally valid point, and something that should be discussed; <br>
But, at the same time, it doesn't mean much, or progress any conversation in any meaningful way, especially when it's used as a pivot of _'These people are bad'_

It shuts down any kind of open discussion for working towards improvements, and divides people who have the common goal of genuinely want to make the game better.

In a sense, using Discord 'In-Game Overlay' actually hooks into the games rendering pipeline to provide the overlay. <br>
ReShade, it's a great tool for adjusting contrast and color, and can provide many visual filters for glare, it can provide genuine benefits for people who struggle, but it can also trip anti-cheats. <br>
Some people force DLSS / FSR onto games in a bid to try squeeze Seed into running on a laptops and mobile devices it otherwise would struggle to run, and can make deep-modifications into the game to make such changes. <br> <br>

I don't bring these up to play semantics, but rather point out, these things are far more a-like than people realise, and there is far more substance any conversation than just _'No'_ and slamming the door.


</details>

</details>

# What's to come? Where is everything?
---

Now the dramatic stuff is out of the way, what does this actually do? <br>
What does it fix?

To keep it simple, I've listed what I plan to port from the previous repo to this new project. <br> 
I've also included things that previously existed but are either no longer required, or won't be ported.

These changes will need to be rebuilt rather than simply copied over. <br> 
Although I know **how** the fixes were made and still have the shared code and notes, this
implementation will effectively be an abstract layer inserted into the game.

I genuinely don't know how easy these changes will be to port, especially the
ones that are more deeply rooted. <br> 
They will take time to figure out, and some may turn out to be entirely impractical... <br> 
Unfortunately there will likely be only one contributor going forward and I do not have the same quantity of free time I had 2 months ago, but I'll give it a swing.

## What's being changes/added

Nothing in this project is intended to add new features or UI elements,
automate tasks, or change the balance of how things are done.

Anything from the previous project that could be considered a _feature
addition_ is listed for clarity, but I **do not** plan to reimplement it here.

> **Status labels:** Items marked *(Porting)*, *(Planned)*, *(Not Planned)*,
> *(Needs Investigation)*, *(Failed)*, or *(Deprecated)* describe their
> current status or plans. *(Completed & Worked)* and *(Did Not Complete)*
> describe their status in the previous project.

---

<details>
<summary><strong>1. Bug Fixes</strong></summary>

Things that are clearly intended to exist in the game, but are broken.

- Haul Job — Outside of Society — **(Failed)**
- Multi-boxes: Pick-up Action — Outside of Society — **(Porting)**
- Multi-boxes: View Container UI — Outside of Society — **(Porting)**
- Prevent Go-to Actions Being Created Whilst in UI — **(Porting)**
- Resource Deposit View Icons Flushed to Terrain — **(Planned)**
- Terrain Storage Dumping: Memory Leak/Game Lock-up — **(Planned)**
- Prevent Flaxa Select-Through — **(Planned)**

</details>

---

<details>
<summary><strong>2. Performance Improvements — Fixes</strong></summary>

Fixes for performance issues, or improvements that don't change what the game is intended to show or do.

- MSAA Bluescreen Fix for Intel — **(Deprecated)**
- Resource Deposit View: Reduce Raycasts / Improve FPS — **(Planned)**
- Terrain Storage Dumping: Memory Leak/Game Lock-up — **(Planned)**
- Building Stability Checks: Lag/Game Freeze — Big O Notation Lag — **(Not Planned)**
- Build Deconstruction Mass-selection: Lag/Game Freeze — **(Needs Investigation)**

</details>

---

<details>
<summary><strong>3. Performance Improvements — Additions</strong></summary>

Performance improvements that added functionality or actively changing how things are rendered. <br>
It is unlikely that anything here will be added or rebuilt.

- FOW Culling — **(Did Not Complete)**

</details>

---

<details>
<summary><strong>4. Feature Fixes & Improvements</strong></summary>

Adjustments to existing features to make them work better. <br>
Some may potentially be added, so long as they are fixes problems and not changes.

<details><summary>Plant/Small Hitboxes Stationary Square - <strong>(Porting)</strong></summary>
  Whoever made the Mushroom hitboxes a stem that feels like it's 3 pixel wide, then jiggles in the wind should be subject to execution. <br> 
  This genuinely pisses me off beyond measure, it's unbelievably frustrating on a touch-pad & touch-screen.<br>
  I have shaky hands, it's the most hostile feature imaginable and feels like there was very little consideration.<br> <br>

  Anyway, plan is to render a stationary square bounding box over the Mushrooms pivot position.</details>
- Hide/Flag Exhausted Resource Deposits — **(Completed & Not Planned)**
- Multiple Selection UI — **(Not Planned)**

</details>

---

<details>
<summary><strong>5. Added Features</strong></summary>

Direct additions for which no equivalent existence in the game currently. <br>
These are unlikely to happen and **will not** be ported over.

> Statuses below refer to the **previous project**.

- Building Ext.: Clone Last Floor — **(Completed & Worked)**
- Building Int.: Clone Floor Layout — **(Completed & Worked)**
- Building Int.: Instant Elevator — **(Completed & Worked)**
- Mouse Hover: Inventory Preview — **(Did Not Complete)**
- Action Queuing: Predicted Inventory Reservation — **(Did Not Complete)**

</details>
