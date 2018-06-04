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

# _DISK_INT13_INFO structure


## -description


Contains standard Int13 drive geometry parameters.


## -struct-fields




### -field DriveSelect

The letter that is related to the specified partition or hard disk.  For valid values, see the BIOS documentation.


### -field MaxCylinders

The maximum number of cylinders per head. For valid values, see the BIOS documentation.


### -field SectorsPerTrack

The number of sectors per track. For valid values, see the BIOS documentation.


### -field MaxHeads

The maximum number of heads for this hard disk.  For valid values, see the BIOS documentation.


### -field NumberDrives

The number of drives. For valid values, see the BIOS documentation.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552601">DISK_DETECTION_INFO</a>
 

 

