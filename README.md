# Blank Text File.app + Terminal Here.app
An group of AppleScript application(s) that allows FAST creation of a text file in the current finder window and QUICKLY open a Terminal window in the current Finder directory.

<img width="842" alt="image" src="https://github.com/user-attachments/assets/a7e1442d-51ff-4505-8b0a-2189e0cd53d6" />

___

## HOW TO USE:

1. Download the pre-built application from:
-- > https://github.com/jamubc/finder_quick_actions/archive/refs/heads/main.zip
   
3. Unzip the downloaded BlankTextFile.app/OpenTerminalHere.app.

4. Open a new finder window and go to the exctracted files.
5. while holding the `Command (⌘) + Option (⌥)',` Drag either app `(BlankTextFile.app/OpenTerminalHere.app)` to the Finder's toolbar.

6. It should work now when clicked!

**Note:** This tool requires a Finder window to be open and displaying a folder.

## Building from Source

If you want to build the application yourself:

* Blank Text File.app *
```
tell application "Finder" to make new file at (the target of the front window) as alias
```
* Terminal Here.app *
```
tell application "Finder"
    set posixPath to POSIX path of (target of front window as alias)
end tell

tell application "Terminal"
    do script "cd " & quoted form of posixPath
    activate
end tell
```

1. Create a new automation type Application in Applications.
2. Add a "run Applescript" node to the new Application.
3. Enter the code above or write your own.
4. Save it.
5. Refer to --> HOW TO USE above.

The icons come from "https://fonts.google.com/icons", If you dont like green you can easially change the colors by downloading an icon in a color, copying it. Going to the .app we just made or you just unzipped, right click it, click get info, click the icon to make it "glow", press delete, then `paste` the image in your clipboard to set it as the new icon.



