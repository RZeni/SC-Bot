# SC-Bot
A Starcraft Brood War Competition Bot

# Downloading and installing:

1. If you haven't got it already, install SC:BW and update it to version 1.16.1.

2. Download the latest version of the BroodWar Application Programming Interface (BWAPI) (as of writing the latest version is BWAPI 4.1.1 Beta) from here, and install it. You will also need ChaosLauncher, but that should come with BWAPI when you install it.

3. Download the latest version of Visual Studio C++. I downloaded Visual Studio Community 2013 from here but other versions might work too. VS always comes with a million extra things, and you can probably untick some of the boxes if you don't want it all; as long as you get the C++ stuff.

# Compiling and running the Example AI

1. Go to the directory you installed BWAPI. Inside there should be a folder called ExampleAIModule. Inside this there should be a VC++ Project file called ExampleAIModule.vcxproj; open this in Visual Studio. Note: ExampleAIModule; NOT ExampleAIClient or ExampleTournamentModule.

2. Once Visual Studio has loaded, find solution configuration and change it from 'Debug' to 'Release'.

3. In the Solution Explorer window, right click on ExampleAIModule and click 'Build'.

Note: if step 3 fails to build because you get a compiler version error, then get the vs 2013 SDK and change your toolkit to vs 2013

4. Go back to your BWAPI directory (up one level from the ExampleAIModule folder) and find the folder named 'Release'. Inside you should find a file named ExampleAIModule.dll; copy this file. Note: compiling will also create another folder called Release inside the ExampleAIModule folder; this is the wrong folder; you won't find the dll file here. Look inside the Release folder in your BWAPI directory instead.

5. Find where you have StarCraft installed. Inside this directory you hopefully have a folder called bwapi-data, inside this is another folder called AI. Go to Starcraft/bwapi-data/AI/ and paste the newly created ExampleAIModule.dll inside.
Note: I suppose if these folders aren't there, you can probably create them.

6. Now you need to run ChaosLauncher. Go back to your BWAPI directory. Inside, there should be a folder called ChaosLauncher; inside this should be ChaosLauncher.exe. Make sure to right click and run this as Administrator or you might get some stupid error message.

7. In ChaosLauncher, make sure 'BWAPI Injector (1.16.1) RELEASE' is ticked and W_Mode is clicked.

8. Select the 'BWAPI Injector (1.16.1) RELEASE' option and click on the button that says 'Config'; this should open a text file. Near the top of the text file should be a line that says "ai = bwapi-data/AI/ExampleAIModule.dll". If ai is = to something other than "bwapi-data/AI/ExampleAIModule.dll" then the AI won't run; so make sure it's typed in correctly (but it should be there by default). You can now close Config.

