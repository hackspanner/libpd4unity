libpd (pure data) for unity 5.x

updated from libpd4unity by Patrick Sebastien

this project only supports Windows currently 

### status: ###
* working with unity pro and unity free*
* Windows 32bit & 64bit

The following files/folders in the Unity project are of relevance:
* LibPdFilterRead.cs: Initialises libpd, sets up audio callback, opens patches, etc. Best attached to the camera or an empty game object. Make sure there is only ONE instance of this script active in a scene. 
* GUITextScript.cs: Example that shows how to receive messages from Pd
* GUIToggleScript.cs: Example that shows how to send messages to Pd
* 01\_LibPd_Basic.unity: A scene that shows the above working
* 02\_LibPd_ADC.unity: A scene that shows how to pass audio into Pd using adc~

The whole libpd API hasn't been tested, but will happen at some point in the near future. Feel free to test and report any issues. 

### setup: ###
To ensure cross-platform compatibility, place all patches, audio files and externals in Assets > StreamingAssets > PdAssets. Externals have been tested and work fine on OSX. Other platforms are pending.

### known issues: ###
* Unpredictable SIGILL when using Unity Editor

### thanks to: ###
* Miller Puckette (pure data)
* Peter Brinkmann (libpd)
* Tebjan Halm (libpdcsharp)
* Jean-S�bastien Leduc (bridge)
* Magicolo (uPD)
* Patrick Sebastien || http://www.workinprogress.ca || (all the initial work and Windows support)
* Varun Nair || http://www.re-sounding.com/ || (OSX and Android) 
* Peter Cardwell-Gardner || http://www.thefuntastic.com/ || (dll not found fix)
* Patrick Sebastien

### original project (unity4 winx86,android,ios support): ###
* https://github.com/patricksebastien/libpd4unity ###

### howto: ###
* Windows: nuget.exe install LibPDBinding -Version 0.3.0
