Crayfish (QGIS plugin)
======================

<img align="right" src="https://raw.githubusercontent.com/lutraconsulting/qgis-crayfish-plugin/master/crayfish/crayfish_128px.png">

The Crayfish Plugin is a visualiser for temporal structured/unstructured grids in QGIS.

You can use Crayfish to load the following file formats in QGIS:


- [NetCDF](https://en.wikipedia.org/wiki/NetCDF): Generic format for scientific data. Examples can be found [here](http://apps.ecmwf.int/datasets/data/interim-full-daily/levtype=sfc/)
- [GRIB](https://en.wikipedia.org/wiki/GRIB): Format commonly used in meteorology. Examples can be found [here](http://apps.ecmwf.int/datasets/data/interim-full-daily/levtype=sfc/)
- [XMDF](https://en.wikipedia.org/wiki/XMDF): As an example, hydraulic outputs from TUFLOW modelling package
- [SWW](http://anuga.anu.edu.au/): Outputs of the ANUGA modelling package
- [DAT](http://www.xmswiki.com/wiki/SMS:ASCII_Dataset_Files_*.dat): Outputs of various hydrodynamic modelling packages (e.g. BASEMENT, HYDRO_AS-2D)
- [HEC-RAS](http://www.hec.usace.army.mil/software/hec-ras/): Outputs of the HEC-RAS modelling package
- [Serafin files](http://www.gdal.org/drv_selafin.html): Outputs of the TELEMAC 2D hydrodynamic modelling package

<img src="https://travis-ci.org/lutraconsulting/qgis-crayfish-plugin.svg?branch=master">

### Using Crayfish

For instructions of how to install and use Crayfish, please refer to the [Crayfish resources page][crp] on our website.

### Installing Crayfish on Linux

For installing Crayfish on Linux you need:

* development environment and a compiler installed
* Qt4 and development tools
* HDF5 library (for XMDF format)
* NetCDF library (for AnuGA SWW format)
* GDAL library

On Debian/Ubuntu you need to install the following packages:

```bash
sudo apt-get install build-essential libqt4-dev qt4-qmake libgdal-dev libhdf5-dev libnetcdf-dev libproj-dev git
```

If all this packages are installed you can clone the crayfish plugin using the command:

```bash
git clone https://github.com/lutraconsulting/qgis-crayfish-plugin.git
```

After cloning the source you should run the installation script which compiles and installs everything
to user's QGIS python plugin directory (`~/.qgis2/python/plugins/crayfish`):

```bash
cd qgis-crayfish-plugin
export QT_SELECT=qt4
./install.py
```

Now restart QGIS and you are able to use crayfish plugin on your Linux Computer.


### Installing Crayfish on Windows

For 32-bit version:

* Install Microsoft Visual Studio 2008
* Install OSGeo4W (32bit) to C:\OSGeo4W
* Run scripts\crayfish32.bat to build the crayfish DLL

For 64-bit version:

* Install Microsoft Visual Studio 2010
* Install OSGeo4W (64bit) to C:\OSGeo4W64
* Run scripts\crayfish64.bat to build the crayfish DLL


[crp]: http://www.lutraconsulting.co.uk/resources/crayfish
