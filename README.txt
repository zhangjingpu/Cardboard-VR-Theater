Main Controller:
Contains a public Array of strings.
This array is sopposed to be filled with a list of youtube URLs.

The default resolution is the resolution in which the video will be loaded. The code that handle the resolution is provided by Youtube Player asset.


The child Objects are the bottuns on the side. To add A new button, write it's function inside the Function Method thats inside the ButtonFunction Script, adding a bool, then checking it on the inspector (!!Remenber to only have on checked for prefab and add the script to the new button!!).
Each button has it's own highlighted color, Ajust it by setting the ColorOfHighlightedButton variable in ispector.
Turn on and off the highlight color function by the checkbox ChangeColorOnHighlight.


The "Cube" prefab, grandson of YoutubeVideoPlayer_Mobile, is the Collider that detects if the gaze is on the screen.
i.e. making it the same size of as it's father prefab will make it only pause when the eye gaze ray, origin in "Right Eye" Camera and direction forward of the gaze, goes out of the screen.


SkyBlockSphere is the inverted sphere that represent the room as skyblock.


The "Right Eye" camera contains the gaze ray.
The TimeBeteweenIterations controls the time beteween each check if the raycast has hit a button. This check only occurs when the buttons are visible.
The TimerToCallButton maneges for how long is needed to look at the button before it's function is called.
The script TiltController has the variable TiltAngle, which controls the angle needed to reset the z axis to 0.(!Not recomended bellow 10, since it may cause misscalls of the Recenter method!)



The volume cannot be controled by standard methods( AudioListener.volume or AudioSource.volume) because of the way easy movie texture handles sound.


So brightness and volume will need to be added via external android coding.
