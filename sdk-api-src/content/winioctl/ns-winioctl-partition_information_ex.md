---
UID: NS:winioctl._PARTITION_INFORMATION_EX
title: PARTITION_INFORMATION_EX
description: Contains partition information for standard AT-style master boot record (MBR) and Extensible Firmware Interface (EFI) disks.
helpviewer_keywords: ["*PPARTITION_INFORMATION_EX","PARTITION_INFORMATION_EX","PARTITION_INFORMATION_EX structure [Files]","_win32_partition_information_ex_str","base.partition_information_ex_str","fs.partition_information_ex_str","winioctl/PARTITION_INFORMATION_EX"]
old-location: fs\partition_information_ex_str.htm
tech.root: fs
ms.assetid: 3c88ebae-274e-403a-8f57-58fdf863f511
ms.date: 12/05/2018
ms.keywords: '*PPARTITION_INFORMATION_EX, PARTITION_INFORMATION_EX, PARTITION_INFORMATION_EX structure [Files], _win32_partition_information_ex_str, base.partition_information_ex_str, fs.partition_information_ex_str, winioctl/PARTITION_INFORMATION_EX'
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
req.typenames: PARTITION_INFORMATION_EX, *PPARTITION_INFORMATION_EX
req.redist: 
f1_keywords:
 - _PARTITION_INFORMATION_EX
 - winioctl/_PARTITION_INFORMATION_EX
 - PPARTITION_INFORMATION_EX
 - winioctl/PPARTITION_INFORMATION_EX
 - PARTITION_INFORMATION_EX
 - winioctl/PARTITION_INFORMATION_EX
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
 - PARTITION_INFORMATION_EX
---

# PARTITION_INFORMATION_EX structure


## -description

Contains partition information for standard <i>AT-style</i> master boot record (MBR) and Extensible Firmware Interface (EFI) disks.

## -struct-fields

### -field PartitionStyle

The format of the partition. For a list of values, see 
<a href="/windows/desktop/api/winioctl/ne-winioctl-partition_style">PARTITION_STYLE</a>.

### -field StartingOffset

The starting offset of the partition.

### -field PartitionLength

The size of the partition, in bytes.

### -field PartitionNumber

The number of the partition (1-based).

### -field RewritePartition

If this member is <b>TRUE</b>, the partition is rewritable. The value of this parameter should be set to <b>TRUE</b>.

### -field IsServicePartition

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Mbr

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_mbr">PARTITION_INFORMATION_MBR</a> structure that specifies partition information specific to master boot record (MBR) disks. The MBR partition format is the standard <i>AT-style</i> format.

### -field DUMMYUNIONNAME.Gpt

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_gpt">PARTITION_INFORMATION_GPT</a> structure that specifies partition information specific to GUID partition table (GPT) disks. The GPT format corresponds to the EFI partition format.

## -remarks

If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout">IOCTL_DISK_SET_DRIVE_LAYOUT</a>.

## -see-also

<a href="/windows/desktop/FileIO/file-system-recognition">File System Recognition</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info_ex">IOCTL_DISK_GET_PARTITION_INFO_EX</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_partition_info_ex">IOCTL_DISK_SET_PARTITION_INFO_EX</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_gpt">PARTITION_INFORMATION_GPT</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_mbr">PARTITION_INFORMATION_MBR</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-partition_style">PARTITION_STYLE</a>