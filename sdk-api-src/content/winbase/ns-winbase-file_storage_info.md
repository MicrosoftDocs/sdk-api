---
UID: NS:winbase._FILE_STORAGE_INFO
title: FILE_STORAGE_INFO (winbase.h)
description: Contains directory information for a file. (FILE_STORAGE_INFO)
helpviewer_keywords: ["*PFILE_STORAGE_INFO","FILE_STORAGE_INFO","FILE_STORAGE_INFO structure [Files]","PFILE_STORAGE_INFO","PFILE_STORAGE_INFO structure pointer [Files]","STORAGE_INFO_FLAGS_ALIGNED_DEVICE","STORAGE_INFO_FLAGS_PARTITION_ALIGNED_ON_DEVICE","_FILE_STORAGE_INFO","fs.file_storage_info","winbase/FILE_STORAGE_INFO","winbase/PFILE_STORAGE_INFO"]
old-location: fs\file_storage_info.htm
tech.root: fs
ms.assetid: 1aa9585d-9001-4d94-babe-a39c8dde2332
ms.date: 12/05/2018
ms.keywords: '*PFILE_STORAGE_INFO, FILE_STORAGE_INFO, FILE_STORAGE_INFO structure [Files], PFILE_STORAGE_INFO, PFILE_STORAGE_INFO structure pointer [Files], STORAGE_INFO_FLAGS_ALIGNED_DEVICE, STORAGE_INFO_FLAGS_PARTITION_ALIGNED_ON_DEVICE, _FILE_STORAGE_INFO, fs.file_storage_info, winbase/FILE_STORAGE_INFO, winbase/PFILE_STORAGE_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: FILE_STORAGE_INFO, *PFILE_STORAGE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILE_STORAGE_INFO
 - winbase/_FILE_STORAGE_INFO
 - PFILE_STORAGE_INFO
 - winbase/PFILE_STORAGE_INFO
 - FILE_STORAGE_INFO
 - winbase/FILE_STORAGE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - FILE_STORAGE_INFO
---

# FILE_STORAGE_INFO structure


## -description

Contains directory information for a file. This structure is returned from the 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a> function when 
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

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>
