---
UID: NS:winioctl._DISK_EXTENT
title: DISK_EXTENT
author: windows-sdk-content
description: Represents a disk extent.
old-location: fs\disk_extent_str.htm
tech.root: fileio
ms.assetid: 1b8dc6fa-e60b-4490-b439-44c93b6f4ce5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDISK_EXTENT, DISK_EXTENT, DISK_EXTENT structure [Files], PDISK_EXTENT, PDISK_EXTENT structure pointer [Files], _win32_disk_extent_str, base.disk_extent_str, fs.disk_extent_str, winioctl/DISK_EXTENT, winioctl/PDISK_EXTENT"
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
 - DISK_EXTENT
product: Windows
targetos: Windows
req.typenames: DISK_EXTENT, *PDISK_EXTENT
req.redist: 
---

# DISK_EXTENT structure


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




<a href="https://msdn.microsoft.com/8faff037-d815-48f8-8b59-d63f4ff4a746">IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>



<a href="https://msdn.microsoft.com/3f38f03c-1b99-4072-904c-dca1b98a245c">VOLUME_DISK_EXTENTS</a>
 

 

