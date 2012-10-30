PHP_CodeSniffer Fuel PHP Standard
=================================

PHP Code Sniffer rules that cover a large part of the [Fuel PHP coding standards]
(http://docs.fuelphp.com/general/coding_standards.html "Fuel PHP Coding Standards").

Install
-------------------
Technically this install can by bypassed by just telling PHP Code Sniffer where your standard is, this is mostly for convenience.

### Standard Linux

1. clone the project ``git clone git@github.com:ucfcdl/fuelphp-phpcs.git``
2. change directory to ./fuelphp-phpcs ``cd fuelphp-phpcs``
3. run installer with root privileges ``sudo ./install.sh``

### Linux (when pear libs are in unexpected places)

I installed a newer version of PHP on OSX, which left php and pear a little different then standard setups.  If you have a similar situation you may need to go the long way around to simplify your phpcs calls

1. clone the project ``git clone git@github.com:ucfcdl/fuelphp-phpcs.git``
2. locate *PEAR directory* using ``pear config-show``
3. verify *PEAR directory* above is included by php listed in the **include_dir** ``php -i``
4. create sym link to rules in this repo ``sudo ln -s DIRECTORY_TO_THIS_GIT_REPO/Standards/FuelPHP PEAR_DIRECTORY/PHP/CodeSniffer/Standards/FuelPHP``

Uninstall
----------------------

### Standard Linux
1. change directory to ./fuelphp-phpcs ``cd fuelphp-phpcs``
2. run installer with root privileges ``sudo ./uninstall.sh``

### Odd Linux Installs (see above)
1. remove sym link ``sudo rm PEAR_DIRECTORY/PHP/CodeSniffer/Standards/FuelPHP

How to use
----------
run ``phpcs --standard=FuelPHP PROJECT_TO_SNIFF_DIRECTORY`` where
_PROJECT_TO_SNIFF_DIRECTORY_ is your fuel php project directory.

### Without Convenient Install
run ``phpcs --standard=DIRECTORY_TO_THIS_REPO/Standards/FuelPHP PROJECT_TO_SNIFF_DIRECTORY``

**BE AWARE not to use --tab-width phpcs option with another value than 0,
this would disable tabs recognition !**
