---
UID: NS:winioctl._DISK_PARTITION_INFO
title: DISK_PARTITION_INFO
description: Contains the disk partition information.
helpviewer_keywords: ["*PDISK_PARTITION_INFO","DISK_PARTITION_INFO","DISK_PARTITION_INFO structure [Files]","PDISK_PARTITION_INFO","PDISK_PARTITION_INFO structure pointer [Files]","_win32_disk_partition_info_str","base.disk_partition_info_str","fs.disk_partition_info_str","winioctl/DISK_PARTITION_INFO","winioctl/PDISK_PARTITION_INFO"]
old-location: fs\disk_partition_info_str.htm
tech.root: fs
ms.assetid: 34a086fc-72ea-46ed-adb3-c084abcb3c74
ms.date: 12/05/2018
ms.keywords: '*PDISK_PARTITION_INFO, DISK_PARTITION_INFO, DISK_PARTITION_INFO structure [Files], PDISK_PARTITION_INFO, PDISK_PARTITION_INFO structure pointer [Files], _win32_disk_partition_info_str, base.disk_partition_info_str, fs.disk_partition_info_str, winioctl/DISK_PARTITION_INFO, winioctl/PDISK_PARTITION_INFO'
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
req.typenames: DISK_PARTITION_INFO, *PDISK_PARTITION_INFO
req.redist: 
f1_keywords:
 - _DISK_PARTITION_INFO
 - winioctl/_DISK_PARTITION_INFO
 - PDISK_PARTITION_INFO
 - winioctl/PDISK_PARTITION_INFO
 - DISK_PARTITION_INFO
 - winioctl/DISK_PARTITION_INFO
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
 - DISK_PARTITION_INFO
---

# DISK_PARTITION_INFO structure


## -description

Contains the disk partition information.

## -struct-fields

### -field SizeOfPartitionInfo

The size of this structure, in bytes.

### -field PartitionStyle

The format of a partition.

For more information, see [PARTITION_STYLE](ne-winioctl-partition_style.md).

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Mbr

If **PartitionStyle** is **PARTITION_STYLE_MBR** (0), the union is a structure that contains information for a master boot record partition, which includes a disk signature and a checksum.

### -field DUMMYUNIONNAME.Mbr.Signature

MBR signature of the partition.

### -field DUMMYUNIONNAME.Mbr.CheckSum

### -field DUMMYUNIONNAME.Gpt

If **PartitionStyle** is **PARTITION_STYLE_GPT** (1), the union is a structure that contains information for a **GUID** partition table partition, which includes a disk identifier (**GUID**).

### -field DUMMYUNIONNAME.Gpt.DiskId

**GUID** of the GPT partition.

## -see-also

[DISK_GEOMETRY_EX](ns-winioctl-disk_geometry_ex.md), [PARTITION_STYLE](ne-winioctl-partition_style.md)

