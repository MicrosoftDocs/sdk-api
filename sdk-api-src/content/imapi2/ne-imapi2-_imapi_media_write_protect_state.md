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

# _IMAPI_MEDIA_WRITE_PROTECT_STATE enumeration


## -description


Defines values that indicate the media write protect status.   One or more write protect values can be set on a given drive.


## -enum-fields




### -field IMAPI_WRITEPROTECTED_UNTIL_POWERDOWN

  Power to the drive needs to be cycled before allowing writes to the media.


### -field IMAPI_WRITEPROTECTED_BY_CARTRIDGE

The media is in a cartridge with the write protect tab set.


### -field IMAPI_WRITEPROTECTED_BY_MEDIA_SPECIFIC_REASON

The drive is disallowing writes for a media-specific reason. For example:  <ul>
<li>The media was originally in a cartridge and was set to disallow writes when the media is not in a cartridge.</li>
<li>The media has used all available spare areas for defect management and is preventing writes to protect the existing data.</li>
</ul>



### -field IMAPI_WRITEPROTECTED_BY_SOFTWARE_WRITE_PROTECT

A write-protect flag on the media is set. Various media types, such as DVD-RAM and DVD-RW, support a special area on the media to indicate the disc's write protect status.


### -field IMAPI_WRITEPROTECTED_BY_DISC_CONTROL_BLOCK

A write-protect flag in the disc control block of a DVD+RW disc is set. DVD+RW media can persistently alter the write protect state of media by writing a device control block (DCB) to the media.  

This value has limited usefulness because some DVD+RW drives do not recognize or honor this setting.


### -field IMAPI_WRITEPROTECTED_READ_ONLY_MEDIA

The drive does not recognize write capability of the media.


## -see-also




<a href="https://msdn.microsoft.com/b3e58024-9a51-46e9-a9a1-c850166c9a85">IDiscFormat2Data::get_WriteProtectStatus</a>
 

 

