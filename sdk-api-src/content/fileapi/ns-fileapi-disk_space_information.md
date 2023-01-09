---
UID: NS:fileapi.DISK_SPACE_INFORMATION
tech.root: fs
title: DISK_SPACE_INFORMATION structure (fileapi.h)
ms.date: 01/05/2023
targetos: Windows
description: The DISK_SPACE_INFORMATION structure contains information about the disk space for a particular volume.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: fileapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DISK_SPACE_INFORMATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fileapi.h
api_name:
 - DISK_SPACE_INFORMATION
f1_keywords:
 - DISK_SPACE_INFORMATION
 - fileapi/DISK_SPACE_INFORMATION
dev_langs:
 - c++
helpviewer_keywords:
 - DISK_SPACE_INFORMATION
---

## -description

The **DISK_SPACE_INFORMATION** structure contains information about the disk space for a particular volume.

## -struct-fields

### -field ActualTotalAllocationUnits

The `ActualTotalAllocationUnits` is the total volume size without considering Quota setting.

### -field ActualAvailableAllocationUnits

The `ActualTotalAllocationUnits` is the available space for the volume without considering Quota setting.

### -field ActualPoolUnavailableAllocationUnits

The `ActualPoolUnavailableAllocationUnits` is the unavailable space for the volume due to insufficient free pool space

### -field CallerTotalAllocationUnits

The `CallerTotalAllocationUnits` is the total volume size limited by Quota setting.

### -field CallerAvailableAllocationUnits

The `CallerAvailableAllocationUnits` is the available space for the volume limited by Quota setting.

### -field CallerPoolUnavailableAllocationUnits

The `CallerAvailableAllocationUnits` is the unavailable space for the volume due to insufficient free pool space.

### -field UsedAllocationUnits

The used space of the volume.

### -field TotalReservedAllocationUnits

Total reserved space.

### -field VolumeStorageReserveAllocationUnits

A special type of reserved space for per-volume storage reserve. This is included in the `TotalReservedAllocationUnits`.

### -field AvailableCommittedAllocationUnits

The space that has been committed by storage pool but has not been allocated by file system.

### -field PoolAvailableAllocationUnits

Available space in corresponding storage pool. If the volume is not a spaces volume, the `PoolAvailableAllocationUnits` is set to `0`.

### -field SectorsPerAllocationUnit

The number of sectors per allocation unit for the volume.

### -field BytesPerSector

The number of bytes per sector for the volume.

## -remarks

## -see-also

[GetDiskSpaceInformationA](nf-fileapi-getdiskspaceinformationa.md)

[GetDiskSpaceInformationW](nf-fileapi-getdiskspaceinformationw.md)
