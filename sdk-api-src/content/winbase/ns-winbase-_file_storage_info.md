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

# _FILE_STORAGE_INFO structure


## -description


Contains directory information for a file. This structure is returned from the 
    <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a> function when 
    <b>FileStorageInfo</b> is passed in the <i>FileInformationClass</i> 
    parameter.


## -struct-fields




### -field LogicalBytesPerSector

Logical bytes per sector  reported by physical storage. This is the smallest size for which uncached I/O is 
      supported.


### -field PhysicalBytesPerSectorForAtomicity

Bytes per sector for atomic writes. Writes smaller than this may require a read before the entire block can 
      be written atomically.


### -field PhysicalBytesPerSectorForPerformance

Bytes per sector for optimal performance for writes.


### -field FileSystemEffectivePhysicalBytesPerSectorForAtomicity

This is the size of the block used for atomicity by the file system. This may be a trade-off between the 
      optimal size of the physical media and one that is easier to adapt existing code and structures.


### -field Flags

This member can contain combinations of flags specifying information about the alignment of the 
      storage.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STORAGE_INFO_FLAGS_ALIGNED_DEVICE"></a><a id="storage_info_flags_aligned_device"></a><dl>
<dt><b>STORAGE_INFO_FLAGS_ALIGNED_DEVICE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
When set, this flag indicates that the logical sectors of the storage device are aligned to physical 
        sector boundaries.

</td>
</tr>
<tr>
<td width="40%"><a id="STORAGE_INFO_FLAGS_PARTITION_ALIGNED_ON_DEVICE____"></a><a id="storage_info_flags_partition_aligned_on_device____"></a><dl>
<dt><b>STORAGE_INFO_FLAGS_PARTITION_ALIGNED_ON_DEVICE    </b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
When set, this flag indicates that the partition is aligned to physical sector boundaries on the 
        storage device.

</td>
</tr>
</table>
 


### -field ByteOffsetForSectorAlignment

Logical sector offset within the first physical sector where the first logical sector is placed, in bytes. 
      If this value is set to <b>STORAGE_INFO_OFFSET_UNKNOWN</b> (0xffffffff), there was 
      insufficient information to compute this field.


### -field ByteOffsetForPartitionAlignment

Offset used to align the partition to a physical sector boundary on the storage device, in bytes. If this 
      value is set to <b>STORAGE_INFO_OFFSET_UNKNOWN</b> (0xffffffff), there was insufficient 
      information to compute this field.


## -remarks



If a volume is built on top of storage devices with different properties (for example a mirrored, spanned, 
    striped, or RAID configuration) the sizes returned are those of the largest size of any of the underlying storage 
    devices.




## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>
 

 

