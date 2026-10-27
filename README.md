Claude (Anthropic) generated

# CameraPitch (WotLK 3.3.5a)

Keybinds for looking up and down with the camera, so you don't need to hold
right-click and move the mouse. Made for playing on a controller or handheld
(e.g. Lenovo Legion Go), or when the mouse is uncomfortable to use.

WoW 3.3.5a has keybinds for turning left and right, but none for looking up and
down. This addon adds them.

## Features

- **Camera Look Up / Look Down**: tilts the camera while the key is held.
- **Camera Pan Left / Right**: swings the camera around your character
  without turning you, like holding left-click and moving the mouse.
- **The game's own Pitch Up / Pitch Down binds now also move the camera.**
  Your flight or swim angle and the camera move together, like
  right-click + mouse up/down.
- Adjustable speed, saved between sessions.
- Works in combat.

## Installation

1. Download and extract the zip.
2. Put the `CameraPitch` folder in `World of Warcraft/Interface/AddOns/`.
   The path should be `Interface/AddOns/CameraPitch/CameraPitch.toc`, not a
   folder inside another folder.
3. Restart the game, or type `/reload` if you are already logged in.

## Setup

**Esc → Key Bindings**

- **Camera Pitch** section: Camera Look Up/Down and Camera Pan Left/Right.
  These move only the camera.
- **Movement** section: Pitch Up/Down (built into the game). With this addon,
  the camera follows them. This is the "right-click style" option for flying
  and swimming.

## Slash commands

| Command | What it does |
|---|---|
| `/campitch` | Shows current speeds and help |
| `/campitch 60` | Sets the camera up/down speed |
| `/campitch 60 120` | Sets the up/down speed and the left/right pan speed |
| `/campitch follow` | Turns the camera tilt on Pitch Up/Down on or off |

If the camera and your character's pitch drift apart while flying, change the
first number until they match better.

## Known limitations

- **On the ground, only the camera moves.** Characters on foot can't pitch.
  This is how right-click behaves too.
- **Pitch can go further than the camera.** The game limits how far the camera
  can tilt, especially near the ground, but your flying or swimming pitch can
  go steeper. If you hold Pitch all the way, the camera stops and they drift
  apart. Tap the opposite direction to bring them back together.
- **Not perfectly synchronised.** The camera and the character pitch at
  separate speeds. Use `/campitch <number>` to get them close.
- **Steering needs the game's Pitch binds.** Addons can't make your character
  pitch from their own keybinds, so the steering feature uses the game's
  built-in Pitch Up/Down binds instead.
- Tested only on WotLK 3.3.5a (Warmane). Other versions may not work.

## What to know

- Uses only built-in WoW API functions (`MoveViewUp/Down/Left/Right`, hooks
  on `PitchUp/Down`). It does not automate anything or play for you. Each key
  press is your own input, like a normal keybind.
- No code taken from other addons.
- Settings are saved in `WTF/Account/<account>/SavedVariables/CameraPitch.lua`.
  Delete that file to reset them.

## Credits

Made by Radu (idea, design, in-game testing), written with help from Claude
(Anthropic's AI).
Inspired by the same need as older addons like *Camera Keys* (2006) and
*Camera Tilt* (ajhyun, retail). No code from either.

## License

MIT. Use, modify and share freely. See `LICENSE.txt`.
