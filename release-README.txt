HousePartyVR 0.7.0 (beta)
=========================

Play House Party in PC VR. Roomscale with your own hands: walk around the party, grab and throw things, and treat
people as physical bodies with weight. You can lead them, pose them, carry them, ragdoll them, and take their
clothes off by hand. A sandbox radial menu adds moods, feelings, dancing, poses, god mode and slow motion.

ADULTS ONLY (18+). House Party is an adult game and this mod includes adult interactions. Nudity and sex scenes need
the game's own official Explicit Content Add-On (paid DLC on Steam) with censoring turned off in the game's settings.
The mod does not unlock or bypass anything: without the add-on, underwear stays on.

BETA: tested on one setup only (Meta Quest 3 through Virtual Desktop, RTX 4090). Other headsets and runtimes
should work through OpenXR but are untested. Expect rough edges.


Requirements
------------
- House Party on Steam (the current Unity 2022.3 version), Windows.
- A PC VR headset with an active OpenXR runtime: Virtual Desktop (VDXR), SteamVR, or Meta Quest Link.
- MelonLoader 0.7.3: https://github.com/LavaGang/MelonLoader
- A strong GPU. The game renders twice, once per eye.


Install
-------
1. BACK UP YOUR SAVES first: %USERPROFILE%\AppData\LocalLow\Eek\House Party\Saves
   (god mode, on by default, changes relationship values, and those are saved; see "God mode" below).
2. Install MelonLoader 0.7.3 into House Party: run the MelonLoader installer, pick HouseParty.exe, and choose version
   0.7.3. Launch the game once so MelonLoader can set itself up, then quit.
3. Extract this zip into the House Party folder (the one that contains HouseParty.exe) and let it merge folders.
   It adds these files:
     Mods\HousePartyVR.dll
     HouseParty_Data\Plugins\x86_64\UnityOpenXR.dll
     HouseParty_Data\Plugins\x86_64\openxr_loader.dll
     HouseParty_Data\UnitySubsystems\UnityOpenXR\UnitySubsystemsManifest.json
4. If you use ReShade or anything else installed as dxgi.dll in the game folder, rename it to dxgi.dll.off while
   playing in VR.


Play
----
- Connect your headset and make sure its OpenXR runtime is the active one, then launch the game.
- VR starts by itself a few seconds after the first scene loads. F6 starts and stops VR.
- While in VR, the game runs in a 1920x1080 window and the desktop window shows black. Keep that window focused:
  a strong controller buzz when you press a button means it is not in front, so click it.
- F7 (or holding the right stick click) recenters. Stand up straight when you do: your standing height is taken
  from it.


Controls (right-handed; set LeftHanded=true to swap hands)
--------------------------------------------------------
Walk in your room      Your character walks with you; duck to crouch.
Your hands             Your character's arms follow the controllers; squeeze the grip to close the fingers.
Left stick             Walk (relative to where you look).
X (hold)               Run.
Right stick            Turn (smooth by default; TurnMode=Snap for snap turns).
Right stick click      Tap: combat mode on/off. Hold: recenter.
Left stick click       SANDBOX RADIAL. It works on whoever the laser points at: clothes, mood, feelings, dance,
                       knock out / wake up, freeze, bring / pose, intimacy. It also has pages for everyone, for
                       yourself (god mode, strip/dress, sober up), and for slow motion. Tilt a stick to choose;
                       trigger or A picks; B goes back.
Grip (either hand)     On an item: hold it; swing and let go to throw.
                       On a person: your hand holds that spot.
                         - Hand or arm: you lead them.
                         - Head, back or hips, or two hands: you pose them like a doll, feet planted
                           (push the head forward and they bend over).
                         - Yank hard: they lose their balance.
                       Bodies have weight: one hand drags, two hands lift.
Swing into someone     Hit them: a medium swing staggers, a hard one knocks them over, a very fast one knocks
                       them out.
Right trigger          While holding someone awake: they go limp as a ragdoll you can position (they get up after
                       you let go).
                       On clothing: pull it. Solid garments tear off into your hand; skirts and dresses lift first.
                       Release the garment on them to put it back, anywhere else to drop or throw it.
                       In game menus: click.
A                      While holding someone: freeze their pose (A again to unfreeze).
                       Otherwise: use what the laser points at (the game's action wheel).
B                      Back / pause menu. In a conversation, hold B to leave it.
Y                      The game's radial (inventory, memories, opportunities).
Laser on game menus    Moves the mouse; trigger clicks.

Keyboard and mouse keep working.


God mode (on by default)
------------------------
You start in god mode. It sets everyone's romance, friendship and trust toward you to the maximum and their fear and
offense to zero. THESE VALUES ARE WRITTEN INTO THE GAME'S STATE AND YOUR SAVES. In god mode, conversations that people
start on their own are also closed at once.

To play normally, set StartInGodMode=false and GodModeMaxRelationships=false (see Settings), and leave god mode off
in the radial.


Intimacy (Explicit Content Add-On required)
-------------------------------------------
Open the sandbox radial on someone, then Intimacy. These are the game's own sex acts, with a willing partner within
2.5 m. In god mode that is anyone awake who loves you. Nobody is teleported to a bed: the two of you line up in the
game's own pose right where your partner stands.
- Left stick: slide you both (out of a wall, onto a bed).
- Right stick: turn you both.
- Your view moves into your character's eyes. Hold the right stick click (or press F7) to re-fit it.
- Your hands stay free. Thrusting (your head moving toward and away from your partner) fills the orgasm meters.
- Hold B to stop.
It never works with, and ends at once for, anyone who is knocked out, ragdolled, getting up, frozen, or in a
scripted scene.

Grip at your own crotch to masturbate (the game's own act; stroke along the shaft).


Settings
--------
UserData\MelonPreferences.cfg, section [HousePartyVR]. Edit it while the game is closed; the file is created after
the first run. Useful ones:
- Comfort and movement: TurnMode, SmoothTurnDegreesPerSecond, SnapTurnDegrees, DuckToCrouch, LeftHanded
- People: PeopleByHand, HandStrength (lower = heavier people), LeadUpperBodyStiffness, PoseHipStiffness,
  PoseLegStiffness, WakeAfterGrabSeconds, TouchPhysics, NpcsBackAwayFromYou
- God mode: StartInGodMode, GodModeMaxRelationships, GodModeLeavesForcedConversations
- Intimacy: FreeformIntimacy, GodModeEveryoneWilling, ThrustSensitivity, HandsOnYourself, StrokeSensitivity
- Display and performance: RenderScale, DesktopMirror, VrMirrors, VrScreenSpaceReflections


Troubleshooting
---------------
- Log: MelonLoader\Latest.log; look for lines starting with [HousePartyVR].
- VR does not start: check that your headset's OpenXR runtime is active, and rename any dxgi.dll in the game folder.
- No nudity: the log's "Content:" line says whether the Explicit Content Add-On or the censor setting is the problem.
- Buttons do nothing (strong buzz): click the game window on the desktop.
- Known limits:
  - If censoring is on, its mosaic is drawn on the menu panel, not on the bodies.
  - The Shake Light can't be shaken.
  - People can briefly vanish in the left eye when you peek around a door frame.


Uninstall
---------
Delete the four files listed under Install (step 3). Your saves are not touched by uninstalling; restore your backup
if you want god mode's relationship changes undone.


Third-party files
-----------------
UnityOpenXR.dll, openxr_loader.dll and UnitySubsystemsManifest.json come from Unity's OpenXR Plugin
(com.unity.xr.openxr 1.14.3). See the licenses folder: Unity's package license, and the Khronos OpenXR loader under
Apache 2.0. Unofficial fan mod, not affiliated with Eek! Games or Unity.
