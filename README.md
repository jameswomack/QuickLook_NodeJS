# QuickLook Node.js

QuickLookNodeJS is a QuickLook plugin that lets you view plain text files, focused on NodeJS dev, without a file extension. Files like:

    README
    INSTALL
    coffee
    iced
    etc...

You can also customise the plugin to determine which files it previews. See [*Customizing white/black lists*](#customizing-whiteblack-lists---step-by-step), below.


## Installation


### Pre-compiled

* [Download the latest version of QuickLookNodeJS](
  https://github.com/downloads/whomwah/qlnodejs/QLNodeJS.qlgenerator.zip)
* Unzip 
* Copy the file into `/Library/QuickLook` or `~/Library/QuickLook` 
  (You can create the `QuickLook` folder if it doesn’t exist)


### Manually Compiled

Compliling the project yourself? Just copy the generated `QLNodeJS.qlgenerator` 
file into the relevant `QuickLook` folder (as above).



## Customizing white/black lists - Step by Step

Want to change the current behaviour?  Just follow the instructions below.  

**Note:** 
Plists used here are not same as user defaults, so you won’t find 
them in `~/Library/Preferences`. Instead, you need to edit the plist 
files inside the bundle—in this case, the plugin file: 
`QLNodeJS.qlgenerator`.


#### 1. Show the contents of the bundle.

If you installed the plugin, it should be in `~/Library/QuickLook/`.

<a href="http://a.yfrog.com/img740/933/tipb.png"><img src="http://a.yfrog.com/img740/933/tipb.png" width="300"/></a>


#### 2. Edit the appropriate plist file in your favorite text editor.

<a href="http://a.yfrog.com/img878/3563/hd9w.png"><img src="http://a.yfrog.com/img878/3563/hd9w.png" width="400"/></a>

Plist files:

* **`QLNodeJSWhiteList.plist`** : files with these names will **always** be previewed
* **`QLNodeJSExtensionsBlackList.plist`** : files with these extensions will **never** be previewed
* **`QLNodeJSDirectoriesBlackList.plist`** : files contained by these directories will **never** be previewed


## Trouble?

If you’ve installed the plugin, but don’t see any changes:

- Make sure you are editing (a) the correct plist of (b) the correct bundle. 
  (For example, you might have two `QLNodeJS` plugins. It’s possible the plugin in 
   another directory—perhaps `/Library/QuickLook/`—is what is being read.)
- Run `qlmanage -r` in the Terminal. (This will restart QuickLook, which reloads all plugins.)


## Authors

**Original author:** Duncan Robertson
**NodeJS defaults:** James Womack

Special thanks to the following people for submitting patches:

* [Guillermo Ignacio Enriquez Gutierrez](https://github.com/nacho4d)
* [Rob Lourens](https://github.com/roblourens)
* [Avi Flax](https://github.com/aviflax)
* [Tony] (https://github.com/Zearin)


## Contributing

* Fork the project
* Send a pull request
* Don’t change the build number (I’ll do that when I release a new version)
