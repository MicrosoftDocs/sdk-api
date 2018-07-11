---
UID: NS:winioctl._PARTITION_INFORMATION
title: "_PARTITION_INFORMATION"
author: windows-sdk-content
description: Contains information about a disk partition.
old-location: fs\partition_information_str.htm
old-project: fileio
ms.assetid: 2c8fa83a-0694-4e17-a9e4-87f839a0d458
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: "*PPARTITION_INFORMATION, PARTITION_INFORMATION, PARTITION_INFORMATION structure [Files], PPARTITION_INFORMATION, PPARTITION_INFORMATION structure pointer [Files], _PARTITION_INFORMATION, _win32_partition_information_str, base.partition_information_str, fs.partition_information_str, winioctl/PARTITION_INFORMATION, winioctl/PPARTITION_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PARTITION_INFORMATION, *PPARTITION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - PARTITION_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _PARTITION_INFORMATION structure


## -description


Contains information about a disk partition.
<div class="alert"><b>Note</b>  <b>PARTITION_INFORMATION</b> has been superseded by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563754">PARTITION_INFORMATION_EX</a> structure.</div><div> </div>

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
<a href="https://msdn.microsoft.com/b2e15b93-a02b-4d6f-b242-b5ec9a30c97b">Disk Partition Types</a>.


### -field BootIndicator

If this member is <b>TRUE</b>, the partition is bootable.


### -field RecognizedPartition

If this member is <b>TRUE</b>, the partition is of a recognized type.


### -field RewritePartition

If this member is <b>TRUE</b>, the partition information has changed. When you change a partition (with 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560408">IOCTL_DISK_SET_DRIVE_LAYOUT</a>), the system uses this member to determine which partitions have changed and need their information rewritten.


## -remarks



If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of <a href="https://msdn.microsoft.com/library/windows/hardware/ff560408">IOCTL_DISK_SET_DRIVE_LAYOUT</a>.




## -see-also




<a href="https://msdn.microsoft.com/a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3">File System Recognition</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560361">IOCTL_DISK_GET_DRIVE_LAYOUT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560373">IOCTL_DISK_GET_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560408">IOCTL_DISK_SET_DRIVE_LAYOUT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560413">IOCTL_DISK_SET_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563754">PARTITION_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563773">PARTITION_STYLE</a>
 

 

