---
UID: NS:winioctl._DISK_EXTENT
title: DISK_EXTENT
description: Represents a disk extent.
helpviewer_keywords: ["*PDISK_EXTENT","DISK_EXTENT","DISK_EXTENT structure [Files]","PDISK_EXTENT","PDISK_EXTENT structure pointer [Files]","_win32_disk_extent_str","base.disk_extent_str","fs.disk_extent_str","winioctl/DISK_EXTENT","winioctl/PDISK_EXTENT"]
old-location: fs\disk_extent_str.htm
tech.root: fs
ms.assetid: 1b8dc6fa-e60b-4490-b439-44c93b6f4ce5
ms.date: 12/05/2018
ms.keywords: '*PDISK_EXTENT, DISK_EXTENT, DISK_EXTENT structure [Files], PDISK_EXTENT, PDISK_EXTENT structure pointer [Files], _win32_disk_extent_str, base.disk_extent_str, fs.disk_extent_str, winioctl/DISK_EXTENT, winioctl/PDISK_EXTENT'
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
targetos: Windows
req.typenames: DISK_EXTENT, *PDISK_EXTENT
req.redist: 
f1_keywords:
 - _DISK_EXTENT
 - winioctl/_DISK_EXTENT
 - PDISK_EXTENT
 - winioctl/PDISK_EXTENT
 - DISK_EXTENT
 - winioctl/DISK_EXTENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DISK_EXTENT
---

# DISK_EXTENT structure


## -description

Represents a disk extent.

## -struct-fields

### -field DiskNumber

The number of the disk that contains this extent.

This is the same number that is used to construct the name of the disk, for example, the *X* in "\\\\?\\PhysicalDrive*X*" or "\\\\?\\\Harddisk*X*".

### -field StartingOffset

The offset from the beginning of the disk to the extent, in bytes.

### -field ExtentLength

The number of bytes in this extent.

## -see-also

* [IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS](ni-winioctl-ioctl_volume_get_volume_disk_extents.md)
* [LARGE_INTEGER](../winnt/ns-winnt-large_integer-r1.md)
* [VOLUME_DISK_EXTENTS](ns-winioctl-volume_disk_extents.md)