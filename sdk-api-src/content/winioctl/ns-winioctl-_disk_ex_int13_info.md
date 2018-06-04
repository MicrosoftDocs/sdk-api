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

# _DISK_EX_INT13_INFO structure


## -description


Contains extended Int13 drive parameters.


## -struct-fields




### -field ExBufferSize

The size of the extended drive parameter buffer for this partition or disk.  For valid values, see the BIOS documentation.


### -field ExFlags

The information flags for this partition or disk.  For valid values, see the BIOS documentation.


### -field ExCylinders

The number of cylinders per head.  For valid values, see the BIOS documentation.


### -field ExHeads

The maximum number of heads for this hard disk.  For valid values, see the BIOS documentation.


### -field ExSectorsPerTrack

The number of sectors per track.  For valid values, see the BIOS documentation.


### -field ExSectorsPerDrive

The total number of sectors for this disk.  For valid values, see the BIOS documentation.


### -field ExSectorSize

The sector size for this disk.  For valid values, see the BIOS documentation.


### -field ExReserved

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552601">DISK_DETECTION_INFO</a>
 

 

