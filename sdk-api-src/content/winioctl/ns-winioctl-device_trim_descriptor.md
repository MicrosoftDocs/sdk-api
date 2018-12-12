---
UID: NS:winioctl._DEVICE_TRIM_DESCRIPTOR
title: DEVICE_TRIM_DESCRIPTOR
author: windows-sdk-content
description: Used in conjunction with the IOCTL_STORAGE_QUERY_PROPERTY request to retrieve the trim descriptor data for a device.
old-location: fs\device_trim_descriptor.htm
tech.root: fileio
ms.assetid: 60b38d08-5869-442f-845b-b3d8667d069f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDEVICE_TRIM_DESCRIPTOR, DEVICE_TRIM_DESCRIPTOR, DEVICE_TRIM_DESCRIPTOR structure [Files], PDEVICE_TRIM_DESCRIPTOR, PDEVICE_TRIM_DESCRIPTOR structure pointer [Files], fs.device_trim_descriptor, winioctl/DEVICE_TRIM_DESCRIPTOR, winioctl/PDEVICE_TRIM_DESCRIPTOR"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DEVICE_TRIM_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: DEVICE_TRIM_DESCRIPTOR, *PDEVICE_TRIM_DESCRIPTOR
req.redist: 
---

# DEVICE_TRIM_DESCRIPTOR structure


## -description


Used in conjunction with the 
   <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request to 
   retrieve the trim descriptor data for a device.


## -struct-fields




### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.


### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.


### -field TrimEnabled

Specifies whether trim is enabled for the device.


## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>
 

 

