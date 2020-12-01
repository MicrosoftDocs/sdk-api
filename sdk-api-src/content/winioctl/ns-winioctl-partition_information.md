---
UID: NS:winioctl._PARTITION_INFORMATION
title: PARTITION_INFORMATION
description: Contains information about a disk partition.
helpviewer_keywords: ["*PPARTITION_INFORMATION","PARTITION_INFORMATION","PARTITION_INFORMATION structure [Files]","PPARTITION_INFORMATION","PPARTITION_INFORMATION structure pointer [Files]","_win32_partition_information_str","base.partition_information_str","fs.partition_information_str","winioctl/PARTITION_INFORMATION","winioctl/PPARTITION_INFORMATION"]
old-location: fs\partition_information_str.htm
tech.root: fs
ms.assetid: 2c8fa83a-0694-4e17-a9e4-87f839a0d458
ms.date: 12/05/2018
ms.keywords: '*PPARTITION_INFORMATION, PARTITION_INFORMATION, PARTITION_INFORMATION structure [Files], PPARTITION_INFORMATION, PPARTITION_INFORMATION structure pointer [Files], _win32_partition_information_str, base.partition_information_str, fs.partition_information_str, winioctl/PARTITION_INFORMATION, winioctl/PPARTITION_INFORMATION'
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
req.typenames: PARTITION_INFORMATION, *PPARTITION_INFORMATION
req.redist: 
f1_keywords:
 - _PARTITION_INFORMATION
 - winioctl/_PARTITION_INFORMATION
 - PPARTITION_INFORMATION
 - winioctl/PPARTITION_INFORMATION
 - PARTITION_INFORMATION
 - winioctl/PARTITION_INFORMATION
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
 - PARTITION_INFORMATION
---

# PARTITION_INFORMATION structure


## -description

Contains information about a disk partition.
<div class="alert"><b>Note</b>  <b>PARTITION_INFORMATION</b> has been superseded by the 
<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_ex">PARTITION_INFORMATION_EX</a> structure.</div><div> </div>

## -struct-fields

### -field StartingOffset

The starting offset of the partition.

### -field PartitionLength

The length of the partition, in bytes.

### -field HiddenSectors

The number of hidden sectors in the partition.

### -field PartitionNumber

The number of the partition (1-based).

### -field PartitionType

The type of partition. For a list of values, see 
<a href="/windows/desktop/FileIO/disk-partition-types">Disk Partition Types</a>.

### -field BootIndicator

If this member is <b>TRUE</b>, the partition is bootable.

### -field RecognizedPartition

If this member is <b>TRUE</b>, the partition is of a recognized type.

### -field RewritePartition

If this member is <b>TRUE</b>, the partition information has changed. When you change a partition (with 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout">IOCTL_DISK_SET_DRIVE_LAYOUT</a>), the system uses this member to determine which partitions have changed and need their information rewritten.

## -remarks

If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout">IOCTL_DISK_SET_DRIVE_LAYOUT</a>.

## -see-also

<a href="/windows/desktop/FileIO/file-system-recognition">File System Recognition</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout">IOCTL_DISK_GET_DRIVE_LAYOUT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info">IOCTL_DISK_GET_PARTITION_INFO</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout">IOCTL_DISK_SET_DRIVE_LAYOUT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_partition_info">IOCTL_DISK_SET_PARTITION_INFO</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_ex">PARTITION_INFORMATION_EX</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-partition_style">PARTITION_STYLE</a>