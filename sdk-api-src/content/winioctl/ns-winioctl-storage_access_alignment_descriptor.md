---
UID: NS:winioctl._STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
title: STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
description: Used in conjunction with the IOCTL_STORAGE_QUERY_PROPERTY control code to retrieve the storage access alignment descriptor data for a device.
helpviewer_keywords: ["*PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR","PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR","PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR structure pointer [Files]","STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR","STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR structure [Files]","fs.storage_access_alignment_descriptor","winioctl/PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR","winioctl/STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR"]
old-location: fs\storage_access_alignment_descriptor.htm
tech.root: fs
ms.assetid: 99f33d12-5da0-4ed9-a20f-5e808a610545
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR structure pointer [Files], STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR structure [Files], fs.storage_access_alignment_descriptor, winioctl/PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, winioctl/STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, *PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
req.redist: 
f1_keywords:
 - _STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
 - winioctl/_STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
 - PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
 - winioctl/PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
 - STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
 - winioctl/STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
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
 - STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
---

# STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR structure


## -description

Used in conjunction with the 
   <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control code to 
   retrieve the storage access alignment descriptor data for a device.

## -struct-fields

### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.

### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.

### -field BytesPerCacheLine

The number of bytes in a cache line of the device.

### -field BytesOffsetForCacheAlignment

The address offset necessary for proper cache access alignment, in bytes.

### -field BytesPerLogicalSector

The number of bytes in a logical sector of the device.

### -field BytesPerPhysicalSector

The number of bytes in a physical sector of the device.

### -field BytesOffsetForSectorAlignment

The logical sector offset within the first physical sector where the first logical sector is placed, in bytes.

Example:  Offset = 3 Logical sectors


``` syntax
+---------+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|LBA      |##|##|##|00|01|02|03|04|05|06|07|08|09|10|11|12|13|14|15|16|17|
+---------+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|Physical |                       |                       |                ...
|Sector   |           0           |           1           |           2
+---------+-----------------------+-----------------------+---------------
```

In this example, <code>BytesOffsetForSectorAlignment = 3 * BytesPerLogicalSector</code>.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>
