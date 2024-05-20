# astpp_installer
This installation script is partly based on the iNetrix Technologies Pvt. Ltd. installtion script for installing ASTPP.
#
This script will only install version 5 of ASTPP, and for using only  
Debian 11

The purpose of this script is for multiple reasons compared to the one provided by iNetrix:

 1) Uses FreeSwitch packages from SignalWire repo 
    which requires a SignalWire account with a token attached to that account

 2) Uses MariaDB from the Debian repo instead of MySQL from their repo.
    This has caused issues in the past

 3) Does not use RemiRepo for PHP 7.3+. iNetrix for unknown reasons uses the RemiRepo  
    Instead uses PHP Version 7.4

 4) No longer support of CentOS 7/8 as those are End of Life
    CentOS Stream is now the default distro, and not stable for production
    May consider Rocky Linux 8 (CentOS 8 fork) in the future

 5) Option to install Postfix instead of sendmail which provides better logging

 6) No telemetry sent
 
 7) option to install Let's Encrypt Certificate

WARNING: Make sure the date/time is correct on the server before proceeding, or the install can fail.

To excute installer (must be as root or sudo): 


wget https://raw.githubusercontent.com/hecatae/astpp_installer/main/astpp_v6_install_Deb11_FS_packages.sh

chmod +x astpp_v6_install_Deb11_FS_packages.sh


./astpp_v6_install_Deb11_FS_packages.sh



