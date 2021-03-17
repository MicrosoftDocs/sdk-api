---
UID: NS:winioctl._DEVICE_COPY_OFFLOAD_DESCRIPTOR
title: DEVICE_COPY_OFFLOAD_DESCRIPTOR
description: Contains the copy offload capabilities for a storage device.
helpviewer_keywords: ["*PDEVICE_COPY_OFFLOAD_DESCRIPTOR","DEVICE_COPY_OFFLOAD_DESCRIPTOR","DEVICE_COPY_OFFLOAD_DESCRIPTOR structure [Files]","PDEVICE_COPY_OFFLOAD_DESCRIPTOR","PDEVICE_COPY_OFFLOAD_DESCRIPTOR structure pointer [Files]","fs.device_copy_offload_descriptor","winioctl/DEVICE_COPY_OFFLOAD_DESCRIPTOR","winioctl/PDEVICE_COPY_OFFLOAD_DESCRIPTOR"]
old-location: fs\device_copy_offload_descriptor.htm
tech.root: fs
ms.assetid: ff100db5-f244-4d34-8b55-9b6b21b9e382
ms.date: 12/05/2018
ms.keywords: '*PDEVICE_COPY_OFFLOAD_DESCRIPTOR, DEVICE_COPY_OFFLOAD_DESCRIPTOR, DEVICE_COPY_OFFLOAD_DESCRIPTOR structure [Files], PDEVICE_COPY_OFFLOAD_DESCRIPTOR, PDEVICE_COPY_OFFLOAD_DESCRIPTOR structure pointer [Files], fs.device_copy_offload_descriptor, winioctl/DEVICE_COPY_OFFLOAD_DESCRIPTOR, winioctl/PDEVICE_COPY_OFFLOAD_DESCRIPTOR'
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
targetos: Windows
req.typenames: DEVICE_COPY_OFFLOAD_DESCRIPTOR, *PDEVICE_COPY_OFFLOAD_DESCRIPTOR
req.redist: 
f1_keywords:
 - _DEVICE_COPY_OFFLOAD_DESCRIPTOR
 - winioctl/_DEVICE_COPY_OFFLOAD_DESCRIPTOR
 - PDEVICE_COPY_OFFLOAD_DESCRIPTOR
 - winioctl/PDEVICE_COPY_OFFLOAD_DESCRIPTOR
 - DEVICE_COPY_OFFLOAD_DESCRIPTOR
 - winioctl/DEVICE_COPY_OFFLOAD_DESCRIPTOR
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
 - DEVICE_COPY_OFFLOAD_DESCRIPTOR
---

# DEVICE_COPY_OFFLOAD_DESCRIPTOR structure


## -description

The 
   <b>DEVICE_COPY_OFFLOAD_DESCRIPTOR</b> 
   structure is one of the query result structures returned from an 
   <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> request. This 
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
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> request when the 
    <b>PropertyId</b> member of 
    <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a> is set to 
    <b>StorageDeviceCopyOffloadProperty</b>.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a>