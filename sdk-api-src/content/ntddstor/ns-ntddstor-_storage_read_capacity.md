---
UID: NS:ntddstor._STORAGE_READ_CAPACITY
title: "_STORAGE_READ_CAPACITY"
author: windows-driver-content
description: Contains information about the size of a device. This is returned from the IOCTL_STORAGE_READ_CAPACITY control code.
old-location: base\storage_read_capacity.htm
old-project: DevIO
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PSTORAGE_READ_CAPACITY, PSTORAGE_READ_CAPACITY structure pointer, STORAGE_READ_CAPACITY, STORAGE_READ_CAPACITY structure, _STORAGE_READ_CAPACITY, base.storage_read_capacity, ntddstor/PSTORAGE_READ_CAPACITY, ntddstor/STORAGE_READ_CAPACITY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STORAGE_READ_CAPACITY, PSTORAGE_READ_CAPACITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntddstor.h
api_name:
-	STORAGE_READ_CAPACITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _STORAGE_READ_CAPACITY structure


## -description


Contains information about the size of a device. This is returned from the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/jj553708">IOCTL_STORAGE_READ_CAPACITY</a> control 
    code.


## -struct-fields




### -field Version

The version of this structure. The caller must set this member to 
      <code>sizeof(STORAGE_READ_CAPACITY)</code>.


### -field Size

The size of the data returned.


### -field BlockLength

The number of bytes per block.


### -field NumberOfBlocks

The total number of blocks on the disk.


### -field DiskLength

The disk size in bytes.


## -remarks



The header file Ntddstor.h is available in the Windows Driver Kit (WDK).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/jj553708">IOCTL_STORAGE_READ_CAPACITY</a>
 

 

