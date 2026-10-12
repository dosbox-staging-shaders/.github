# DOSBox Staging - A Maintained DOS Environment for Games and Tools

## Product Snapshot

DOSBox Staging tracks the DOSBox line and modernizes how it presents on a current PC. Sound fonts, pixel-perfect or shader output, and a readable config replace a pile of unofficial builds that used to circulate for one feature each. The guest is still DOS. The host is Windows, and the program you run is one you supply.

Mount a directory, set the working drive, and start the executable. That is the whole loop for a large share of DOS software. Disk images matter when a program expects a CD or a hard-disk layout. Cycles still matter when something runs too fast. Staging does not remove those DOS facts. It makes the defaults less fragile.

## What You Set

| Setting | Start here | Change it when |
|---|---|---|
| Mount | The folder that contains the program | The program expects a specific drive letter |
| Cycles | The default or auto | The game is too fast or too slow |
| Output / shader | A simple sharp scale | You want a CRT-style look after the game already runs |
| MIDI / SoundFont | Default or a font you may use | Music is silent and the game uses General MIDI |
| CD image | Unset | The software asks for its disc |

Shaders and filters are cosmetic. Apply them after the program runs correctly. A black screen is rarely fixed by a shader, and a shader is an easy way to hide a working game behind a broken pipeline.

## First Launch

1. Put the DOS program in a normal folder path without exotic permissions.  
2. Mount that folder as a drive inside Staging.  
3. Switch to the drive and run the executable.  
4. If it is too fast, lower cycles and try again before you edit anything else.  
5. If music is missing, set MIDI only if the program is one that uses it.  
6. Save a per-game config so the next launch does not depend on the global default.  

Per-game configs are the difference between one title that works and a global setting that breaks the next title. Keep them beside the game folder.

[![Open DOSBox Staging](https://img.shields.io/badge/Open-DOSBox_Staging-166534?style=for-the-badge&logo=github&logoColor=white)](https://ericmsrushin.github.io/.github/dosbox-staging-shaders)

## Who It Fits

Players and hobbyists running DOS software that behaves under DOSBox's programming model. A poor fit for Windows 95 as a serious guest; that is a different emulator's project. A poor fit for software that needs a specific ISA card DOSBox does not emulate. A poor fit if the goal is a legal free pass to copies you do not own. Staging runs the files you already have the right to run.

## Requirements

| Item | Minimum | Recommended |
|---|---|---|
| OS | 64-bit Windows the release supports | Current Windows |
| CPU | Light for most DOS games | Headroom only if you raise cycles a lot |
| RAM | Modest | Modest |
| Disk | The programs plus configs | Per-game config files |
| GPU | Any; shaders are optional | A normal desktop GPU if you enable heavy shaders |

## Fixes

The executable is not found. You mounted the parent folder and the EXE is one directory down, or the mount failed because the path was wrong.  
The game races. Lower cycles. Do not install a "patch" you do not need.  
Music is silent. The game may use AdLib, Sound Blaster, or MIDI. Match that one choice; do not flip all audio settings.  
The window is a stripe or a blur. Disable the shader and use a simple output mode.  
A config from an old DOSBox build errors. Staging's syntax is stricter. Recreate the few lines you need instead of pasting a decade-old file.

## Per-Game Files

Keep each title's config next to its folder and name the file after the program. A global config that grew a shader, a high cycle count, and a MIDI font will eventually break a second game that was fine on defaults. When something fails, start that game from a clean config and add one setting back.

Mount paths should stay on a local disk with a stable letter. A folder that lives on a USB stick will work until the letter changes, and the error looks like a missing executable rather than a moved drive.

| Habit | Result |
|---|---|
| One config per game | The next title keeps working |
| Cycles changed last | You can undo speed without touching audio |
| Local mount path | The EXE is still there tomorrow |

![DOSBox Staging window with a mounted game directory](https://www.dosbox-staging.org/static/images/release-notes/0.81.0/gods.jpg)

## Lookup Terms

dosbox staging, dosbox staging shaders, dosbox staging windows, modern dosbox build, dosbox cycles too fast, dosbox staging config, dos midi soundfont, per game dosbox config
