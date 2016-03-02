# HydroGeoSphere Language Grammar

This repository contains the necessary files for codehighlighting of [HydroGeoSphere][hgs] input files ("grok files"): The definition of the syntax of such input files, and the definition of which syntax to show in what coloring options. 

There are various options for text editors that understand this setup, it is tested using [TextMate][TM] on OSX and [Sublimetext][ST] (versions for various flavours of operating systems exist). Other text editors that understand `tmLanguage` syntax specifications exist.



This repository contains "compiled" version of the necessary files that need to be put into proper folders (see Section "Installation"). This repository contains also the [syntax definition as ASCII file][syntax_def_ascii].

Please contact me with questions related to the syntax or suggestions for improvements.

## Installation

### TextMate

The installation for TextMate is straight forward:

1. download the [hgs.tmbundle][hgs.tmbundle]
2. double click and follow the instructions

### SublimeText 
Two files need to be copied at two different locations. The destinations vary, depending on which version of SublimeText you use

#### Syntax Definition
This is where you will copy a zipped version of the language syntax

_OSX_:

- version 2: go to `/Applications/Sublime\ Text.app/Contents/MacOS/Packages`
- version 3: go to `Sublie Text` - `Preferences` - `Browse Packages`

_WINDOWS_:




Then, the procedure to get to the zipped version is described by [this post on stackoverflow][ST3_zip]:

1. Put the myLang.tmLanguage file into a folder with your desired syntax name.
2. Zip the folder so that it's named myLang.zip
3. Rename the zip archive to myLang.sublime-package
4. Put the myLang.sublime-package into the Sublime 3 packages folder. It will now appear in the sublime syntax highlighting menu.


#### Color Scheme

- copy the [Sublimetext color scheme][ST_color_scheme] to one of the two paths described above
- go to `Sublie Text` - `Preferences` - `Settings - User`; a file will pop up where you can specity the color scheme you want to use, in this case refer to the one you just copied by its file name. Typically, this could look like this:

    // Settings in here override those in "Default/Preferences.sublime-settings",
    // and are overridden in turn by file type specific settings.
    {
    	"color_scheme": "Packages/Color Scheme - hgs/hgs.tmTheme"
    }

NOTE: the file ending of the package is not demanded here (no `sublime-package`)!


## 2. Color Schemes
Color schemes can be viewed, modified, and created using [this][online_themes] online theme editor





[hgs]: http://www.aquanty.com/hydrogeosphere/
[TM]: http://macromates.com/
[ST]: http://www.sublimetext.com
[online_themes]: http://tmtheme-editor.herokuapp.com
[ST3_zip]:http://stackoverflow.com/questions/20385550/syntax-highlight-tmlanguage-in-sublime-text-3-for-packages/29566977#29566977
[syntax_def_ascii]: tm_hgs_language.grammar
[hgs.tmbundle]: 
[ST_color_scheme]: "Color Scheme - hgs.sublime-package"
[ST_syntax]: hgs.sublime-package