This is a collection of a few simple mods I have made. 
They all require [Melon Loader](https://melonwiki.xyz/#/README?id=installation-on-il2cpp-games) and [UIExpansionKit](https://github.com/knah/VRCMods/)

**USE IT AT YOUR OWN RISK. Modding the client is against VRChat's ToS. I am not responsible for any bans or any punishments you may get by using these mods**

**This was made in my free time, and is provided AS IS without warranty of any kind, express or implied. Any use is at your own risk and you accept all responsibility**


# VRC-NearClippingPlaneAdjuster
This is a mod for adjusting the near clipping plane for the player's camera. This can allow you to get much closer to objects before they start clipping and be used for seeing your limbs with a VERY small avatar. 

Note: This mod will not fix your menu breaking at small avatar sizes. However, the keyboard shortcut 'Ctrl + \\' works for setting you to the default avatar. 

This mod requires [Melon Loader](/https://melonwiki.xyz/#/README?id=installation-on-il2cpp-games) and [UIExpansionKit](https://github.com/knah/VRCMods/)

Once you install the mod you should see new options to the left of your Settings menu. 

![image](https://user-images.githubusercontent.com/68404726/107717860-34b56a80-6c9a-11eb-92e5-6915c8f0d9b8.png)

Very rarely using .0001 near plane distance will stop you from being able to interact with your menu, I have only ever seen this in a handful of worlds where the player location is far from the origin of the map. However .01 should always be safe to use as that is the normal minimum size Unity lets you use.  


VRChat will set this back to default every world change. This mod will set the near plane clipping distance to .01 15 seconds after you load into a world.  (Reason for the delay is that we can't know exactly when the world's referenceCamera's settings are copied onto the player's camera)

Now adjusts the clipping plane on your photo camera thanks to an addition by tylerhasman.

Now includes an option to adjust the Nearclipping Plane up to 0.05. This was suggested as a compatibility option for very large worlds where the Far Clipping Plane was getting pulled in too close by 0.01

There are now two preferences in Mod Settings, 
* Keyboard Shortcuts - Enables keyboard shortcuts to set your clipping plane to the smallest or largest values.  **[** for 0.001 and  **]** for 0.05
* Smaller Default - Sets a smaller value on World Change - 0.001 vs 0.01

# VRC-CameraResChanger
Another simple mod that does just one thing! This uses [UIExpansionKit](https://github.com/knah/V.RCMods/) to add a few buttons to your camera menu, allowing you to set the VRC camera resolution to, Default (1920x1080), 4K (3840x2160), 6k (5760x3240), 8k (7680x4320).

![image](https://user-images.githubusercontent.com/4786654/86955451-370c8080-c11d-11ea-8038-4b39c7c10979.png)

Couple notes: 
* Larger resolutions will cause your game to hang for a few seconds while it renders the image, I have not had VRC crash outright though, but in one instance an 8k photo took 30 seconds.  
* Thanks to [Lag Free Screenshots](https://github.com/knah/VRCMods#lag-free-screenshots) I was silly and added a 16k option if that mod is also installed.
  *  Note, make sure you have a good amount of RAM free. A friend of mine recently mentioned that he was having issues with this and I checked and a 16k photo spikes RAM usage by 6GB  
  * __Resolutions greater than 8k may randomly break with new VRC versions__
* This will not work with Virtual Lens, that camera has a lot of hard coded resolution values in it's shaders. Using anything but the default resolution will just result in a picture of you.??**VRCLens** will work with the 4k option though (if you set the camera prefab to use it when you add it to your avatar)

I would also recommend [CameraMinus](https://github.com/knah/VRCMods) for some other camera QoL. 

# VRC-RemoveChairs
Very simple mod which adds a Toggle Chairs button to the Worlds menu that will locally toggle all active chairs in a world. Useful for when map makers put chairs in inconvenient locations and don't have a way to disable them.

![image](https://user-images.githubusercontent.com/68404726/107717998-86f68b80-6c9a-11eb-9d30-53189e873661.png)

# VRC-LocalCamera
In the latest addition to look-at-yourself technology, this mod adds a pickable camera. This was made to replicate the functionality of turning the default camera around and pointing it at yourself, but to be local so others don't see the floating lens.

You should find a button on your UIX Quick Menu called 'Local Camera'

![image](https://user-images.githubusercontent.com/68404726/107718087-bf966500-6c9a-11eb-90bc-2c6efa02d591.png)

Features include:
  * Enable/Disable Pickup of Camera 
  * Change Camera Scale
    * Togglable 4k Render Texture Size (Not much of a reason to enable this)
  * Change Camera FoV (Zoom)
  * Lock Camera to your Tracking Space (like the normal VRC camera moves)
  * Selfie Stick for moving the camera
  * Rotate to your Head - Turns the Camera to face you
  
# VRC-DisableControllerOverlay
A simple and limited functionality mod. This simply disables the white outlined controller tooltips you get when hovering over an interactable item when Tool tips are enabled. 

Why make this? Because randomly that outline gets stuck on and the only way in the past to get rid of it was to restart the game, now I can just click a button. 

This has been tested with Index controllers, but should work with others, probably? 

![image](https://user-images.githubusercontent.com/68404726/107717602-a17c3500-6c99-11eb-8ae8-9f0fd4a42165.png)

# VRC-ImmobilizePlayerMod
An ultra simple mod, this puts a toggle on the UIX QuickMenu called "Immobilize" clicking will change the Immobilize value on your VRCPlayer to True or False. **Immobilize being True should have the same behavior as opening a big menu like Settings.** 
This will stop your body from spinning while laying down in non FBT with SDK2 avatars, with SDK3 avatars Immobilize breaks the current animation and roots your feet to the ground from my experience. 

In mod settings there are two preferences, where you can toggle having the "Immobilize" button on your quick menu, ~~and delay it's load so it is the last button on the menu.~~

# VRC-TeleportCameraToYou
Another ultra simple mod, this puts a button on the UIX _Camera_ QuickMenu that teleports the Viewfinder of your camera right in front of your face. This is useful if you left it somewhere far away, or are using a small avatar. 

In mod settings there is one preference, the distance from your head the camera gets teleported to. 

# VRC-ToggleIKTAnim
Did you like having a button you could pin to your QuickMenu to quickly toggle movement animations with IKTweaks? This ultra simple mod adds a toggle to your QM that forcefully sets the preference for IgnoreAnimationsMode betweek "None" and "All".    
It is simple, dirty, but works! 

# VRC-LocalCube
Did you ever just not want to see the rest of the world? This mod gives you that ability! Now you can spawn a cube around you that only you can see!   

The silly inspiration for this mod was VRC reconnecting me to a world while I was sleeping, the sleep area is dark, but spawn is super bright. Obvious answer is to make a mod to make a black cube to hide the blinding light! 

Also has been useful at times for just using a wall from the cube to hide certain parts of the map when they bug out. Don't need to worry about the seizure textures if you just hide them! 

# VRC-MirrorLayers
Requires [UIX](https://github.com/knah/VRCMods/releases/latest/download/UIExpansionKit.dll) for it's menus  
  
This mods allows you to edit the layers that mirrors reflect in VRChat
You can: Set all Mirrors to Full/Optimized   
Enable/Disable layers on all mirrors or a specific mirror using the "View Mirrors" button.  

Includes the option to force setting a default layer mask to all mirrors on joining the world, accessible in the "Defaults Menu"
  
You can access these options using the "Edit Mirror Layers" buttons in the Worlds Big Menu, and Quick Menu. (Quick Menu button is disabled by default, you can enable it in Mod Settings)  

# VRC-PlayerSpeedAdjSlower
Did you ever want to move slower in game? This mod lets you do that! This is a very simple mod that uses [UIExpansionKit](https://github.com/knah/VRCMods/) to add three buttons to your settings menu. Default Speed, Half speed and 1/10 speed. 
Honestly the main purpose for making this was use with very small avatars. 

![image](https://user-images.githubusercontent.com/68404726/107718127-d341cb80-6c9a-11eb-8250-4c2f142b09f4.png)

Count it as either a bug or a feature, but this does not affect the strafe speed, so you still can move side to side at full speed. 

After pressing the button it will set the speed every 30 seconds for 5 minutes, to allow you to switch avatars and keep the set speed.

VRC_Player-crasher will pop up a menu you have to open while in game so it pulls up all the other players in the lobby you are in
it will show you other users account stats-friendslist and the ability to crash them *Disclaimer* USE AT YOUR OWN RISK you can get banned for crashing players

