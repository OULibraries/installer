# Installer

This installer configures the Measure the Future project on an Intel Edison. It installs both scout and mothership components.

![alpha](https://img.shields.io/badge/stability-alpha-orange.svg?style=flat "Alpha")&nbsp;
 ![GPLv3 License](https://img.shields.io/badge/license-GPLv3-blue.svg?style=flat "GPLv3 License")

## Installation (Edison)

1. [Download the latest Edison Installer from Intel](https://software.intel.com/en-us/iot/hardware/edison/downloads)
2. Update your Edison to the latest firmware version (3.5 at the time of writing).
3. Open up a terminal and run 'screen' to access your Edison (the xxx part will differ for your board)
```
	$ screen -L /dev/cu.usbserial-XXXXXXXX 115200 –L
```
4. Use 'root' for the login.
5. Configure the Intel Edison to connect to the Internet over a wifi network.
```
	# configure_edison --wifi
```
6. Download and run the mtf-install script.
```
	# wget https://raw.githubusercontent.com/MeasureTheFuture/installer/master/mtf-install.sh
	# wget https://raw.githubusercontent.com/MeasureTheFuture/installer/master/db-bootstrap.sql
	# chmod +x mtf-install.sh
	# ./mtf-install.sh
```

## TODO:
* Automatically spin up postgres on boot.
* Automatically spin up the scout on boot.
* Automatically spin up the mothership on boot.
* Prompt the user for a Posgres/DB password.
* Prompt the user for a wifi access point password.
* Look at uninstalling gstreamer and python as well.
* fix up all the go get github module warnings.

## License

Copyright (C) 2016, Clinton Freeman

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
