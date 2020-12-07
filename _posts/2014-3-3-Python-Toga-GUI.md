---
layout: post
title: Python GUI programming with toga
---
# Toga
![Toga](https://beeware.org/project/projects/libraries/toga/toga.png)


Toga is a Python native, OS native, cross platform GUI toolkit. Toga consists of a library of base components with a shared interface to simplify platform-agnostic GUI development.

Toga is available on Mac OS, Windows, Linux (GTK), and mobile platforms such as Android and iOS.
![](https://toga.readthedocs.io/en/latest/_images/tutorial-2.png)

## Installation
### for linux
```bash
# Ubuntu, Debian 9
sudo apt-get update
sudo apt-get install python3-dev libgirepository1.0-dev libcairo2-dev libpango1.0-dev libwebkitgtk-3.0-0 gir1.2-webkit-3.0

# Debian 10
# has webkit2-4.0
# libwebkitgtk version seems very specific, but that is what it currently is @ 20190825
sudo apt-get update
sudo apt-get install python3-dev libgirepository1.0-dev libcairo2-dev libpango1.0-dev libwebkit2gtk-4.0-37 gir1.2-webkit2-4.0

# Fedora
sudo dnf install pkg-config python3-devel gobject-introspection-devel cairo-devel cairo-gobject-devel pango-devel webkitgtk3

# Then, for all linux flavors
pip install --pre toga
```
### for MacOS and Windows
```bash
pip install --pre toga
```
## Start...
run following code on python console.
```python
import toga # imports toga

def button_handler(widget):
    print("hello")

def build(app):
    box = toga.Box() # Create Box Widget
    button = toga.Button('Hello world', on_press=button_handler)
    # Create Button Widget with some text, and adds a event handler for click event
    button.style.padding = 50 # set padding for Button
    button.style.flex = 1 # set flex for Button
    box.add(button) # add Button to Box
    return box # return Box

app = toga.App('First App', 'org.beeware.helloworld', startup=build) # create Toga app
# First app is the name of your app
# this reversed domain name is your app id
# startup is a handler for add widgets to main window
app.main_loop() # run Toga App
```
![](https://toga.readthedocs.io/en/latest/_images/tutorial-0.png)
**It's a Toga GUI:smile::smile::smile:**
### Good Bye until next time...
