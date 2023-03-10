---
UID: NE:winioctl._WRITE_THROUGH
title: WRITE_THROUGH
description: Specifies whether a storage device supports write-through caching.
helpviewer_keywords: ["WRITE_THROUGH","WRITE_THROUGH enumeration [Files]","WriteThroughNotSupported","WriteThroughSupported","WriteThroughUnknown","fs.write_through","winioctl/WRITE_THROUGH","winioctl/WriteThroughNotSupported","winioctl/WriteThroughSupported","winioctl/WriteThroughUnknown"]
old-location: fs\write_through.htm
tech.root: fs
ms.assetid: 8bb26be1-ad02-4cf0-8505-021f922f34bf
ms.date: 12/05/2018
ms.keywords: WRITE_THROUGH, WRITE_THROUGH enumeration [Files], WriteThroughNotSupported, WriteThroughSupported, WriteThroughUnknown, fs.write_through, winioctl/WRITE_THROUGH, winioctl/WriteThroughNotSupported, winioctl/WriteThroughSupported, winioctl/WriteThroughUnknown
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WRITE_THROUGH
req.redist: 
f1_keywords:
 - _WRITE_THROUGH
 - winioctl/_WRITE_THROUGH
 - WRITE_THROUGH
 - winioctl/WRITE_THROUGH
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
 - WRITE_THROUGH
---

# WRITE_THROUGH enumeration


## -description

Specifies whether a storage device supports write-through caching.

## -enum-fields

### -field WriteThroughUnknown

Indicates that no information is available about the write-through capabilities of the device.

### -field WriteThroughNotSupported

Indicates that the device does not support write-through caching.

### -field WriteThroughSupported

Indicates that the device supports write-through caching.

## -remarks

The [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) control code reports this value in the [STORAGE_WRITE_CACHE_PROPERTY](ns-winioctl-storage_write_cache_property.md) structure.

## -see-also

* [Disk Management Enumeration Types](/windows/desktop/FileIO/disk-management-enumeration-types)
* [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md)
* [STORAGE_WRITE_CACHE_PROPERTY](ns-winioctl-storage_write_cache_property.md)