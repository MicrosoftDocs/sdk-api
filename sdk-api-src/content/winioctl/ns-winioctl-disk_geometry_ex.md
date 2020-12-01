---
UID: NS:winioctl._DISK_GEOMETRY_EX
title: DISK_GEOMETRY_EX
description: Describes the extended geometry of disk devices and media.
helpviewer_keywords: ["*PDISK_GEOMETRY_EX","DISK_GEOMETRY_EX","DISK_GEOMETRY_EX structure [Files]","PDISK_GEOMETRY_EX","PDISK_GEOMETRY_EX structure pointer [Files]","_win32_disk_geometry_ex_str","base.disk_geometry_ex_str","fs.disk_geometry_ex_str","winioctl/DISK_GEOMETRY_EX","winioctl/PDISK_GEOMETRY_EX"]
old-location: fs\disk_geometry_ex_str.htm
tech.root: fs
ms.assetid: 2b8b2021-8650-452d-a975-54249620d72f
ms.date: 12/05/2018
ms.keywords: '*PDISK_GEOMETRY_EX, DISK_GEOMETRY_EX, DISK_GEOMETRY_EX structure [Files], PDISK_GEOMETRY_EX, PDISK_GEOMETRY_EX structure pointer [Files], _win32_disk_geometry_ex_str, base.disk_geometry_ex_str, fs.disk_geometry_ex_str, winioctl/DISK_GEOMETRY_EX, winioctl/PDISK_GEOMETRY_EX'
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
req.typenames: DISK_GEOMETRY_EX, *PDISK_GEOMETRY_EX
req.redist: 
f1_keywords:
 - _DISK_GEOMETRY_EX
 - winioctl/_DISK_GEOMETRY_EX
 - PDISK_GEOMETRY_EX
 - winioctl/PDISK_GEOMETRY_EX
 - DISK_GEOMETRY_EX
 - winioctl/DISK_GEOMETRY_EX
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
 - DISK_GEOMETRY_EX
---

# DISK_GEOMETRY_EX structure


## -description

Describes the extended geometry of disk devices and media.

## -struct-fields

### -field Geometry

A [**DISK_GEOMETRY**](ns-winioctl-disk_geometry.md) structure.

### -field DiskSize

The disk size, in bytes. See [**LARGE_INTEGER**](../winnt/ns-winnt-large_integer-r1.md).

### -field Data

Any additional data. For more information, see Remarks.

## -remarks

**DISK_GEOMETRY_EX** is a variable-length structure composed of a [**DISK_GEOMETRY**](ns-winioctl-disk_geometry.md) structure followed by a [**DISK_PARTITION_INFO**](ns-winioctl-disk_partition_info.md) structure and a [**DISK_DETECTION_INFO**](ns-winioctl-disk_detection_info.md) structure. Because the detection information is not at a fixed location within the **DISK_GEOMETRY_EX** structure, use the following macro to access the **DISK_DETECTION_INFO** structure.

```cpp
PDISK_DETECTION_INFO DiskGeometryGetDetect(
  PDISK_GEOMETRY_EX Geometry
);
```

Similarly, use the following macro to access the [**DISK_PARTITION_INFO**](ns-winioctl-disk_partition_info.md) structure.

```cpp
PDISK_PARTITION_INFO DiskGeometryGetPartition(
  PDISK_GEOMETRY_EX Geometry
);
```

The information returned does not include the number of partitions nor the partition information contained in the [**DISK_PARTITION_INFO**](ns-winioctl-disk_partition_info.md) structure. To obtain this information, use the [**IOCTL_DISK_GET_DRIVE_LAYOUT_EX**](ni-winioctl-ioctl_disk_get_drive_layout_ex.md) control code.

## -see-also

[DISK_GEOMETRY](ns-winioctl-disk_geometry.md), [DISK_DETECTION_INFO](ns-winioctl-disk_detection_info.md), [DISK_PARTITION_INFO](ns-winioctl-disk_partition_info.md), [IOCTL_DISK_GET_DRIVE_GEOMETRY_EX](ni-winioctl-ioctl_disk_get_drive_geometry_ex.md)

