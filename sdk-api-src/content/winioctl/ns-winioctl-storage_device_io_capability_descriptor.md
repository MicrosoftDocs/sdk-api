---
UID: NS:winioctl._STORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR
title: STORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR (winioctl.h)
author: windows-sdk-content
description: The output buffer for the StorageDeviceIoCapabilityProperty as defined in STORAGE_PROPERTY_ID.
old-location: fs\storage_device_io_capability_descriptor.htm
tech.root: FileIO
ms.assetid: E9AAE295-091C-4DF4-9EBD-0B8AD6C48F9C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSTORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR, PSTORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR, PSTORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR structure pointer [Files], STORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR, STORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR structure [Files], fs.storage_device_io_capability_descriptor, winioctl/PSTORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR, winioctl/STORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR"
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
 - winioctl.h
api_name:
 - STORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: STORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR, *PSTORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR
req.redist: 
---

# STORAGE_DEVICE_IO_CAPABILITY_DESCRIPTOR structure


## -description


The output buffer for the StorageDeviceIoCapabilityProperty as defined in <a href="https://msdn.microsoft.com/9747be01-7c70-4697-97f7-e3830b54ba0a">STORAGE_PROPERTY_ID</a>.


## -struct-fields




### -field Version

The version of this structure. The Size serves as the version.


### -field Size

The size of this structure.


### -field LunMaxIoCount

The logical unit number (LUN) max outstanding I/O count.


### -field AdapterMaxIoCount

The adapter max outstanding I/O count.

