---
layout: page
title: The Elder
description: The Elder is a 3rd-person Adventure Platformer made in Unreal Engine 4.22.
---

# Climbing System

When creating the climbing system for The Elder I was faced with a unique problem. In regular climbing systems, the programmer can rely on the level designers to make sure that climbable points are evenly spaced and work properly within that specific environment.

With my system though, the player can place climbable points at any point, whether the player could reasonably fit at that spot or not. I'm pretty happy with the solution I've created for this game, and I've detailed how it works below.

<script>
foo
</script><video width="520" height="300" controls loop preload=metadata src="https://cdn.jsdelivr.net/gh/hcorion/hcorion.github.io/assets/images/theelder/ClimbingMoving.webm" type="video/webm"></video>


<!--<iframe width="520" height="300" src="https://cdn.jsdelivr.net/gh/hcorion/hcorion.github.io/assets/images/theelder/ClimbingMoving.webm"></iframe>-->

## Core System

So the basics of the the system works like this:

1. Get the direction that the player is inputting (indicated by light blue arrow in diagram)
2. Get all climbable object in that direction.
3. The climbable objects that are farthest away are given the largest score (indicated in diagram by *1.0*).
4. Climbable objects that are farther to the left and right of our target vector are given less priority.
5. The object with the highest score is then checked to see if the player can safely go there without intersecting with other collision.

![Diagram of the Climbing System](/assets/images/theelder/ClimbingDiagram.png){:height="450px" }

The climbing system also fully supports moving climbable points, which was seen briefly in the boss fight.

<video width="520" height="300" controls loop preload=metadata>
    <source src="https://cdn.jsdelivr.net/gh/hcorion/hcorion.github.io/assets/images/theelder/JumpingOnMovingClimbable.webm" type="video/webm">
    Sorry, your browser doesn't support embedded videos.
</video>

Some cool content that never made it into the final game, was the ability to bounce crystals off of mushrooms.
<video width="520" height="300" controls loop preload=metadata>
    <source src="https://cdn.jsdelivr.net/gh/hcorion/hcorion.github.io/assets/images/theelder/BouncyMushroomClimbable.webm" type="video/webm">
    Sorry, your browser doesn't support embedded videos.
</video>

## Mantling

I decided to have mantling be a designer-placed feature rather than a runtime/build-time feature, due to the scope of the game, and the relative ease for me to implement the feature.
It leveraged Unreal's Spline component to create a system that was simple and easy to use for our Level Designer.

<video width="520" height="300" controls loop preload=metadata>
    <source src="https://cdn.jsdelivr.net/gh/hcorion/hcorion.github.io/assets/images/theelder/Ledges.webm" type="video/webm">
    Sorry, your browser doesn't support embedded videos.
</video>

# Final Boss - WIP

## Description

## IK/FK

## Stealth System

# Checkpoint System - WIP

## Core System
