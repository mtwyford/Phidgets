# Phidgets for Geany
Tutorial Support for Running Phidgets on MAC and PC's from Geany/Command Line

There are several reasons for testing and troubleshooting running Phidgets from the terminal or simpler editors, 
However - I think there is much to be learned from learning to troubleshoot and breakfix.
Some are permission related, some are Java Version related, and one was even a machine permisssion issue.

#MAC
Go through the Tutorials to Configure your Phidget for MAC or Windows OS
Download and Unzip the folder to the Destkop
(may require installation/setup with the new USB interface)
Create a new folder in your usual projects folder called Phidgets
Copy the Jav file from the Phidgets download to the new folder
Create a new File, GettingStarted.java in the same foler
Copy the code from the Phidgets web site and replace/paste into the GettingStarted.java file

##Open Geany
Select Build -> Set Build Commands from the Menu Bar at the Top of the Screen

##Create new Custom actions for Compile and Run (Build)
Enter as follows:

COMPILE:
	javac -cp phidget22.jar "%f"

RUN:
	java -cp ".:phidget22.jar" "%e.java" 




#Windows
Follow similar steps, as above

## Copy both DLL files from the x64 folder into your pridgets project folder
##Create new Custom actions for Compile and Run (Build)
Enter as follows:
###COMPILE:
	
## javac -cp phidget22.jar "%f"

### RUN: ** NOTE THIS IS DIFFERENT IN WIONDOWS V MAC**
        ** Note classpath is typed out and it's a semi colon instead of a colon
## java -classpath ".;phidget22.jar" "%e.java" 

  
