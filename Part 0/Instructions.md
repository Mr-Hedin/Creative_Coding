# Welcome to Pygame
### In order to get started, you will need to complete some *absolutely* necessary steps.
1. Create a folder to store your game. If you've downloaded this file, this step is hopefully complete!
2. Create a 'virtual environment' folder. This guy just holds all of your libraries and Python related nonsense so you don't have to worry about where those things go. To do this, open a new terminal (if you're using VS Code that's up at the top under 'Terminal)
#### Type the following in your terminal:
```bash
python -m venv .venv
```
#### This command tells `python` to use the `-m` or module command to run the module `venv` which just stands for virtual environment, the last part `.venv` is the name of the folder you're using as your virtual environment. 
#### This is actually an important part of nearly all python projects, your virtual environment holds onto the libraries/modules and external code you need to make your project run.
#### Once you've got that venv set up, you need to tell Python to use it. 
Type this in your terminal if you're on windows:
```bash
source .venv/Scripts/activate
``` 
or if you're using Linux:
```bash
source .venv/bin/activate
```
3. Next, install the Pygame module. Pygame itself is no longer updated since the developers have moved on. However, pygame-ce (community edition) is updated and maintained by a loving community of random Python devs! To install pygame, use your terminal from before and type the following:
```bash
pip install pygame-ce
```
#### This command tells `pip`, the python package manager, to pull the pygame module from the internet and install it in your venv. Package managers are amazing. They take care of all of the dirty work of dealing with external code - makes it super simple to install just about any Python module someone has written and made available! 
### *As a side note, always be careful when you install a Python package, hackers have started to upload fake Python libraries to catch newbies and experienced devs alike.* 
- Ensure you've spelled the package name correctly, and double check that the package contains safe code. You can often trust the community to vet popular packages so don't stress if you're installing something simple like `pandas` but be a little wary if you're installing something you haven't looked through like `firefox-installer-v6-special-edition-nohack-pinkypromise`... 
4. After you've got your folder and virtual environment with Pygame installed, and you've activated your venv, you're ready to roll. Create a new file called `main.py`. If you've never made a new Python file, simply click `File` then `New Text File` and save it as `main.py`
-  Python files are basically just plain text that gets hucked into something called the 'interpreter' that makes the code run.
5. In `main.py` type the following to get pygame into your project:
```python
import pygame
```
6. There are only a couple more things to write before you'll have a running 'game'. It won't do anything. But we're almost there. How exciting. Let's set up our window dimensions and tell pygame to get ready:
```python
import pygame

WINDOW_HEIGHT = 720
WINDOW_WIDTH = 1280
pygame.init()
screen = pygame.display.set_mode((WINDOW_WIDTH, WINDOW_HEIGHT))
```
7. Finally, we can set up a main loop for our game. This is where all of your final magic will live. We'll set up a `running` variable to tell the program when the game should be running or not, then check for any `events` coming from the pygame module. Type this:
```python
import pygame

WINDOW_HEIGHT = 720
WINDOW_WIDTH = 1280
pygame.init()
screen = pygame.display.set_mode((WINDOW_WIDTH, WINDOW_HEIGHT))

running = True

while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
    # Start doing some rad game code here
pygame.quit()
```

### That's it. 

### To run your incredible work of art type this in your terminal:

```bash
python main.py
```

#### You can start digging in and creating whatever insane nonsense your heart desires. Check out the documentation at https://pyga.me/docs/ for some examples and all of the commands you have access to.

#### There's a wealth of resources available on Youtube, Stack Overflow, and so many other places. Don't be afraid to make something that's terrible. Don't be afraid to ask questions. Good luck out there.