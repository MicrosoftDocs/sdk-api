---
UID: NS:winioctl._DRIVE_LAYOUT_INFORMATION_EX
title: DRIVE_LAYOUT_INFORMATION_EX
description: Contains extended information about a drive's partitions.
helpviewer_keywords: ["*PDRIVE_LAYOUT_INFORMATION_EX","DRIVE_LAYOUT_INFORMATION_EX","DRIVE_LAYOUT_INFORMATION_EX structure [Files]","PARTITION_STYLE_GPT","PARTITION_STYLE_MBR","PARTITION_STYLE_RAW","PDRIVE_LAYOUT_INFORMATION_EX","PDRIVE_LAYOUT_INFORMATION_EX structure pointer [Files]","_win32_drive_layout_information_ex_str","base.drive_layout_information_ex_str","fs.drive_layout_information_ex_str","winioctl/DRIVE_LAYOUT_INFORMATION_EX","winioctl/PDRIVE_LAYOUT_INFORMATION_EX"]
old-location: fs\drive_layout_information_ex_str.htm
tech.root: fs
ms.assetid: 381c87a8-fe40-4251-a4df-dddc9e2a126d
ms.date: 12/05/2018
ms.keywords: '*PDRIVE_LAYOUT_INFORMATION_EX, DRIVE_LAYOUT_INFORMATION_EX, DRIVE_LAYOUT_INFORMATION_EX structure [Files], PARTITION_STYLE_GPT, PARTITION_STYLE_MBR, PARTITION_STYLE_RAW, PDRIVE_LAYOUT_INFORMATION_EX, PDRIVE_LAYOUT_INFORMATION_EX structure pointer [Files], _win32_drive_layout_information_ex_str, base.drive_layout_information_ex_str, fs.drive_layout_information_ex_str, winioctl/DRIVE_LAYOUT_INFORMATION_EX, winioctl/PDRIVE_LAYOUT_INFORMATION_EX'
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
req.typenames: DRIVE_LAYOUT_INFORMATION_EX, *PDRIVE_LAYOUT_INFORMATION_EX
req.redist: 
f1_keywords:
 - _DRIVE_LAYOUT_INFORMATION_EX
 - winioctl/_DRIVE_LAYOUT_INFORMATION_EX
 - PDRIVE_LAYOUT_INFORMATION_EX
 - winioctl/PDRIVE_LAYOUT_INFORMATION_EX
 - DRIVE_LAYOUT_INFORMATION_EX
 - winioctl/DRIVE_LAYOUT_INFORMATION_EX
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
 - DRIVE_LAYOUT_INFORMATION_EX
---

# DRIVE_LAYOUT_INFORMATION_EX structure


## -description

Contains extended information about a drive's partitions.

## -struct-fields

### -field PartitionStyle

The style of the partitions on the drive enumerated by the [**PARTITION_STYLE**](ne-winioctl-partition_style.md) enumeration.

| Style | Value | Meaning |
| --- | --- | --- |
| **PARTITION_STYLE_MBR** | 0 | Master boot record (MBR) format.|
| **PARTITION_STYLE_GPT** | 1 | GUID Partition Table (GPT) format. |
| **PARTITION_STYLE_RAW** | 2 | Partition not formatted in either of the recognized formats—MBR or GPT. |

### -field PartitionCount

The number of partitions on the drive. On hard disks with the MBR layout, this value will always be a multiple of 4. Any partitions that are actually unused will have a partition type of **PARTITION_ENTRY_UNUSED** (0) set in the **PartitionType** member of the [**PARTITION_INFORMATION_MBR**](ns-winioctl-partition_information_mbr.md) structure of the **Mbr** member of the [**PARTITION_INFORMATION_EX**](ns-winioctl-partition_information_ex.md) structure of the **PartitionEntry** member of this structure.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Mbr

A [**DRIVE_LAYOUT_INFORMATION_MBR**](ns-winioctl-drive_layout_information_mbr.md) structure containing information about the master boot record type partitioning on the drive.

### -field DUMMYUNIONNAME.Gpt

A [**DRIVE_LAYOUT_INFORMATION_GPT**](ns-winioctl-drive_layout_information_gpt.md) structure containing information about the GUID disk partition type partitioning on the drive.

### -field PartitionEntry

A variable-sized array of [**PARTITION_INFORMATION_EX**](ns-winioctl-partition_information_ex.md) structures, one structure for each partition on the drive.

## -see-also

[DRIVE_LAYOUT_INFORMATION_GPT](ns-winioctl-drive_layout_information_gpt.md), [DRIVE_LAYOUT_INFORMATION_MBR](ns-winioctl-drive_layout_information_mbr.md), [IOCTL_DISK_GET_DRIVE_LAYOUT_EX](ni-winioctl-ioctl_disk_get_drive_layout_ex.md), [IOCTL_DISK_SET_DRIVE_LAYOUT_EX](ni-winioctl-ioctl_disk_set_drive_layout_ex.md), [PARTITION_INFORMATION_EX](ns-winioctl-partition_information_ex.md), [PARTITION_INFORMATION](ns-winioctl-partition_information.md)

