---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SHSTOCKICONID enumeration


## -description


Used by <a href="https://msdn.microsoft.com/c08b1a53-e67c-4ed0-a9c6-d000c448e182">SHGetStockIconInfo</a> to identify which stock system icon to retrieve.


## -enum-fields




### -field SIID_DOCNOASSOC

<img alt="Blank document icon" src="images/SHSTOCKICONID/SIID_DOCNOASSOC.png"/>
 Document of a type with no associated application.


### -field SIID_DOCASSOC

<img alt="Application-associated document icon" src="images/SHSTOCKICONID/SIID_DOCASSOC.jpg"/>
 Document of a type with an associated application.


### -field SIID_APPLICATION

<img alt="" src="images/SHSTOCKICONID/SIID_APPLICATION.jpg"/>
 Generic application with no custom icon.


### -field SIID_FOLDER

<img alt="" src="images/SHSTOCKICONID/SIID_FOLDER.jpg"/>
 Folder (generic, unspecified state).


### -field SIID_FOLDEROPEN

<img alt="" src="images/SHSTOCKICONID/SIID_FOLDEROPEN.jpg"/>
 Folder (open).


### -field SIID_DRIVE525

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVE525.jpg"/>
 5.25-inch disk drive.


### -field SIID_DRIVE35

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVE35.jpg"/>
 3.5-inch disk drive.


### -field SIID_DRIVEREMOVE

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVEREMOVE.png"/>
 Removable drive.


### -field SIID_DRIVEFIXED

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVEFIXED.jpg"/>
 Fixed drive (hard disk).


### -field SIID_DRIVENET

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVENET.jpg"/>
 Network drive (connected).


### -field SIID_DRIVENETDISABLED

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVENETDISABLED.jpg"/>
 Network drive (disconnected).


### -field SIID_DRIVECD

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVECD.jpg"/>
 CD drive.


### -field SIID_DRIVERAM

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVERAM.jpg"/>
 RAM disk drive.


### -field SIID_WORLD

<img alt="" src="images/SHSTOCKICONID/SIID_WORLD.jpg"/>
 The entire network.


### -field SIID_SERVER

<img alt="" src="images/SHSTOCKICONID/SIID_SERVER.jpg"/>
 A computer on the network.


### -field SIID_PRINTER

<img alt="" src="images/SHSTOCKICONID/SIID_PRINTER.jpg"/>
 A local printer or print destination.


### -field SIID_MYNETWORK

<img alt="" src="images/SHSTOCKICONID/SIID_MYNETWORK.jpg"/>
 The <b>Network</b> virtual folder (<a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">FOLDERID_NetworkFolder</a>/<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_NETWORK</a>).


### -field SIID_FIND

<img alt="" src="images/SHSTOCKICONID/SIID_FIND.jpg"/>
 The <b>Search</b> feature.


### -field SIID_HELP

<img alt="" src="images/SHSTOCKICONID/SIID_HELP.jpg"/>
 The <b>Help and Support</b> feature.


### -field SIID_SHARE

<img alt="" src="images/SHSTOCKICONID/SIID_SHARE.jpg"/>
 Overlay for a shared item.


### -field SIID_LINK

<img alt="" src="images/SHSTOCKICONID/SIID_LINK.jpg"/>
 Overlay for a shortcut.


### -field SIID_SLOWFILE

<img alt="" src="images/SHSTOCKICONID/SIID_SLOWFILE.png"/>
 Overlay for items that are expected to be slow to access.


### -field SIID_RECYCLER

<img alt="" src="images/SHSTOCKICONID/SIID_RECYCLER.jpg"/>
 The Recycle Bin (empty).


### -field SIID_RECYCLERFULL

<img alt="" src="images/SHSTOCKICONID/SIID_RECYCLERFULL.jpg"/>
 The Recycle Bin (not empty).


### -field SIID_MEDIACDAUDIO

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIACDAUDIO.jpg"/>
 Audio CD media.


### -field SIID_LOCK

<img alt="" src="images/SHSTOCKICONID/SIID_LOCK.jpg"/>
 Security lock.


### -field SIID_AUTOLIST

<img alt="" src="images/SHSTOCKICONID/SIID_AUTOLIST.jpg"/>
 A virtual folder that contains the results of a search.


### -field SIID_PRINTERNET

<img alt="" src="images/SHSTOCKICONID/SIID_PRINTERNET.jpg"/>
 A network printer.


### -field SIID_SERVERSHARE

<img alt="" src="images/SHSTOCKICONID/SIID_SERVERSHARE.jpg"/>
 A server shared on a network.


### -field SIID_PRINTERFAX

<img alt="" src="images/SHSTOCKICONID/SIID_PRINTERFAX.jpg"/>
 A local fax printer.


### -field SIID_PRINTERFAXNET

<img alt="" src="images/SHSTOCKICONID/SIID_PRINTERFAXNET.jpg"/>
 A network fax printer.


### -field SIID_PRINTERFILE

<img alt="" src="images/SHSTOCKICONID/SIID_PRINTERFILE.jpg"/>
 A file that receives the output of a <b>Print to file</b> operation.


### -field SIID_STACK

<img alt="" src="images/SHSTOCKICONID/SIID_STACK.jpg"/>
 A category that results from a <b>Stack by</b> command to organize the contents of a folder.


### -field SIID_MEDIASVCD

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIASVCD.jpg"/>
 Super Video CD (SVCD) media.


### -field SIID_STUFFEDFOLDER

<img alt="" src="images/SHSTOCKICONID/SIID_STUFFEDFOLDER.jpg"/>
 A folder that contains only subfolders as child items.


### -field SIID_DRIVEUNKNOWN

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVEUNKNOWN.jpg"/>
 Unknown drive type.


### -field SIID_DRIVEDVD

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVEDVD.jpg"/>
 DVD drive.


### -field SIID_MEDIADVD

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIADVD.jpg"/>
 DVD media.


### -field SIID_MEDIADVDRAM

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIADVDRAM.jpg"/>
 DVD-RAM media.


### -field SIID_MEDIADVDRW

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIADVDRW.jpg"/>
 DVD-RW media.


### -field SIID_MEDIADVDR

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIADVDR.jpg"/>
 DVD-R media.


### -field SIID_MEDIADVDROM

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIADVDROM.jpg"/>
 DVD-ROM media.


### -field SIID_MEDIACDAUDIOPLUS

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIACDAUDIOPLUS.jpg"/>
 CD+ (enhanced audio CD) media.


### -field SIID_MEDIACDRW

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIACDRW.jpg"/>
 CD-RW media.


### -field SIID_MEDIACDR

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIACDR.jpg"/>
 CD-R media.


### -field SIID_MEDIACDBURN

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIACDBURN.jpg"/>
 A writeable CD in the process of being burned.


### -field SIID_MEDIABLANKCD

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIABLANKCD.jpg"/>
 Blank writable CD media.


### -field SIID_MEDIACDROM

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIACDROM.jpg"/>
 CD-ROM media.


### -field SIID_AUDIOFILES

<img alt="" src="images/SHSTOCKICONID/SIID_AUDIOFILES.jpg"/>
 An audio file.


### -field SIID_IMAGEFILES

<img alt="" src="images/SHSTOCKICONID/SIID_IMAGEFILES.jpg"/>
 An image file.


### -field SIID_VIDEOFILES

<img alt="" src="images/SHSTOCKICONID/SIID_VIDEOFILES.jpg"/>
 A video file.


### -field SIID_MIXEDFILES

<img alt="" src="images/SHSTOCKICONID/SIID_MIXEDFILES.jpg"/>
 A mixed file.


### -field SIID_FOLDERBACK

<img alt="" src="images/SHSTOCKICONID/SIID_FOLDERBACK.jpg"/>
 Folder back.


### -field SIID_FOLDERFRONT

<img alt="" src="images/SHSTOCKICONID/SIID_FOLDERFRONT.jpg"/>
 Folder front.


### -field SIID_SHIELD

<img alt="" src="images/SHSTOCKICONID/SIID_SHIELD.jpg"/>
 Security shield. Use for UAC prompts only.


### -field SIID_WARNING

<img alt="" src="images/SHSTOCKICONID/SIID_WARNING.jpg"/>
 Warning.


### -field SIID_INFO

<img alt="" src="images/SHSTOCKICONID/SIID_INFO.jpg"/>
 Informational.


### -field SIID_ERROR

<img alt="" src="images/SHSTOCKICONID/SIID_ERROR.jpg"/>
 Error.


### -field SIID_KEY

<img alt="" src="images/SHSTOCKICONID/SIID_KEY.jpg"/>
 Key.


### -field SIID_SOFTWARE

<img alt="" src="images/SHSTOCKICONID/SIID_SOFTWARE.jpg"/>
 Software.


### -field SIID_RENAME

<img alt="" src="images/SHSTOCKICONID/SIID_RENAME.jpg"/>
 A UI item, such as a button, that issues a rename command.


### -field SIID_DELETE

<img alt="" src="images/SHSTOCKICONID/SIID_DELETE.jpg"/>
 A UI item, such as a button, that issues a delete command.


### -field SIID_MEDIAAUDIODVD

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIAAUDIODVD.jpg"/>
 Audio DVD media.


### -field SIID_MEDIAMOVIEDVD

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIAMOVIEDVD.jpg"/>
 Movie DVD media.


### -field SIID_MEDIAENHANCEDCD

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIAENHANCEDCD.jpg"/>
 Enhanced CD media.


### -field SIID_MEDIAENHANCEDDVD

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIAENHANCEDDVD.jpg"/>
 Enhanced DVD media.


### -field SIID_MEDIAHDDVD

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIAHDDVD.jpg"/>
 High definition DVD media in the HD DVD format.


### -field SIID_MEDIABLURAY

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIABLURAY.jpg"/>
 High definition DVD media in the Blu-ray Disc™ format.


### -field SIID_MEDIAVCD

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIAVCD.jpg"/>
 Video CD (VCD) media.


### -field SIID_MEDIADVDPLUSR

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIADVDPLUSR.jpg"/>
 DVD+R media.


### -field SIID_MEDIADVDPLUSRW

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIADVDPLUSRW.jpg"/>
 DVD+RW media.


### -field SIID_DESKTOPPC

<img alt="" src="images/SHSTOCKICONID/SIID_DESKTOPPC.jpg"/>
 A desktop computer.


### -field SIID_MOBILEPC

<img alt="" src="images/SHSTOCKICONID/SIID_MOBILEPC.jpg"/>
 A mobile computer (laptop).


### -field SIID_USERS

<img alt="" src="images/SHSTOCKICONID/SIID_USERS.jpg"/>
 The <b>User Accounts</b> Control Panel item.


### -field SIID_MEDIASMARTMEDIA

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIASMARTMEDIA.jpg"/>
 Smart media.


### -field SIID_MEDIACOMPACTFLASH

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIACOMPACTFLASH.jpg"/>
 CompactFlash media.


### -field SIID_DEVICECELLPHONE

<img alt="" src="images/SHSTOCKICONID/SIID_DEVICECELLPHONE.jpg"/>
 A cell phone.


### -field SIID_DEVICECAMERA

<img alt="" src="images/SHSTOCKICONID/SIID_DEVICECAMERA.jpg"/>
 A digital camera.


### -field SIID_DEVICEVIDEOCAMERA

<img alt="" src="images/SHSTOCKICONID/SIID_DEVICEVIDEOCAMERA.jpg"/>
 A digital video camera.


### -field SIID_DEVICEAUDIOPLAYER

<img alt="" src="images/SHSTOCKICONID/SIID_DEVICEAUDIOPLAYER.jpg"/>
 An audio player.


### -field SIID_NETWORKCONNECT

<img alt="" src="images/SHSTOCKICONID/SIID_NETWORKCONNECT.jpg"/>
 Connect to network.


### -field SIID_INTERNET

<img alt="" src="images/SHSTOCKICONID/SIID_INTERNET.jpg"/>
 The <b>Network and Internet</b> Control Panel item.


### -field SIID_ZIPFILE

<img alt="" src="images/SHSTOCKICONID/SIID_ZIPFILE.jpg"/>
 A compressed file with a .zip file name extension.


### -field SIID_SETTINGS

<img alt="" src="images/SHSTOCKICONID/SIID_SETTINGS.jpg"/>
 The <b>Additional Options</b> Control Panel item.


### -field SIID_DRIVEHDDVD

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVEHDDVD.jpg"/>
<b>Windows Vista with Service Pack 1 (SP1) and later</b>. High definition DVD drive (any type - HD DVD-ROM, HD DVD-R, HD-DVD-RAM) that uses the HD DVD format.


### -field SIID_DRIVEBD

<img alt="" src="images/SHSTOCKICONID/SIID_DRIVEBD.jpg"/>
<b>Windows Vista with SP1 and later</b>. High definition DVD drive (any type - BD-ROM, BD-R, BD-RE) that uses the Blu-ray Disc format.


### -field SIID_MEDIAHDDVDROM

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIAHDDVDROM.jpg"/>
<b>Windows Vista with SP1 and later</b>. High definition DVD-ROM media in the HD DVD-ROM format.


### -field SIID_MEDIAHDDVDR

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIAHDDVDR.jpg"/>
<b>Windows Vista with SP1 and later</b>. High definition DVD-R media in the HD DVD-R format.


### -field SIID_MEDIAHDDVDRAM

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIAHDDVDRAM.jpg"/>
<b>Windows Vista with SP1 and later</b>. High definition DVD-RAM media in the HD DVD-RAM format.


### -field SIID_MEDIABDROM

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIABDROM.jpg"/>
<b>Windows Vista with SP1 and later</b>. High definition DVD-ROM media in the Blu-ray Disc BD-ROM format.


### -field SIID_MEDIABDR

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIABDR.jpg"/>
<b>Windows Vista with SP1 and later</b>. High definition write-once media in the Blu-ray Disc BD-R format.


### -field SIID_MEDIABDRE

<img alt="" src="images/SHSTOCKICONID/SIID_MEDIABDRE.jpg"/>
<b>Windows Vista with SP1 and later</b>. High definition read/write media in the Blu-ray Disc BD-RE format.


### -field SIID_CLUSTEREDDRIVE

<img alt="" src="images/SHSTOCKICONID/SIID_CLUSTEREDDRIVE.jpg"/>
<b>Windows Vista with SP1 and later</b>. A cluster disk array.


### -field SIID_MAX_ICONS

The highest valid value in the enumeration. Values over 160 are Windows 7-only icons.


## -remarks



SIID_INVALID, with a value of -1, indicates an invalid <b>SHSTOCKICONID</b> value.



