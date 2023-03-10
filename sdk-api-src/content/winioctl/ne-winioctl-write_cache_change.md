---
UID: NE:winioctl._WRITE_CACHE_CHANGE
title: WRITE_CACHE_CHANGE
description: Indicates whether the write cache features of a device are changeable.
helpviewer_keywords: ["WRITE_CACHE_CHANGE","WRITE_CACHE_CHANGE enumeration [Files]","WriteCacheChangeUnknown","WriteCacheChangeable","WriteCacheNotChangeable","fs.write_cache_change","winioctl/WRITE_CACHE_CHANGE","winioctl/WriteCacheChangeUnknown","winioctl/WriteCacheChangeable","winioctl/WriteCacheNotChangeable"]
old-location: fs\write_cache_change.htm
tech.root: fs
ms.assetid: a6974092-fa4f-4524-96ec-b4fad0b8c5ea
ms.date: 12/05/2018
ms.keywords: WRITE_CACHE_CHANGE, WRITE_CACHE_CHANGE enumeration [Files], WriteCacheChangeUnknown, WriteCacheChangeable, WriteCacheNotChangeable, fs.write_cache_change, winioctl/WRITE_CACHE_CHANGE, winioctl/WriteCacheChangeUnknown, winioctl/WriteCacheChangeable, winioctl/WriteCacheNotChangeable
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
req.typenames: WRITE_CACHE_CHANGE
req.redist: 
f1_keywords:
 - _WRITE_CACHE_CHANGE
 - winioctl/_WRITE_CACHE_CHANGE
 - WRITE_CACHE_CHANGE
 - winioctl/WRITE_CACHE_CHANGE
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
 - WRITE_CACHE_CHANGE
---

# WRITE_CACHE_CHANGE enumeration


## -description

Indicates whether the write cache features of a device are changeable.

## -enum-fields

### -field WriteCacheChangeUnknown

The system cannot report the write cache change capability of the device.

### -field WriteCacheNotChangeable

Host software cannot change the characteristics of the device's write cache.

### -field WriteCacheChangeable

Host software can change the characteristics of the device's write cache.

## -remarks

The [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) request returns a **WRITE_CACHE_CHANGE** value in the [STORAGE_WRITE_CACHE_PROPERTY](ns-winioctl-storage_write_cache_property.md) structure.

## -see-also

* [Disk Management Enumeration Types](/windows/desktop/FileIO/disk-management-enumeration-types)
* [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md)
* [STORAGE_WRITE_CACHE_PROPERTY](ns-winioctl-storage_write_cache_property.md)