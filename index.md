---
layout: default
---

Welcome to my GitHub pages portfolio, here you will find a summary of some of my open source programming projects.

# [](#header-1)Who am I?

My name is Jeremy Wade (pseudonym uniflare), an enthusiastic coder from the UK that loves creating and fixing things - nothing brings me more happiness than helping someone smile. 
I started writing html after I got interested in the source code behind my favourite websites, at the time these related to the "Delta Force" series of games back from 2000 (being 11 at the time). 
PHP naturally followed this interest in website programming and I was hooked. Eventually writing applications in several other languages to solve problems I had or to make mine or someone else' life easier - usually small projects, solo. 
It was always 'Just a hobby', something in my down-time, something to relax with or get stuck into, something I could solve problems with, make a difference to someone - or myself.
 
Fast forward around 16 years, I get an interest in C++ programming (I always wanted to learn C or C++ but it was a 'mystical' language to me back then dealing with compilers etc - PHP just worked for me). 
I make the decision to finally learn C++ (the 'ultimate' language - my thoughts at the time). Wrote some simple snippets, experimented, just played around... then comes CRYENGINE, I heard people say it is the most difficult engine to master, that the code is hard to understand.
Perfect! CRYENGINE - the most visually stunning and ground breaking engine from the Crysis series - time to see what the fuss is about!

I have become more and more of a regular CRYENGINE  community member for the better part of a year now and I am thoroughly enjoying my time.

* * *

### [](#header-3)CRYENGINE V - Splash Screen Plugin
![Splash Screen Plugin for CRYENGINE 5.3](/assets/images/splashplugin.jpg)
<span id="langtag">CMake</span><span id="langtag">C++</span><br/>
[GitHub Repository](https://github.com/uniflare/SplashExample)<br />~~[CRYENGINE Marketplace](https://www.cryengine.com/marketplace/product/splash-screen-example-plugin)~~ (Unavailable due forum account bugs, back soon)<br/>

#### Goals
- Provide a simple Splash plugin with an expanded feature-set relative to the built-in splash screen routine.

#### Requirements
- Simple (Drag & drop/Easy as possible)
- Compatible (Between templates/projects in the supported engine versions)
- Maintainable (Well documented code)
- Robust

#### Issues
The wide compatibility requirement did present some issues, the biggest of which involved the default profile that the GameSDK Project uses. 
To work around the issues, I had to implement my own method of detecting whether the current profile is indeed the default profile.

The most successful & effective method that I found was to store a special attribute in the player profile. Since the splash plugin is supposed 
to be loaded on the very first run, it should have primary access to the profile management system. e.g.
```cpp
if (!m_pCurrentProfile->GetAttribute("SplashFlag_FirstRun", bSplashFlag, false))
{
	...
}
```
I decided the risk of having this plugin added during an already released game and a user that set the lowest supported resolution was adequately low.
A positive side-effect of this implementation appears to 'Fix' the initial default GameSDK Profile management code that deals with the user resolution settings.

#### tl'dr
 - Compatible with GameZero & GameSDK + Project templates (5.3).
 - Plug n Play - minimal setup required.
 - Well documented source code and revision history.
 - Modified to meet end-user feedback (pre-splash was a suggestion).

* * *

### [](#header-3)CMakeGen
![CMakeLists.txt Generator](/assets/images/cmakegen.jpg)
<span id="langtag">CMake</span><span id="langtag">C++</span><br/>
[GitHub Repository](https://github.com/uniflare/CMakeGen)<br/>

#### Goals
- To provide a simple yet effective CMakeLists.txt generator based on the source root folder/file structure.

#### Requirements
- Drag & Drop (Project Source Root)
- Double-click (Look for "Code" sub folder)
- Adaptable (Generates a modifiable Root CMakelists Template file)
- Maintainable
- Robust

* * *

### [](#header-3)Arma 2/3 - Server Keepalive Batch Tools
![Server Keepalive Batch Tools](/assets/images/skbt.jpg)
<span id="langtag">BatchFile</span><span id="langtag">C#</span><br/>
[GitHub Repository](https://github.com/uniflare/skbtforarma)<br/>

#### Goals
 - Initially to provide administration relief and improve the admins QOL regarding a dedicated Arma 2 server by:
	- OneClick (or DoubleClick) Start/Stop/Restart of a server instance
	- Easy server version synchronisation
	- Auto restart on crash/exit
	- Realtime logging/continuous console output for monitoring
	- Integration with the server (start/stop/restart routines)
	- Manual control via provided start/stop/restart etc batch files.
	- Easy integration with a web browser based administration system.
	
 - Expanded to create a more modular system over time by:
	- Creating a C# install manager that can handle multiple installations on the same machine.
	- The new application can also control the batch script via provided batch files you can execute.
	- Making the system open-source on GitHub
	- Adapted to Arma 3 from Arma 2
 
#### Requirements
- Easy installation management (Installer created for this purpose)
- Easy to configure and use
- Core system entirely in BatchFile (Requirement from current admins)
- Modular (Batch can be difficult to keep organized, common routines were separated into their own files)

#### Issues
The biggest issues were the batch scripting itself, learning the intricacies of windows Batch File (or.. 'Modern DOS') was an interesting experience.
Definitely not recommended to use batch for this kind of advanced functionality but it works.
 
* * *

### [](#header-3)Contribution - CE Tools
<span id="langtag">Python</span><br/>
[GitHub Repository](https://github.com/patsytau/ce_tools)<br/>

#### Purpose of script
To provide an easy alternative for new CE developers to quickly package a development build of their game to pass to users without, for example, the engine, or launcher to run and test the game.

#### Purpose of contribution
- To fix incompatibility with new CE Versions
- To maximise compatibility (Newer & Older CE Versions)

* * *

### [](#header-3)Activity - CRYENGINE Forums
[Getting Started with CE guides](https://forum.cryengine.com/viewtopic.php?f=11&t=66)<br />
[Forum Profile](https://forum.cryengine.com/memberlist.php?mode=viewprofile&u=83036)
