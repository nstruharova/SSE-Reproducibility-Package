# SSE-Reproducibility-Package

This package contains an automated script to test power consumption of different applications from Microsoft 365 and LibreOffice with different file types. Originally this package was created for Project 1 for a course "Sustainable Software Engineering" offered by TU Delft EEMCS faculty.

The script is a shell script that runs on ZSH. The script was last successfully ran on macOS Monterey 12.2.1 with the use of an automated application made with Automator, where the script was embedded.

## What exactly does the script do
The script tests power consumption of three LibreOffice applications: Writer, Calc and Impress, and three Microsoft 365 applications: Word, Excel and PowerPoint.
Each of the six applications were given a file to open. The energy consumption of the application was then measured from the moment the file was open for a duration of 15 seconds. After these 15 seconds, the application was closed, which was followed by a 20 seconds long cool-down period of idle machine state. Then the next experiments of the same nature followed in the same fashion until all applications were tested with all the predetermined files. 

## Instructions for use
The script can either be ran from Terminal or embedded in an application that can be created on macOS using Automator. The latter is preferred, as Terminal can be closed during the script execution and thus we can minimise interference with other applications. To run the application, clone this repository, and the Automator application will be available in the directory you cloned it in.

For the script to run correctly, make sure to download the "Files" directory and change the path to your local "Files" directory copy in the script. It is also necessary to download the [Intel Power Gadget](https://www.intel.com/content/www/us/en/developer/articles/tool/power-gadget.html) measuring tool and put it in the Applications folder on your local macOS user. Also make sure to create an emptry directory called "Results" and make sure the path is provided in each command in the script.
