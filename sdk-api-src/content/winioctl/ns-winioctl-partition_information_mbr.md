---
UID: NS:winioctl._PARTITION_INFORMATION_MBR
title: PARTITION_INFORMATION_MBR
description: Contains partition information specific to master boot record (MBR) disks.
helpviewer_keywords: ["*PPARTITION_INFORMATION_MBR","PARTITION_INFORMATION_MBR","PARTITION_INFORMATION_MBR structure [Files]","PPARTITION_INFORMATION_MBR","PPARTITION_INFORMATION_MBR structure pointer [Files]","_win32_partition_information_mbr_str","base.partition_information_mbr_str","fs.partition_information_mbr_str","winioctl/PARTITION_INFORMATION_MBR","winioctl/PPARTITION_INFORMATION_MBR"]
old-location: fs\partition_information_mbr_str.htm
tech.root: fs
ms.assetid: 5b74b06f-ef4c-44ab-95c6-49c050faf1f4
ms.date: 12/05/2018
ms.keywords: '*PPARTITION_INFORMATION_MBR, PARTITION_INFORMATION_MBR, PARTITION_INFORMATION_MBR structure [Files], PPARTITION_INFORMATION_MBR, PPARTITION_INFORMATION_MBR structure pointer [Files], _win32_partition_information_mbr_str, base.partition_information_mbr_str, fs.partition_information_mbr_str, winioctl/PARTITION_INFORMATION_MBR, winioctl/PPARTITION_INFORMATION_MBR'
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
req.typenames: PARTITION_INFORMATION_MBR, *PPARTITION_INFORMATION_MBR
req.redist: 
f1_keywords:
 - _PARTITION_INFORMATION_MBR
 - winioctl/_PARTITION_INFORMATION_MBR
 - PPARTITION_INFORMATION_MBR
 - winioctl/PPARTITION_INFORMATION_MBR
 - PARTITION_INFORMATION_MBR
 - winioctl/PARTITION_INFORMATION_MBR
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
 - PARTITION_INFORMATION_MBR
---

# PARTITION_INFORMATION_MBR structure


## -description

Contains partition information specific to master boot record (MBR) disks.

## -struct-fields

### -field PartitionType

The type of partition. For a list of values, see 
<a href="/windows/desktop/FileIO/disk-partition-types">Disk Partition Types</a>.

### -field BootIndicator

If the member is <b>TRUE</b>, the partition is a boot partition. When this structure is used with the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_partition_info_ex">IOCTL_DISK_SET_PARTITION_INFO_EX</a> control code, the value of this parameter is ignored.

### -field RecognizedPartition

If this member is <b>TRUE</b>, the partition is of a recognized type. When this structure is used with the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_partition_info_ex">IOCTL_DISK_SET_PARTITION_INFO_EX</a> control code, the value of this parameter is ignored.

### -field HiddenSectors

The number of hidden sectors to be allocated when the partition table is created.

### -field PartitionId

## -see-also

<a href="/windows/desktop/FileIO/file-system-recognition">File System Recognition</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info_ex">IOCTL_DISK_GET_PARTITION_INFO_EX</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_partition_info_ex">IOCTL_DISK_SET_PARTITION_INFO_EX</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_ex">PARTITION_INFORMATION_EX</a>