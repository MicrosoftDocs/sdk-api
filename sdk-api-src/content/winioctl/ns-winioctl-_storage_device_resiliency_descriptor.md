---
UID: NS:winioctl._STORAGE_DEVICE_RESILIENCY_DESCRIPTOR
title: "_STORAGE_DEVICE_RESILIENCY_DESCRIPTOR"
author: windows-driver-content
description: Reserved for system use.
old-location: fs\storage_device_resiliency_descriptor.htm
old-project: FileIO
ms.assetid: 7ef6d99a-3e2c-44de-ab08-260e8ddc02f4
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: PSTORAGE_DEVICE_RESILIENCY_DESCRIPTOR, PSTORAGE_DEVICE_RESILIENCY_DESCRIPTOR structure pointer [Files], STORAGE_DEVICE_RESILIENCY_DESCRIPTOR, STORAGE_DEVICE_RESILIENCY_DESCRIPTOR structure [Files], _STORAGE_DEVICE_RESILIENCY_DESCRIPTOR, fs.storage_device_resiliency_descriptor, winioctl/PSTORAGE_DEVICE_RESILIENCY_DESCRIPTOR, winioctl/STORAGE_DEVICE_RESILIENCY_DESCRIPTOR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STORAGE_DEVICE_RESILIENCY_DESCRIPTOR, PSTORAGE_DEVICE_RESILIENCY_DESCRIPTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	STORAGE_DEVICE_RESILIENCY_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_DEVICE_RESILIENCY_DESCRIPTOR structure


## -description


Reserved for system use.


## -struct-fields




### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure. Set to 
      <code>sizeof(STORAGE_DEVICE_RESILIENCY_DESCRIPTOR)</code>.


### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.


### -field NameOffset

Byte offset to the null-terminated ASCII string containing the resiliency properties Name. For devices with 
      no Name property, this will be zero.


### -field NumberOfLogicalCopies

Number of logical copies of data that are available.


### -field NumberOfPhysicalCopies

Number of complete copies of data that are stored.


### -field PhysicalDiskRedundancy

Number of disks that can fail without leading to data loss.


### -field NumberOfColumns

Number of columns in the storage device.


### -field Interleave

Size of a stripe unit of the storage device, in bytes. This is also referred to as the stripe width or 
      interleave of the storage device.


## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566997">STORAGE_PROPERTY_QUERY</a>
 

 

