---
UID: NS:winioctl._DISK_GEOMETRY
title: "_DISK_GEOMETRY"
author: windows-driver-content
description: Describes the geometry of disk devices and media.
old-location: fs\disk_geometry_str.htm
old-project: FileIO
ms.assetid: 5e5955b4-1319-42c9-9df8-9910c05dec69
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PDISK_GEOMETRY, DISK_GEOMETRY, DISK_GEOMETRY structure [Files], _DISK_GEOMETRY, _win32_disk_geometry_str, base.disk_geometry_str, fs.disk_geometry_str, winioctl/DISK_GEOMETRY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DISK_GEOMETRY, *PDISK_GEOMETRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	DISK_GEOMETRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

