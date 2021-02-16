---
UID: NS:winioctl._DISK_PERFORMANCE
title: DISK_PERFORMANCE
description: Provides disk performance information.
helpviewer_keywords: ["*PDISK_PERFORMANCE","DISK_PERFORMANCE","DISK_PERFORMANCE structure [Files]","PDISK_PERFORMANCE","PDISK_PERFORMANCE structure pointer [Files]","_win32_disk_performance_str","base.disk_performance_str","fs.disk_performance_str","winioctl/DISK_PERFORMANCE","winioctl/PDISK_PERFORMANCE"]
old-location: fs\disk_performance_str.htm
tech.root: fs
ms.assetid: 938ec37b-450e-4ebf-ad2b-9f1ac5f56112
ms.date: 12/05/2018
ms.keywords: '*PDISK_PERFORMANCE, DISK_PERFORMANCE, DISK_PERFORMANCE structure [Files], PDISK_PERFORMANCE, PDISK_PERFORMANCE structure pointer [Files], _win32_disk_performance_str, base.disk_performance_str, fs.disk_performance_str, winioctl/DISK_PERFORMANCE, winioctl/PDISK_PERFORMANCE'
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
req.typenames: DISK_PERFORMANCE, *PDISK_PERFORMANCE
req.redist: 
f1_keywords:
 - _DISK_PERFORMANCE
 - winioctl/_DISK_PERFORMANCE
 - PDISK_PERFORMANCE
 - winioctl/PDISK_PERFORMANCE
 - DISK_PERFORMANCE
 - winioctl/DISK_PERFORMANCE
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
 - DISK_PERFORMANCE
---

# DISK_PERFORMANCE structure


## -description

Provides disk performance information. It is used by the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_performance">IOCTL_DISK_PERFORMANCE</a> control code.

## -struct-fields

### -field BytesRead

The number of bytes read.

### -field BytesWritten

The number of bytes written.

### -field ReadTime

The time it takes to complete a read.

### -field WriteTime

The time it takes to complete a write.

### -field IdleTime

The idle time.

### -field ReadCount

The number of read operations.

### -field WriteCount

The number of write operations.

### -field QueueDepth

The depth of the queue.

### -field SplitCount

The cumulative count of I/Os that are associated I/Os. 

An associated I/O is a fragmented I/O, where multiple I/Os to a disk are required to fulfill the original logical I/O request. The most common example of this scenario is a file that is fragmented on a disk. The multiple I/Os are counted as split I/O counts.

### -field QueryTime

The system time stamp when a query for this structure is returned. 

Use this member to synchronize between the file system driver and a caller.

### -field StorageDeviceNumber

The unique number for a device that identifies it to the storage manager that is indicated in the <b>StorageManagerName</b> member.

### -field StorageManagerName

The name of the storage manager that controls this device. 

Examples of storage managers are "PhysDisk," "FTDISK," and "DMIO".

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_performance">IOCTL_DISK_PERFORMANCE</a>