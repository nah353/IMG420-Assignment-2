# GDExtensions for Animated Sprite2D nodes

## 1. PulsingSprite (animated)

**Description:**
Creates a gradual fade in/fade out effect for Sprite2D texture. The sprite gradually scales up while active and back down while inactive. Within the game, the PulsingSprite node is used to animate the boost effect by pulsing outward when the player is boosting, then fading back out when the player is not boosting.

**Parameters:**
- pulse_speed: controls speed of the pulse effect's growth
- fade_out_multiplier: controls how quickly the sprite fades out when inactive

**Signals:**
- receives a signal handled by method "_on_player_boosting_changed" to begin pulse effect
- emits a signal called "pulse_complete" when the sprite is fully revealed - used for modulating ship color and playing a sound effect when sprite is fully revealed or "pulsed"

## 2. GrowingSprite (animated)

**Description:**
Similarly to PulsingSprite, animates a Sprite2D node. Creates a growing effect, with the sprite initially invisible and gradually growing outward until reaching full size. Within the game, the GrowingSprite node is used to animate new lives being added to the HUD, with a sound effect playing when the life sprite has fully expanded.

**Parameters:**
- growth_speed: controls speed of the sprite's growth outward

**Signals:**
- receives a signal handled by method "_on_life_added" to begin growth effect of sprite
- emits a signal called "growth_complete" when the sprite is fully expanded - used for playing a sound effect when the sprite is fully expanded

# Compilation Info
Built using Godot version `4.5.beta`. I initially compiled with C++ bindings built following the [GDExtensions tutorial](https://docs.godotengine.org/en/4.4/tutorials/scripting/gdextension/gdextension_cpp_example.html#building-the-c-bindings) and building with "scons platform=<platform>" at the root of the project directory - SConstruct file already included in the project. 
