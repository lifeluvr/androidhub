#A.D.B.
###AN ANDROID DEBUGGING BRIDGE BREAKDOWN 
###By Eric Payne

ADB, by itself, is NOT a program or application. It's actually part of a much larger program, Android Studio. ADB is often included in many other applications that communicate directly with Android devices because of it's unique abilities. 
    
Technically, ADB is a binary file. The ADB binaries are a key part of every Android Operating System. Often referred to as the "Back End" in programming, it does the work that the "Front End" tells it to do. The "Front End" being the part of a program that user sees and interacts with. All programs must have a stable back end. Or else, the front end will not function properly. Make sense?

Since ADB doesn't have a GUI or front end, we're forced to use the terminal to access it's abilities but, to give your terminal these added ADB abilities your terminal MUST be open in the same directory or working folder that contains the ADB binaries! If you are not, your terminal will not know what ADB is and won’t know what to do with ADB commands! To do this we'll use the "cd" (change directory) command followed by the location of the ADB binaries:
     
````
~$ cd location/of/ADB/binaries
````

Another method is to use the file manager to open the location of the ADB binaries. After you're in the same folder, right-click on any empty spot and select "Open in terminal". 

If you've downloaded and unpacked Android Studio already, the ADB binaries are located in the _Android/android-studio/platform-tools_ folder. You can also find the ADB binaries online but, Android Studio's binaries are always current and up to date (If you update Android Studio).

![cd2platform-tools](/library/cd2platform-tools.png)

That's all it takes to make ADB commands recognizable while using the terminal! You can check by typing:

````
~$ adb
````

or plug your Android in with USB Debugging set to _ON_ and type:

````
~$ adb devices
````

_But_....

We don't want to bother with that every time we want to use ADB commands, right? 

If you open the file manager to the Linux root system files. There is a folder named "usr". Inside of that folder is another folder named "bin". In this case, "bin" is short for "Linux Root System’s User Binary Folder" but, who wants to type all of that, right? In the terminal you can get there by typing:

````
~$ cd  /usr/bin
````

![usrBin](/library/usrBin.png)

If you add the ADB binaries to that system binary location, your linux terminal will always have ADB abilities and, you won't have to bother with being in the same directory or folder with ADB! 

*IMPORTANT! It's best to NOT remove Android Studio's ADB binaries! Use "copy n' paste" and, make copies instead!* 

Let's use the "Front End" method, with root permissions, so we can watch all the action! Open up your terminal and type:

````
~$ sudo nautilus
````

Enter your password. When the file manager opens you'll need to navigate to the /usr/bin folder. Next, open a second file manager (root is optional) and go to the folder containing your downloaded ADB binaries. Now, copy n' paste the ADB binaries into the open /usr/bin folder and do the same thing with "Fastboot" while we're here. Exit all of your open windows.

![copyNpaste](/library/copyNpaste.png/)

You now have ADB binaries installed on BOTH your devices! Finally, your devices can communicate via ADB commands in the terminal!

That's it! You're all done and super-charged with awesome ADB and Fastboot powers! Any where you want!
