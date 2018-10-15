---
UID: NS:winioctl._DEVICE_WRITE_AGGREGATION_DESCRIPTOR
title: "_DEVICE_WRITE_AGGREGATION_DESCRIPTOR"
author: windows-sdk-content
description: Reserved for system use.
old-location: fs\device_write_aggregation_descriptor.htm
tech.root: FileIO
ms.assetid: 124f05bc-6c3f-4778-9cc0-5a55891cb141
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*PDEVICE_WRITE_AGGREGATION_DESCRIPTOR, DEVICE_WRITE_AGGREGATION_DESCRIPTOR, DEVICE_WRITE_AGGREGATION_DESCRIPTOR structure [Files], PDEVICE_WRITE_AGGREGATION_DESCRIPTOR, PDEVICE_WRITE_AGGREGATION_DESCRIPTOR structure pointer [Files], _DEVICE_WRITE_AGGREGATION_DESCRIPTOR, fs.device_write_aggregation_descriptor, winioctl/DEVICE_WRITE_AGGREGATION_DESCRIPTOR, winioctl/PDEVICE_WRITE_AGGREGATION_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DEVICE_WRITE_AGGREGATION_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: DEVICE_WRITE_AGGREGATION_DESCRIPTOR, *PDEVICE_WRITE_AGGREGATION_DESCRIPTOR
req.redist: 
---

# _DEVICE_WRITE_AGGREGATION_DESCRIPTOR structure


## -description


Reserved for system use.


## -struct-fields




### -field Version

Contains the size, in bytes, of this structure. The value of this member will change as members are added 
      to the structure.


### -field Size

Specifies the total size of the descriptor, in bytes.


### -field BenefitsFromWriteAggregation

<b>TRUE</b> if the device benefits from write aggregation.


## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>
 

 

