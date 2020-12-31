Show files installed by package:
   ```
   dpkg -L package
   ```

List all installed packages:
   ```
   apt list --installed
   ```

Which installed package owns a file:
   ```
   dpkg -S /bin/ls
   ```

Search repository for files with given name:
   ```
   sudo apt-get install apt-file
   sudo apt-file update
   apt-file find kwallet.h
   ```

Serch for package name in repository:
   ```
   apt-cache search qt4
   ```

Remove the binaries, but not the configuration or data files of the package:
   ```
   apt-get remove packagename
   ```

Remove about everything regarding the package, but not the dependencies installed with it on installation. Both commands are equivalent:
   ```
   apt-get purge packagename
   apt-get remove --purge packagename
   ```

Removes orphaned packages, i.e. installed packages that used to be installed as an dependency, but aren't any longer. Use this after removing a package which had installed dependencies you're no longer interested in:
   ```
   apt-get autoremove
   ```

Remove other packages which were required by packagename on but are not required by any remaining packages. Note that aptitude only remembers dependency information for packages that it has installed.
   ```
   aptitude remove packagename or aptitude purge packagename (likewise)
   ```

Removes package with dependencies:
   ```
   dpkg --purge --force-depends application
   ```

