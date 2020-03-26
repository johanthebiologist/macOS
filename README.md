# macOS
Settings for new macOS accounts

**JalView**

`defaults write -g CGFontRenderingFontSmoothingDisabled -bool NO` to make texts MUCH easier to read (and smooth font makes the program very laggy). - http://www.jalview.org/Fuzzy-fonts-in-the-alignment-view-on-OSX-Mojave-1014x

**Edit creation date of files**

`touch -t "201501312214.33" FILENAME.PNG` ([1](https://smallbusiness.chron.com/change-file-date-mac-finder-46835.html), [2](https://hackernoon.com/how-to-change-a-file-s-last-modified-and-creation-dates-on-mac-os-x-494f8f76cdf4), [3](https://gmelikov.com/2016/12/19/change-a-files-last-modified-and-creation-dates-on-mac-os-x-and-linux/), [4](https://forums.macrumors.com/threads/touch-wont-change-file-creation-date-why.1969185/)).

**Create README file in current folder**
In Automator, create a new application, drag "Run Applescript" over to the right panel. and insert following code

`tell application "Finder"
    set txt to make new file at (the target of the front window) as alias with properties {name:"README.txt"}
    select txt
end tell`
