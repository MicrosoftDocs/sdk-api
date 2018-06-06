---
UID: NS:winioctl._STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
title: "_STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR"
author: windows-sdk-content
description: Used in conjunction with the IOCTL_STORAGE_QUERY_PROPERTY control code to retrieve the storage access alignment descriptor data for a device.
old-location: fs\storage_access_alignment_descriptor.htm
old-project: FileIO
ms.assetid: 99f33d12-5da0-4ed9-a20f-5e808a610545
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR structure pointer [Files], STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR structure [Files], _STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, fs.storage_access_alignment_descriptor, winioctl/PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, winioctl/STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR, PSTORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR structure


## -description


Used in conjunction with the 
   <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> control code to 
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

<pre class="syntax" xml:space="preserve"><code>+---------+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|LBA      |##|##|##|00|01|02|03|04|05|06|07|08|09|10|11|12|13|14|15|16|17|
+---------+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+--+
|Physical |                       |                       |                ...
|Sector   |           0           |           1           |           2
+---------+-----------------------+-----------------------+---------------</code></pre>
In this example, <code>BytesOffsetForSectorAlignment = 3 * BytesPerLogicalSector</code>.


## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a>
 

 

