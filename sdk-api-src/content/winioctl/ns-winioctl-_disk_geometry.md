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

# _DISK_GEOMETRY structure


## -description


Describes the geometry of disk devices and media.


## -struct-fields




### -field Cylinders

The number of cylinders. See <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>.


### -field MediaType

The type of media. For a list of values, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a>.


### -field TracksPerCylinder

The number of tracks per cylinder.


### -field SectorsPerTrack

The number of sectors per track.


### -field BytesPerSector

The number of bytes per sector.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560357">IOCTL_DISK_GET_DRIVE_GEOMETRY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560559">IOCTL_STORAGE_GET_MEDIA_TYPES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a>
 

 

