---
UID: NS:winioctl._DEVICE_COPY_OFFLOAD_DESCRIPTOR
title: "_DEVICE_COPY_OFFLOAD_DESCRIPTOR"
author: windows-sdk-content
description: Contains the copy offload capabilities for a storage device.
old-location: fs\device_copy_offload_descriptor.htm
tech.root: fileio
ms.assetid: ff100db5-f244-4d34-8b55-9b6b21b9e382
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDEVICE_COPY_OFFLOAD_DESCRIPTOR, DEVICE_COPY_OFFLOAD_DESCRIPTOR, DEVICE_COPY_OFFLOAD_DESCRIPTOR structure [Files], PDEVICE_COPY_OFFLOAD_DESCRIPTOR, PDEVICE_COPY_OFFLOAD_DESCRIPTOR structure pointer [Files], _DEVICE_COPY_OFFLOAD_DESCRIPTOR, fs.device_copy_offload_descriptor, winioctl/DEVICE_COPY_OFFLOAD_DESCRIPTOR, winioctl/PDEVICE_COPY_OFFLOAD_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
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
 - DEVICE_COPY_OFFLOAD_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: DEVICE_COPY_OFFLOAD_DESCRIPTOR, *PDEVICE_COPY_OFFLOAD_DESCRIPTOR
req.redist: 
---

# _DEVICE_COPY_OFFLOAD_DESCRIPTOR structure


## -description


The 
   <b>DEVICE_COPY_OFFLOAD_DESCRIPTOR</b> 
   structure is one of the query result structures returned from an 
   <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request. This 
   structure contains the copy offload capabilities for a storage device.


## -struct-fields




### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.


### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.


### -field MaximumTokenLifetime

The maximum lifetime of the token, in seconds.


### -field DefaultTokenLifetime

The default lifetime of the token, in seconds.


### -field MaximumTransferSize

The maximum transfer size, in bytes.


### -field OptimalTransferCount

The optimal transfer size, in bytes.


### -field MaximumDataDescriptors

The maximum number of data descriptors.


### -field MaximumTransferLengthPerDescriptor

The maximum transfer length, in blocks, per descriptor.


### -field OptimalTransferLengthPerDescriptor

The optimal transfer length per descriptor.


### -field OptimalTransferLengthGranularity

The granularity of the optimal transfer length, in blocks. Transfer lengths that are not an even multiple 
      of this length may be delayed.


### -field Reserved

Reserved.


## -remarks



This structure is returned from a 
    <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request when the 
    <b>PropertyId</b> member of 
    <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a> is set to 
    <b>StorageDeviceCopyOffloadProperty</b>.




## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>
 

 

