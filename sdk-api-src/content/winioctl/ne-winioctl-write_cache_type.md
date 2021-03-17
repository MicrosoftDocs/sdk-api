---
UID: NE:winioctl._WRITE_CACHE_TYPE
title: WRITE_CACHE_TYPE
description: Specifies the cache type.
helpviewer_keywords: ["WRITE_CACHE_TYPE","WRITE_CACHE_TYPE enumeration [Files]","WriteCacheTypeNone","WriteCacheTypeUnknown","WriteCacheTypeWriteBack","WriteCacheTypeWriteThrough","fs.write_cache_type","winioctl/WRITE_CACHE_TYPE","winioctl/WriteCacheTypeNone","winioctl/WriteCacheTypeUnknown","winioctl/WriteCacheTypeWriteBack","winioctl/WriteCacheTypeWriteThrough"]
old-location: fs\write_cache_type.htm
tech.root: fs
ms.assetid: fb861a65-5207-4af3-b994-0883febcbb0a
ms.date: 12/05/2018
ms.keywords: WRITE_CACHE_TYPE, WRITE_CACHE_TYPE enumeration [Files], WriteCacheTypeNone, WriteCacheTypeUnknown, WriteCacheTypeWriteBack, WriteCacheTypeWriteThrough, fs.write_cache_type, winioctl/WRITE_CACHE_TYPE, winioctl/WriteCacheTypeNone, winioctl/WriteCacheTypeUnknown, winioctl/WriteCacheTypeWriteBack, winioctl/WriteCacheTypeWriteThrough
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
req.typenames: WRITE_CACHE_TYPE
req.redist: 
f1_keywords:
 - _WRITE_CACHE_TYPE
 - winioctl/_WRITE_CACHE_TYPE
 - WRITE_CACHE_TYPE
 - winioctl/WRITE_CACHE_TYPE
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
 - WRITE_CACHE_TYPE
---

# WRITE_CACHE_TYPE enumeration


## -description

Specifies the cache type.

## -enum-fields

### -field WriteCacheTypeUnknown

The system cannot report the type of the write cache.

### -field WriteCacheTypeNone

The device does not have a write cache.

### -field WriteCacheTypeWriteBack

The device has a write-back cache.

### -field WriteCacheTypeWriteThrough

The device has a write-through cache.

## -remarks

There are two main types of write cache: *write back* and *write through*. With a write-back cache, the device does not copy cache data to nonvolatile media until absolutely necessary. This type of operation improves the performance of write operations. With a write-through cache, the device writes data to the cache and the media in parallel. This type of operation does not improve write performance, but it makes subsequent read operations faster.

The [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) control code reports a **WRITE_CACHE_TYPE** value in the [STORAGE_WRITE_CACHE_PROPERTY](ns-winioctl-storage_write_cache_property.md) structure.

## -see-also

* [Disk Management Enumeration Types](/windows/desktop/FileIO/disk-management-enumeration-types)
* [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md)
* [STORAGE_WRITE_CACHE_PROPERTY](ns-winioctl-storage_write_cache_property.md)