# Sprite Flight

## Play the Game
**Unity Play Link**: [(https://play.unity.com/en/games/8bd8a621-bfa4-461b-981a-71d87fbbddf6/sprite-flight)]

## Game Overview
In this game, the player steers a rocket through space to avoid asteroids, scoring higher for the longer they avoid collisions.  

### Controls
The game uses the mouse/trackpad for controls.
Player moves the rocket via mouse clicks (of the left key only). The rocket will rotate and move in the direction of a click. 
When the mouse key is held down, the rocket accelerates, and when the key is released, it decelerates. 

### How to Play
The objective of this game is to avoid obstacles, which are the floating asteroids and the borders of the gameplay area. 
Players click in the direction they want to turn or move the rocket to evade the asteroids. 
If the player collides with an asteroid or the game borders, the rocket explodes and the game ends, with the option to restart.
The score increases the longer the player goes without collision, and the objective is to get the highest score possible. 

## Base Game Implementation

### Completion Status
- [x] Player movement and controls
- [x] Obstacle spawning system
- [x] Collision detection
- [x] Score system
- [x] Game over state

### Known Bugs
- No known bugs

### Limitations
- Max speed of asteroids is not clamped. So far, I have not seen them accelerate to a point in which playing the game becomes impossible, but this could theoretically occur. 

## Extensions Implemented

### 1. [Create A Cohesive Color Scheme] (2 points)
**Implementation**: Used an online palette generator and applied these colors to game elements
**Game Impact**: Increases visual appeal of game through color scheme unity. 
**Technical Details**: Changed colors of Player object, Obstacle prefab, Borders object, and GameUI text via typing in hex codes from palette generator. 
**Known Issues**: No known bugs

### 2. [Destroy the Borders on Game Over] (4 points)
**Implementation**: Set borders to disappear when the Player object is destroyed
**Game Impact**: Creates distinction between regular gameplay and "Game Over" state.
**Technical Details**: Added code to PlayerController to deactivate Borders GameObject when player collides with either borders or an obstacle
**Known Issues**: No known bugs

### 3. [Add Ambient Background Particles] (4 points)
**Implementation**: Added a particle system and adjusted settings to create "starry" look
**Game Impact**: Increases player immersion by adding to outer-space atmosphere
**Technical Details**: Adds a new particle system on a layer below other game components
**Known Issues**: No known bugs

### 4. [Increase Difficulty Over Time] (5 points)
**Implementation**: Changed bounciness of obstacle material
**Game Impact**: Asteroids slightly increase speed with each collision, making gameplay gradually increase in difficulty. 
**Technical Details**: Changed PhysMat_Bouncy bounciness from 1.0 to 1.1
**Known Issues**: Maximum speed not clamped. Has not been an issue so far but has the potential to create issues in the future. 

### 5. [Add Sound Effects and Background Music] (5 points)
**Implementation**: Added Audio Components to existing elements of the game
**Game Impact**: Increases player immersion by providing atmospheric music and audio feedback for rocket destruction
**Technical Details**: Added and configured Audio Components. 
Background music is added to Main Camera, and loops automatically as soon as the game is run. 
Explosion sound effect is added to ExplosionEffect particle system, and is triggered on Player sprite destruction through the same code as the particle system. 
**Known Issues**: No known bugs

## Credits
- Explosion SFX: sfx-Explosion.ogg from Unity Sprite Flight tutorial: [(https://unity-connect-prd.storage.googleapis.com/20250521/92b774c0-a17b-4f72-ab52-4e4c42d20074/sfx-Explosion.ogg)]
- Background music: sfx-MusicEthereal.ogg from Unity Sprite Flight tutorial: [(https://unity-connect-prd.storage.googleapis.com/20250521/9ff2422f-9c44-4165-9a57-6fb0621c2320/sfx-MusicEthereal.ogg)]

## Reflection
**Total Points Claimed**: [Base: 80% + Extensions: 20% = 100%]
**Challenges**: I struggled to configure Unity and GitHub, as I had initial issues with the .gitignore file. I think my biggest struggles for this project came from outside of Unity!
**Learning Outcomes**: I learned quite a bit about the basics of 2D game development in Unity. 
I learned important techniques like creating prefabs, setting up player controls, setting colliders, adding audio, and working with particle systems, among many other things. 
