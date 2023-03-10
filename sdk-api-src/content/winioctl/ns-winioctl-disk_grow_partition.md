---
UID: NS:winioctl._DISK_GROW_PARTITION
title: DISK_GROW_PARTITION
description: Contains information used to increase the size of a partition.
helpviewer_keywords: ["*PDISK_GROW_PARTITION","DISK_GROW_PARTITION","DISK_GROW_PARTITION structure [Files]","PDISK_GROW_PARTITION","PDISK_GROW_PARTITION structure pointer [Files]","base.disk_grow_partition_str","fs.disk_grow_partition_str","winioctl/DISK_GROW_PARTITION","winioctl/PDISK_GROW_PARTITION"]
old-location: fs\disk_grow_partition_str.htm
tech.root: fs
ms.assetid: 17ff8bbb-45a6-4ddd-a871-8519500c03a9
ms.date: 12/05/2018
ms.keywords: '*PDISK_GROW_PARTITION, DISK_GROW_PARTITION, DISK_GROW_PARTITION structure [Files], PDISK_GROW_PARTITION, PDISK_GROW_PARTITION structure pointer [Files], base.disk_grow_partition_str, fs.disk_grow_partition_str, winioctl/DISK_GROW_PARTITION, winioctl/PDISK_GROW_PARTITION'
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
req.typenames: DISK_GROW_PARTITION, *PDISK_GROW_PARTITION
req.redist: 
f1_keywords:
 - _DISK_GROW_PARTITION
 - winioctl/_DISK_GROW_PARTITION
 - PDISK_GROW_PARTITION
 - winioctl/PDISK_GROW_PARTITION
 - DISK_GROW_PARTITION
 - winioctl/DISK_GROW_PARTITION
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
 - DISK_GROW_PARTITION
---

# DISK_GROW_PARTITION structure


## -description

Contains information used to increase the size of a partition.This structure is used by the <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_grow_partition">IOCTL_DISK_GROW_PARTITION</a> control code.

## -struct-fields

### -field PartitionNumber

The identifier of the partition to be enlarged.

### -field BytesToGrow

The number of bytes by which the partition is to be enlarged (positive value) or reduced (negative value). Note that this value is not the new size of the partition.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_grow_partition">IOCTL_DISK_GROW_PARTITION</a>



<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>