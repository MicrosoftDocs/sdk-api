---
UID: NS:winioctl._DISK_GEOMETRY
title: DISK_GEOMETRY
author: windows-sdk-content
description: Describes the geometry of disk devices and media.
old-location: fs\disk_geometry_str.htm
tech.root: FileIO
ms.assetid: 5e5955b4-1319-42c9-9df8-9910c05dec69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PDISK_GEOMETRY, DISK_GEOMETRY, DISK_GEOMETRY structure [Files], _win32_disk_geometry_str, base.disk_geometry_str, fs.disk_geometry_str, winioctl/DISK_GEOMETRY'
ms.topic: struct
f1_keywords:
- winioctl/DISK_GEOMETRY
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoCtl.h
api_name:
- DISK_GEOMETRY
product: Windows
targetos: Windows
req.typenames: DISK_GEOMETRY, *PDISK_GEOMETRY
req.redist: 
---

# DISK_GEOMETRY structure


## -description


Describes the geometry of disk devices and media.


## -struct-fields




### -field Cylinders

The number of cylinders. See <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_large_integer">LARGE_INTEGER</a>.


### -field MediaType

The type of media. For a list of values, see 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-media_type">MEDIA_TYPE</a>.


### -field TracksPerCylinder

The number of tracks per cylinder.


### -field SectorsPerTrack

The number of sectors per track.


### -field BytesPerSector

The number of bytes per sector.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry">IOCTL_DISK_GET_DRIVE_GEOMETRY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_media_types">IOCTL_STORAGE_GET_MEDIA_TYPES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-media_type">MEDIA_TYPE</a>
 

 

