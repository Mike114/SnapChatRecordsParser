# SnapChatRecordsParser

SNAP CHAT GEOLOCATION TOOLS

There are two SnapChat parser tools.  They both do the basically the same thing, but the command line version has more options and can be used by third party scripting tools.  This tool is based on the current SnapChat location return format and if SnapChat changes the format, the tool will break.  After the tool processes the SnapChat locations, a KML file is created.  This file can be dragged into Google Earth and the locations can be viewed.  The KML file has a timeline function built in, so if you are not seeing any data points in Google Earth check the timeline slider and expand it accordingly.    


SnapChatRecordsParser – GUI.exe
 
This is the easiest was to run it.  Double click the exe file and then enter the name of the SnapChat PDF file when prompted.  The filename and extension must be correctly typed.  The file obtained from SnapChat needs to be in the same folder as the SnapChat parsing tool.  The file names from SnapChat are often long, so just rename the file to something easy to type.  For example, rename dru.reyes31_1675365883455.pdf to 1.pdf and then type 1.pdf into the prompt (kind of hard to misspell 1.pdf).  The filename can also be cut and pasted into the prompt, just make sure the file path is not included.  

The GUI version will output (2) separate KML files.  One has all of the locations and the radius of those locations plotted.  The second has the word “common” in the file name and plots the locations based on the frequency of times a particular location occurs in the records.  The GUI version will plot the top (100) frequent locations.  

SnapChatRecordsParser.exe
 
This is the command line version of the tool.  Double clicking it will do nothing as it must be run from the command line.  If you know how to use the command line the syntax is as follows:

SnapChatRecordsParser-CLI.exe [-h] -i INFILE [-o OUTFILE] [-t] [-c] [-r] [-V] [-q | -v]

SnapChat Records Parser Options

Options:
  -h,	 --help            show this help message and exit
  -i ,	--infile            The SnapChat File to be processed
  -o 	--outfile         The name of the output file. File extension not needed
  -t, 	--timeline      Utilizes the timeline feature in Google Earth
  -c, 	--count           Plots the frequency of locations. Good for determining common locations
  -r, 	--radius          Plots the radius of a point
  -V, 	--version       show program's version number and exit
  -q, 	--quiet           Does not print progress updates or stats
  -v, 	--verbose      Prints processing messaging


Examples:
SnapChatRecordsParser-CLI.exe –i 1.pdf –o BadguyLocations –t –c –r 
This will process the pdf names 1.pdf and name the output files BadguyLocations.  It will include a timeline, common locations, and plot the radius of the points.


SnapChatRecordsParser-CLI.exe –i 1.pdf
This will process the pdf named 1.pdf and output only the points to the default output file name.

Additional
The –t, -c, and the –r can be used in any combination and the results will vary depending on the one used.

The –o option allows you to name the outfile.  If not used there is a default outfile name.

The –q is a good option when using a third party or scripting the executable and no processing data is needed. 

The –v option can be good for debugging when things to not work correctly.  




