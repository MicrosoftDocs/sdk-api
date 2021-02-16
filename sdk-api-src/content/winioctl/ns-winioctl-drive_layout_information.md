---
UID: NS:winioctl._DRIVE_LAYOUT_INFORMATION
title: DRIVE_LAYOUT_INFORMATION
description: Contains information about the partitions of a drive.
helpviewer_keywords: ["*PDRIVE_LAYOUT_INFORMATION","DRIVE_LAYOUT_INFORMATION","DRIVE_LAYOUT_INFORMATION structure [Files]","PDRIVE_LAYOUT_INFORMATION","PDRIVE_LAYOUT_INFORMATION structure pointer [Files]","_win32_drive_layout_information_str","base.drive_layout_information_str","fs.drive_layout_information_str","winioctl/DRIVE_LAYOUT_INFORMATION","winioctl/PDRIVE_LAYOUT_INFORMATION"]
old-location: fs\drive_layout_information_str.htm
tech.root: fs
ms.assetid: e67ccaa7-a735-4695-8385-28f57b41821c
ms.date: 12/05/2018
ms.keywords: '*PDRIVE_LAYOUT_INFORMATION, DRIVE_LAYOUT_INFORMATION, DRIVE_LAYOUT_INFORMATION structure [Files], PDRIVE_LAYOUT_INFORMATION, PDRIVE_LAYOUT_INFORMATION structure pointer [Files], _win32_drive_layout_information_str, base.drive_layout_information_str, fs.drive_layout_information_str, winioctl/DRIVE_LAYOUT_INFORMATION, winioctl/PDRIVE_LAYOUT_INFORMATION'
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
req.typenames: DRIVE_LAYOUT_INFORMATION, *PDRIVE_LAYOUT_INFORMATION
req.redist: 
f1_keywords:
 - _DRIVE_LAYOUT_INFORMATION
 - winioctl/_DRIVE_LAYOUT_INFORMATION
 - PDRIVE_LAYOUT_INFORMATION
 - winioctl/PDRIVE_LAYOUT_INFORMATION
 - DRIVE_LAYOUT_INFORMATION
 - winioctl/DRIVE_LAYOUT_INFORMATION
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
 - DRIVE_LAYOUT_INFORMATION
---

# DRIVE_LAYOUT_INFORMATION structure


## -description

Contains information about the partitions of a drive.

> [!NOTE]
> **DRIVE_LAYOUT_INFORMATION** is superseded [**DRIVE_LAYOUT_INFORMATION_EX**](ns-winioctl-drive_layout_information_ex.md) structure.

## -struct-fields

### -field PartitionCount

The number of partitions on a drive.

On disks with the MBR layout, this value is always a multiple of 4. Any partitions that are unused have a partition type of **PARTITION_ENTRY_UNUSED** (0).

### -field Signature

The drive signature value.

### -field PartitionEntry

A variable-sized array of [**PARTITION_INFORMATION**](ns-winioctl-partition_information.md) structures, one structure for each partition on a drive.

## -see-also

[DRIVE_LAYOUT_INFORMATION_EX](ns-winioctl-drive_layout_information_ex.md), [IOCTL_DISK_GET_DRIVE_LAYOUT](ni-winioctl-ioctl_disk_get_drive_layout.md), [IOCTL_DISK_SET_DRIVE_LAYOUT](ni-winioctl-ioctl_disk_set_drive_layout.md)

