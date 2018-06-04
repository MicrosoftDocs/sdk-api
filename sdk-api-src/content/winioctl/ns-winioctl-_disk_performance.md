---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DISK_PERFORMANCE structure


## -description


Provides disk performance information. It is used by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560388">IOCTL_DISK_PERFORMANCE</a> control code.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560388">IOCTL_DISK_PERFORMANCE</a>
 

 

