---
UID: NS:winioctl._DISK_GROW_PARTITION
title: DISK_GROW_PARTITION
author: windows-sdk-content
description: Contains information used to increase the size of a partition.
old-location: fs\disk_grow_partition_str.htm
tech.root: FileIO
ms.assetid: 17ff8bbb-45a6-4ddd-a871-8519500c03a9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDISK_GROW_PARTITION, DISK_GROW_PARTITION, DISK_GROW_PARTITION structure [Files], PDISK_GROW_PARTITION, PDISK_GROW_PARTITION structure pointer [Files], base.disk_grow_partition_str, fs.disk_grow_partition_str, winioctl/DISK_GROW_PARTITION, winioctl/PDISK_GROW_PARTITION"
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
 - DISK_GROW_PARTITION
product: Windows
targetos: Windows
req.typenames: DISK_GROW_PARTITION, *PDISK_GROW_PARTITION
req.redist: 
---

# DISK_GROW_PARTITION structure


## -description


Contains information used to increase the size of a partition.This structure is used by the <a href="https://msdn.microsoft.com/bbcb0bee-a507-4abb-83df-328f3aa6caaa">IOCTL_DISK_GROW_PARTITION</a> control code.


## -struct-fields




### -field PartitionNumber

The identifier of the partition to be enlarged.


### -field BytesToGrow

The number of bytes by which the partition is to be enlarged (positive value) or reduced (negative value). Note that this value is not the new size of the partition.


## -see-also




<a href="https://msdn.microsoft.com/bbcb0bee-a507-4abb-83df-328f3aa6caaa">IOCTL_DISK_GROW_PARTITION</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>
 

 

