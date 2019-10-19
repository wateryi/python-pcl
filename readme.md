# How to install on windows 10

## download
1. `Visual Studio 2017 - 64 bit <https://github.com/PointCloudLibrary/pcl/releases/download/pcl-1.9.1/PCL-1.9.1-AllInOne-msvc2017-win64.exe>`_
2. git clone https://github.com/wateryi/python-pcl.git
3. `Windows Gtk+ Download <http://www.tarnyko.net/dl/gtk.htm>`_
### summary
We got files PCL-1.9.1-AllInOne-msvc2017-win64.exe, gtk+-bundle_3.6.4-20130513_win64.zip, and folder python-pcl-master
## prepare
1. unzip gtk+-bundle_3.6.4-20130513_win64.zip
2. copy folder gtk+-bundle_3.6.4-20130513_win64\bin to python-pcl-master\pkg-config

## install
### install pcl
1. run PCL-1.9.1-AllInOne-msvc2017-win64.exe, set install path as "C:\ProgramFiles\PCL 1.9.1" remove the space in 'Program Files'
2. install OpenNI2 similar with step 1

### set enviroment 
1. Add %PCL_ROOT%\bin\;%OPEN_NI2_ROOT%\Tools;%VTK_ROOT%\bin; at the end of Path
2. Add new variable PCL_ROOT with value C:\ProgramFiles\PCL 1.9.1
3. Add new variable PCL_VERSION with value 1.9
4. Add new variable VTK_ROOT with value C:\ProgramFiles\PCL 1.9.1\3rdParty\VTK
5. Check if the below enviroment existed
              'OPENNI2_INCLUDE64': 'C:\\ProgramFiles\\OpenNI2\\Include\\',
              'OPENNI2_LIB64': 'C:\\ProgramFiles\\OpenNI2\\Lib\\',
              'OPENNI2_REDIST64': 'C:\\ProgramFiles\\OpenNI2\\Redist\\',
              'OPEN_NI2_ROOT': 'C:\\ProgramFiles\\OpenNI2'
### anaconda setting
1. create a new enviroment with python vertion 3.6.X, activate it
2. Open terminal
2. conda install -c anaconda numpy
3. conda install -c anaconda cython

### install python-pcl
1. Enter in folder python-pcl-master with the terminal
2. python setup.py build_ext -i
3. python setup.py install
