# Setup

<!-- MarkdownTOC autolink='true' -->

- [Folder](#folder)
- [Blender](#blender)
- [.inf File](#inf-file)
- [Zip-Snapshot 01](#zip-snapshot-01)

<!-- /MarkdownTOC -->


> On Windows, some problems with file permissions might occur if your Re-Volt folder is in the _Program Files_ folder (`C:\Program Files\Acclaim Entertainment\Re-Volt\`). Sometimes it is **better to move your Re-Volt folder to your Desktop** or your user folder.

## Folder
Create a new folder within `...\Re-Volt\levels` with the name of your track (keep it lowercase and rather short). In our example, we'll call it `testtrack`.

An example for the full path:

`C:\Program Files\Acclaim Entertainment\Re-Volt\levels\testtrack` or `C:\Users\YourName\Desktop\Re-Volt\levels\testtrack`

Examples for track names are `track_name`, `track_name01`, `track1name`, ...  
It's best to use lowercase letters, underscores and letters.

## Blender
Open Blender and save the empty Blender file with **CTRL S** to the directory that you created for the track. Call it according to your project, for example `testtrack.blend`.

## .inf File
The .inf file defines parameters for the game so it can see and read the track. Feel free to copy the file below and use it as a template. If you want to disable certain features (like MUSIC), put a semicolon in front of it (this will deactivate the line). Create an empty text file in your track folder and rename it to your track folder name, e.g. testtrack.inf. You will be prompted if you really want to rename it. Click yes.

Copy the following file and customize it to fit your track (you can leave most of the things as they are right now).

> TODO: Sample track.inf

```
;--------------------------
;Revolt .INF file structure
;--------------------------

NAME                   'Test Track'                   	  ;The name of the level as seen in-game
STARTPOS               0 0 0                              ;Start position of the car (x, y, z)
STARTPOSREV            0 0 0                              ;Start position of the car in reverse mode
STARTROT               0                                  ;Start rotation of the car (0 - 1)
STARTROTREV            0                                  ;Start rotation of the car in reverse mode (0 - 1)
FARCLIP                34000                              ;Far clipping distance (draw distance)
FOGSTART               33000                              ;Fog start (slightly less than FARCLIP)
FOGCOLOR               0 0 0                              ;Fog and background color (RGB)
VERTFOGSTART           0                                  ;Vertical fog start (as in rooftops)
VERTFOGEND             0                                  ;Vertical fog end (as in rooftops)
WORLDRGBPER            100                                ;RGB percent of original world gouraud (0 is dark)
MODELRGBPER            100                                ;RGB percent of original model (cars, etc.) gouraud
INSTANCERGBPER         80                                 ;RGB percent of original instance (decorations, etc.) gouraud
MIRRORS                0 0.75 0 256                       ;Type - mix - intensity start - distance
MUSIC                  'levels\testtrack\testtrack.mp3'   ;supported formats are mp3, ogg and wav
REDBOOK                4 9                                ;Redbook soundtrack if redbook folder is present. Two values, first and last track.
ENVROLL                'levels\testtrack\envroll.bmp'     ;Reflection on cars
ENVSTILL               'levels\testtrack\envstill.bmp'    ;Reflection on stationary objects and the ball bearing weapon
SHADOWBOX              -96                                ;Changes the contrast/brightness or the shadows on the track, default -96.
ROCK                   0 0 0 0                            ;Rocking effect like on Toytanic.
```

Check the [RVGL Documentation](https://yethiel.gitlab.io/RVDocs/#for-track-makers) for more options.

So far, we:
1. installed Blender
2. installed the addon and activated it
3. created a level folder for our track
4. saved an empty .blend file
5. created an .inf file so the track gets recognized by the game

## Zip-Snapshot 01
If you're unsure, you can download my level folder:

[Download Zip File](track_snapshot01.zip)