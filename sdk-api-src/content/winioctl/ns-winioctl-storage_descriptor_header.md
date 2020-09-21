---
UID: NS:winioctl._STORAGE_DESCRIPTOR_HEADER
title: STORAGE_DESCRIPTOR_HEADER
description: Used in conjunction with the IOCTL_STORAGE_QUERY_PROPERTY control code to retrieve the properties of a storage device or adapter.
helpviewer_keywords: ["*PSTORAGE_DESCRIPTOR_HEADER","PSTORAGE_DESCRIPTOR_HEADER","PSTORAGE_DESCRIPTOR_HEADER structure pointer [Files]","STORAGE_DESCRIPTOR_HEADER","STORAGE_DESCRIPTOR_HEADER structure [Files]","fs.storage_descriptor_header","winioctl/PSTORAGE_DESCRIPTOR_HEADER","winioctl/STORAGE_DESCRIPTOR_HEADER"]
old-location: fs\storage_descriptor_header.htm
tech.root: fs
ms.assetid: f98e53d5-45cb-4c3f-b04d-8eecd98655d2
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_DESCRIPTOR_HEADER, PSTORAGE_DESCRIPTOR_HEADER, PSTORAGE_DESCRIPTOR_HEADER structure pointer [Files], STORAGE_DESCRIPTOR_HEADER, STORAGE_DESCRIPTOR_HEADER structure [Files], fs.storage_descriptor_header, winioctl/PSTORAGE_DESCRIPTOR_HEADER, winioctl/STORAGE_DESCRIPTOR_HEADER'
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
req.typenames: STORAGE_DESCRIPTOR_HEADER, *PSTORAGE_DESCRIPTOR_HEADER
req.redist: 
f1_keywords:
 - _STORAGE_DESCRIPTOR_HEADER
 - winioctl/_STORAGE_DESCRIPTOR_HEADER
 - PSTORAGE_DESCRIPTOR_HEADER
 - winioctl/PSTORAGE_DESCRIPTOR_HEADER
 - STORAGE_DESCRIPTOR_HEADER
 - winioctl/STORAGE_DESCRIPTOR_HEADER
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
 - STORAGE_DESCRIPTOR_HEADER
---

# STORAGE_DESCRIPTOR_HEADER structure


## -description

Used in conjunction with the 
   <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control code to 
   retrieve the properties of a storage device or adapter.

## -struct-fields

### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.

### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.

## -remarks

The data retrieved by 
     <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> is reported in 
     the buffer immediately following this structure.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-device_seek_penalty_descriptor">DEVICE_SEEK_PENALTY_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-device_trim_descriptor">DEVICE_TRIM_DESCRIPTOR</a>



<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/win32/api/winioctl/ns-winioctl-storage_access_alignment_descriptor">STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_adapter_descriptor">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor">STORAGE_DEVICE_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_device_id_descriptor">STORAGE_DEVICE_ID_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_miniport_descriptor">STORAGE_MINIPORT_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_write_cache_property">STORAGE_WRITE_CACHE_PROPERTY</a>