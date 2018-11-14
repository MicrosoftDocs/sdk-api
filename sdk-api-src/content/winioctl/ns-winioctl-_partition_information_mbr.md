---
UID: NS:winioctl._PARTITION_INFORMATION_MBR
title: "_PARTITION_INFORMATION_MBR"
author: windows-sdk-content
description: Contains partition information specific to master boot record (MBR) disks.
old-location: fs\partition_information_mbr_str.htm
tech.root: fileio
ms.assetid: 5b74b06f-ef4c-44ab-95c6-49c050faf1f4
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PPARTITION_INFORMATION_MBR, PARTITION_INFORMATION_MBR, PARTITION_INFORMATION_MBR structure [Files], PPARTITION_INFORMATION_MBR, PPARTITION_INFORMATION_MBR structure pointer [Files], _PARTITION_INFORMATION_MBR, _win32_partition_information_mbr_str, base.partition_information_mbr_str, fs.partition_information_mbr_str, winioctl/PARTITION_INFORMATION_MBR, winioctl/PPARTITION_INFORMATION_MBR"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - PARTITION_INFORMATION_MBR
product: Windows
targetos: Windows
req.typenames: PARTITION_INFORMATION_MBR, *PPARTITION_INFORMATION_MBR
req.redist: 
---

# _PARTITION_INFORMATION_MBR structure


## -description


Contains partition information specific to master boot record (MBR) disks.


## -struct-fields




### -field PartitionType

The type of partition. For a list of values, see 
<a href="https://msdn.microsoft.com/b2e15b93-a02b-4d6f-b242-b5ec9a30c97b">Disk Partition Types</a>.


### -field BootIndicator

If the member is <b>TRUE</b>, the partition is a boot partition. When this structure is used with the 
<a href="https://msdn.microsoft.com/6feec7a9-5b57-406b-bbea-04cf9cdaf56b">IOCTL_DISK_SET_PARTITION_INFO_EX</a> control code, the value of this parameter is ignored.


### -field RecognizedPartition

If this member is <b>TRUE</b>, the partition is of a recognized type. When this structure is used with the 
<a href="https://msdn.microsoft.com/6feec7a9-5b57-406b-bbea-04cf9cdaf56b">IOCTL_DISK_SET_PARTITION_INFO_EX</a> control code, the value of this parameter is ignored.


### -field HiddenSectors

The number of hidden sectors to be allocated when the partition table is created.


### -field PartitionId

 




## -see-also




<a href="https://msdn.microsoft.com/a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3">File System Recognition</a>



<a href="https://msdn.microsoft.com/f84f8be6-2b01-4a20-8669-cb1a55c32907">IOCTL_DISK_GET_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/6feec7a9-5b57-406b-bbea-04cf9cdaf56b">IOCTL_DISK_SET_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/3c88ebae-274e-403a-8f57-58fdf863f511">PARTITION_INFORMATION_EX</a>
 

 

