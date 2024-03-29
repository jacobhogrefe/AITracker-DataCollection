# AITracker Data Collection Application

## What is this?
This is the data collection application for our neural network AITracker. The application takes pictures of the user looking in specific directions, in a format that is exactly what our neural network will see in the main application.

## How to run as a user

### Download Application

1. Go to the releases section on GitHub.
	* ![](md_images/releases.jpg)
2. Select the download for your operating system (the first .zip file is for macOS, and the second is for Windows).
	* ![](md_images/downloads.jpg)

### Windows
1. Once the zip has been downloaded, make sure it is on your desktop and double click the zip file.
2. You should see a folder with a similar name as the zip file, then open the folder.
3. Run the file named "AITracker-DataCollection.exe"

### MacOS
Since macOS is a little troublesome to get an application running that's not signed (which is $99 a year!), we're going to have to do a little bit of work to get everything to work in properly.

1. Once the zip has been downloaded, make sure it is on your desktop and double click the zip file. 
	* ![](md_images/zip.jpg)
3. Now you should see a folder with the same name as the zip file. 
	* ![](md_images/folder.jpg)
4. Right click on the folder, go down to "Services >", and click "New Terminal at folder." (mine looks a little different) 
	* ![](md_images/services.png)
5. Next, type in the following command `bash quarantine.sh` and hit enter. 
	* ![](md_images/script.png)
6. Once the script has finished running, go into the folder and double click on the file named "AITracker-DataCollection" and the app should start up! Please be patient as the app does take some time to load in.
	* ![](md_images/executable.png)

Explanation on what the `quarantine.sh` script does: 

When a file is downloaded from the internet, macOS automatically applies a flag named "quarantine" to it, ensuring that it has the proper permissions to run, and essentially acts as a firewall to prevent malicious apps from running that aren't signed. What the script does is remove this quarantine flag, allowing the app to run normally, without having to pay Apple $99 a year to "sign" our app to verify it can be run on Macs. This script ONLY modifies this flag for files in this project, meaning that this won't affect any of your other files. In addition, the script will automatically delete itself once it has finished running.

## How to run as a developer
#### Ensure you have Python installed (this project was built in Python 3.11).

Make a virtual environment: `python3.11 -m venv env`

Activate the virtual environment: `source env/bin/activate`

Install required packages: `pip3 install -r requirements.txt`

Run the script using: `python3.11 AITracker-DataCollection.py`