---
UID: NS:winioctl._STORAGE_DEVICE_ID_DESCRIPTOR
title: STORAGE_DEVICE_ID_DESCRIPTOR
description: Used with the IOCTL_STORAGE_QUERY_PROPERTY control code request to retrieve the device ID descriptor data for a device.
helpviewer_keywords: ["*PSTORAGE_DEVICE_ID_DESCRIPTOR","PSTORAGE_DEVICE_ID_DESCRIPTOR","PSTORAGE_DEVICE_ID_DESCRIPTOR structure pointer [Files]","STORAGE_DEVICE_ID_DESCRIPTOR","STORAGE_DEVICE_ID_DESCRIPTOR structure [Files]","fs.storage_device_id_descriptor","winioctl/PSTORAGE_DEVICE_ID_DESCRIPTOR","winioctl/STORAGE_DEVICE_ID_DESCRIPTOR"]
old-location: fs\storage_device_id_descriptor.htm
tech.root: fs
ms.assetid: 67b346fd-8976-4cd7-bb2f-a44ef6d56bc4
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_DEVICE_ID_DESCRIPTOR, PSTORAGE_DEVICE_ID_DESCRIPTOR, PSTORAGE_DEVICE_ID_DESCRIPTOR structure pointer [Files], STORAGE_DEVICE_ID_DESCRIPTOR, STORAGE_DEVICE_ID_DESCRIPTOR structure [Files], fs.storage_device_id_descriptor, winioctl/PSTORAGE_DEVICE_ID_DESCRIPTOR, winioctl/STORAGE_DEVICE_ID_DESCRIPTOR'
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
req.typenames: STORAGE_DEVICE_ID_DESCRIPTOR, *PSTORAGE_DEVICE_ID_DESCRIPTOR
req.redist: 
f1_keywords:
 - _STORAGE_DEVICE_ID_DESCRIPTOR
 - winioctl/_STORAGE_DEVICE_ID_DESCRIPTOR
 - PSTORAGE_DEVICE_ID_DESCRIPTOR
 - winioctl/PSTORAGE_DEVICE_ID_DESCRIPTOR
 - STORAGE_DEVICE_ID_DESCRIPTOR
 - winioctl/STORAGE_DEVICE_ID_DESCRIPTOR
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
 - STORAGE_DEVICE_ID_DESCRIPTOR
---

# STORAGE_DEVICE_ID_DESCRIPTOR structure


## -description

Used with the 
   <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control code 
   request to retrieve the device ID descriptor data for a device.

## -struct-fields

### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.

### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.

### -field NumberOfIdentifiers

Contains the number of identifiers reported by the device in the <b>Identifiers</b> array.

### -field Identifiers

Contains a variable-length array of identification descriptors.

## -remarks

The device ID descriptor consists of an array of device IDs taken from the SCSI-3 vital product data (VPD) 
    page 0x83 that was retrieved during discovery.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_adapter_descriptor">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_descriptor_header">STORAGE_DESCRIPTOR_HEADER</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor">STORAGE_DEVICE_DESCRIPTOR</a>