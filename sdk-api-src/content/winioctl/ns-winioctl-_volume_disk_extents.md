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

# _VOLUME_DISK_EXTENTS structure


## -description


Represents a physical location on a disk. It is the output buffer for the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560644">IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS</a> 
    control code.


## -struct-fields




### -field NumberOfDiskExtents

The number of disks in the volume (a volume can span multiple disks).

An extent is a contiguous run of sectors on one disk. When the number of extents returned is greater than 
       one (1), the error code  <b>ERROR_MORE_DATA</b> is returned. You should call 
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> again, allocating enough buffer 
       space based on the value of <b>NumberOfDiskExtents</b> after the first 
       <b>DeviceIoControl</b> call.


### -field Extents

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff552606">DISK_EXTENT</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552606">DISK_EXTENT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560644">IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS</a>
 

 

