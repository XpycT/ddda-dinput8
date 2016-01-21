# DDDASaveBackup
dinput8.dll hook for the game Dragon's Dogma: Dark Arisen, which backups saves.

## Features

### Save backups
Every time the game tries to create a save, the hook adds a timestamp to the file name.  
(instead of "ddda.sav" it's for example "ddda_2016-01-20_20-18-59.sav")

Then whenever the game tries to load a save, the hook redirects it to the one with the latest timestamp.  
-> When you need to revert to previous save, simply remove the new ones.

It also creates a log file (dinput8.log) in the main DDDA directory, which logs paths/names of handled saves.  
(-> so you can see where to find them) 

### Character customization screen
Allows you to enter the character customization screen at any time:  
1) go to the main menu (either the one with load game/options/etc or the one with main menu/manual/exit game)  
2) hold Home+End and press Enter

## Installation
Copy dinput8.dll into the main DDDA folder.

## Credits
MinHook - The Minimalistic x86/x64 API Hooking Library:
http://www.codeproject.com/Articles/44326/MinHook-The-Minimalistic-x-x-API-Hooking-Libra

JSON for Modern C++
http://nlohmann.github.io/json/

Idea for entering customization screen taken from:
http://forum.cheatengine.org/viewtopic.php?p=5641841&sid=74351ba2a0e31e335a5cb0b5cbf3105f#5641841