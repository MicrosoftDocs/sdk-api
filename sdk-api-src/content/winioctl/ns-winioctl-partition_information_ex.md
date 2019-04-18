---
UID: NS:winioctl._PARTITION_INFORMATION_EX
title: PARTITION_INFORMATION_EX (winioctl.h)
author: windows-sdk-content
description: Contains partition information for standard AT-style master boot record (MBR) and Extensible Firmware Interface (EFI) disks.
old-location: fs\partition_information_ex_str.htm
tech.root: FileIO
ms.assetid: 3c88ebae-274e-403a-8f57-58fdf863f511
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPARTITION_INFORMATION_EX, PARTITION_INFORMATION_EX, PARTITION_INFORMATION_EX structure [Files], _win32_partition_information_ex_str, base.partition_information_ex_str, fs.partition_information_ex_str, winioctl/PARTITION_INFORMATION_EX"
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
 - PARTITION_INFORMATION_EX
product: Windows
targetos: Windows
req.typenames: PARTITION_INFORMATION_EX, *PPARTITION_INFORMATION_EX
req.redist: 
ms.custom: 19H1
---

# PARTITION_INFORMATION_EX structure


## -description


Contains partition information for standard <i>AT-style</i> master boot record (MBR) and Extensible Firmware Interface (EFI) disks.


## -struct-fields




### -field PartitionStyle

The format of the partition. For a list of values, see 
<a href="https://msdn.microsoft.com/254e4ea1-d0c8-4033-b8af-e5dbfb7c7da8">PARTITION_STYLE</a>.


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
<a href="https://msdn.microsoft.com/5b74b06f-ef4c-44ab-95c6-49c050faf1f4">PARTITION_INFORMATION_MBR</a> structure that specifies partition information specific to master boot record (MBR) disks. The MBR partition format is the standard <i>AT-style</i> format.


### -field DUMMYUNIONNAME.Gpt

A 
<a href="https://msdn.microsoft.com/373b4eb3-af6d-4112-9787-f14c19972189">PARTITION_INFORMATION_GPT</a> structure that specifies partition information specific to GUID partition table (GPT) disks. The GPT format corresponds to the EFI partition format.


## -remarks



If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of <a href="https://msdn.microsoft.com/8cace6a5-666a-4d35-a557-6bf0564dbe58">IOCTL_DISK_SET_DRIVE_LAYOUT</a>.




## -see-also




<a href="https://msdn.microsoft.com/a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3">File System Recognition</a>



<a href="https://msdn.microsoft.com/f84f8be6-2b01-4a20-8669-cb1a55c32907">IOCTL_DISK_GET_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/6feec7a9-5b57-406b-bbea-04cf9cdaf56b">IOCTL_DISK_SET_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/373b4eb3-af6d-4112-9787-f14c19972189">PARTITION_INFORMATION_GPT</a>



<a href="https://msdn.microsoft.com/5b74b06f-ef4c-44ab-95c6-49c050faf1f4">PARTITION_INFORMATION_MBR</a>



<a href="https://msdn.microsoft.com/254e4ea1-d0c8-4033-b8af-e5dbfb7c7da8">PARTITION_STYLE</a>
 

 

