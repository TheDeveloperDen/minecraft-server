---
cover: >-
  https://images.unsplash.com/photo-1552664730-d307ca884978?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2970&q=80
coverY: 0
description: >-
  The Den has a custom claims plugin that can be used to protect your buildings
  from griefer
---

# Claims

## The Claim Tool

{% hint style="info" %}
Any golden shovel can be used for claiming
{% endhint %}

The Claim Tool is used to select the area you want to claim.&#x20;

To do this, you need to hold the tool, and right click on a block. This sets the first corner for your claim. Then right click on another block for the 2nd corner. The overall claim size must be at least **10x10** blocks, but apart from that it can be any size within your budget.

{% hint style="info" %}
&#x20;Claims cover all Y coordinates.
{% endhint %}

You can get a claim tool for free once a day from `/kit`

## Creating a Claim

Once you have selected your claim area with the Claim Tool, you can make it into a claim!

Claims have to have a name, which can be anything. Names can be used to keep track of different claims.

To create a claim, use the command `/claim <name> create`, replacing `<name>` with the name of the claim. For example, to create a claim named `home`, you would type `/claim home create`



## Managing Claims

### Info

You can use the command `/claim <name> info` to view information about one of your claims. This includes its size, location, and who is trusted.

Alternatively, you can stand in any claim and just run `/claim info` to show information about that claim.

### Deleting a Claim

To delete a claim, use the command `/claim <name> delete`

### Resizing a Claim

To resize a claim, select a new region with the [Claim Tool](claims.md#the-claim-tool) and then use the command `/claim <name> resize`

### Renaming a Claim

To rename a claim, use `/claim <name> rename <newname>`

### Claim Protections

By default, claims are completely protected. Other players can't break or place blocks, fire won't spread, explosions won't destroy anything, chests and other containers can't be opened, PvP is disabled, and friendly mobs can't be hurt.

All of this can be changed if you want, by changing the claim's protections.

This is done using the command `/claim <name> protection add/remove <protection>`

For example, let's say we want players to be able to PvP in a claim called `arena`. To do this, we'll remove `pvp` protection using the command `/claim arena protection remove pvp`. To add it back, we'd do `/claim arena protection add pvp`

These are all the different protection types that can be customised:

* `animals` - Stops players killing friendly mobs
* `break-blocks` - Stops players breaking blocks
* `place-blocks` - Stops players placing blocks
* `containers` - Stops players opening any chests, furnaces, barrels, or any other container
* `fire` - Stops fire from spreading in the claim
* `interact` - Stops players from using buttons, levers, doors, item frames, armor stands, enchantment tables, pressure plates, or any other interaction
* `explosions` - Stops explosions from destroying blocks in the claim. **You will still take damage!**
* `pvp` - Stops players from attacking each other

{% hint style="info" %}
There is no flag to protect hostile mobs, however if a hostile mob is named with a nametag, other players won't be able to attack it.
{% endhint %}

### Trusting Players

There are different levels of roles you can give to other players to let them interact with your claims. This is done with the command `/claim <name> setrole <player> <role>`

There are **4** different roles that you can give:

* `visitor` - Everyone is this role by default. They can only do what's allowed in the [protections](claims.md#claim-protections)
* `member` - Players with this role will bypass the claim's protections
* `trusted` - Players with this role will bypass protections, and can also add and remove members
* `owner` - **This gives someone ownership of your claim. There can only be 1 owner. Be careful with this!**

In simple terms, to "trust" a player, use `/claim <name> setrole <player> member` and to untrust them use `/claim <name> setrole <player> visitor`

## Subclaims

This is an advanced feature which allows you to make smaller claims inside a claim. This has a variety of uses such as making a PvP arena with the `pvp` protection turned off or a public cow farm with the `animals` protection turned off.

These are managed with the command `/claim <name> sub` and follow a similar structure to the main commands.

To create a subclaim, we [select a region](claims.md#the-claim-tool) and use `/claim <name> sub <subname> create`. This creates a subclaim named `<subname>` inside the claim `<name>`

The subclaim can now be managed using very similar commands to a normal claim, except starting with `/claim <name> sub <subname>`.

For example, `/claim <name> sub <subname> protection remove pvp` would allow pvp in our subclaim named `subclaim`
