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

# _DISK_EXTENT structure


## -description


Represents a disk extent.


## -struct-fields




### -field DiskNumber

The number of the disk that contains this extent.

This is the same number that is used to construct the name of the disk, for example, the 
       <i>X</i> in "\\?\PhysicalDrive<i>X</i>" 
       or "\\?\Harddisk<i>X</i>".


### -field StartingOffset

The offset from the beginning of the disk to the extent, in bytes.


### -field ExtentLength

The number of bytes in this extent.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560644">IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568017">VOLUME_DISK_EXTENTS</a>
 

 

