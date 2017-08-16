Roseapple Pi SD Card Image Tool
#################################################################################<br>
Copyright (C) 2015-2017 Saeid Ghazagh <sghazagh@elar-systems.com><br>
<br>
ELAR-Systems<br>
------------<br>
http://www.elar-systems.com<br>
http://www.elar-systems.com.au<br>
<br>
This program is free software; you can redistribute it and/or<br>
modify it under the terms of the GNU General Public License <br>
as published by the Free Software Foundation; either version 2 <br>
of the License, or (at your option) any later version. <br>
 <br>
This program is distributed in the hope that it will be useful, <br>
but WITHOUT ANY WARRANTY; without even the implied warranty of <br>
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the <br>
GNU General Public License for more details. <br>
<br><br>

Required Packages: <br>
-------------------<br>
dd, parted, kpartx, bmap-tools
<br>

Usage<br>
------------ <br>
First get a local copy to your machine <br>
$ git clone https://github.com/elar-systems/Roseapple-Pi<br>

You can make an Image now: <br>
$ cd Roseapple-Pi <br>
$ ./make-roseapple-sdcard-img.sh <image_file_name> <br>
<br>
<b>Note:</b> Script asks you to confirm creating the partition. Type "Yes" to continue.
If it shows the Warning for End Sector of Image, just Ignore it as it automatically adjusts the image end sector size.
<br>
<br>
If you are on a Debian based system, you can install bmap-tools <br>
$ sudo apt-get install bmap-tools <br>
 <br>
Extract the archive and use bmaptool to copy it to the SD card <br>
$ sudo bmaptool copy your_sd_image.img /dev/sdX 
 <br>
You can also use dd but it will take a lot longer since bmaptool doesn't write the empty bits <br>
Windows users can use "Win32DiskImager" to write the .img file to the SD card <br>
 
