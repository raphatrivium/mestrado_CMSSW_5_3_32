# mestrado_CMSSW_5_3_32

-Creating the folder of the CMSSW release
$ cmsrel CMSSS_5_3_32

-Go to de folder src within
$ cd CMSSW_5_3_32/src/

-Enter in the CMS environment 
$ cmsenv

-Create a folder (here named "CMSOpenDataAnalysis") enter it
$ mkdir CMSOpenDataAnalysis
$ cd CMSOpenDataAnalysis

Now, create the structure of analysis (here named "JpsiAnalyzer2011") and anter it
$ mkedanlzr JpsiAnalyzer2011
$ cd JpsiAnalyzer2011

If you list the content with command "ls" you will see some files and folders
Here a page with some informations about them.
https://twiki.cern.ch/twiki/bin/view/CMSPublic/SWGuideBuildFile#CmsswBuildFile

-Copy the BuildFile.xml from this git to your folder

The folder "src" is where the c++ file is. After you copy the c++ file, insire the folder src too,
of this git (here named "JpsiAnalyzerOpen2011.cc"), you must compile it with:
$scram b

Now copy the file "JPSIAnaOpenData2011.py"  of the folder "test" from this git to yout folder "test".
If you open it (with vi or other text editor) you will see, in the line 14:
"root://eospublic.cern.ch//eos/opendata/cms/Run2011A/Doub..."
This is the adress of the root file that you will apply your criteria selection
In the same file you will see, in the line 24: "'data_histo803.root'".
This will be your root file output after you criteria selection.

To run "JPSIAnaOpenData2011.py" you must use the command:
$ cmsRun JPSIAnaOpenData2011.py
And wait to finished.

