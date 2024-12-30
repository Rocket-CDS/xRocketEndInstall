# xRocketEndInstall

This module is to copy files and SQL required by RockCDS on installation.

Some SQL needs to be execute after all other DNN modules.  (Personabar)

There is no compile on this modules.

To build the install package, zip the files into a zip file called "xRocketEndInstall.zip", this file then needs to be the release for the GitHub project.  

1. Download the GitHub zip file.
2. Unzip into a folder.
3. Zip the files on the root of the repo as the root of the package release zip, include subfolders.

The zip file name should be "xRocketEndInstall.zip"

## Magick

Magick as the assemblies required for webp image processing.  

Due to an assembly being locked when used this install package has been created so a general upgrade of any RocketCDS package does not have a problem.  

### Upgrade Magick
If an upgrade of the Magick assemblies are required then the AppPool should be restarted and the first operation after should be to install this packaged, this will avoid the file lock issue.  

**NOTE: A Restart from DNN does not always work, in such case recycle the AppPool from IIS**  

### Alternative Upgrade Magick
- Stop the AppPool.
- Copy the Assemblies to the \bin folder of the installation.
- Restart AppPool.

**Assemblies**  
Magick.Native-Q8-x64.dll  
Magick.NET.Core.dll  
Magick.NET-Q8-AnyCPU.dll  



https://github.com/dlemstra/Magick.NET

*No compile is required*
