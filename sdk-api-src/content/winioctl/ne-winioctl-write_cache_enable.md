---
UID: NE:winioctl._WRITE_CACHE_ENABLE
title: WRITE_CACHE_ENABLE
description: Indicates whether the write cache is enabled or disabled.
helpviewer_keywords: ["WRITE_CACHE_ENABLE","WRITE_CACHE_ENABLE enumeration [Files]","WriteCacheDisabled","WriteCacheEnableUnknown","WriteCacheEnabled","fs.write_cache_enable","winioctl/WRITE_CACHE_ENABLE","winioctl/WriteCacheDisabled","winioctl/WriteCacheEnableUnknown","winioctl/WriteCacheEnabled"]
old-location: fs\write_cache_enable.htm
tech.root: fs
ms.assetid: 3ed8bc79-d8f9-4a57-a37c-46202d639a63
ms.date: 12/05/2018
ms.keywords: WRITE_CACHE_ENABLE, WRITE_CACHE_ENABLE enumeration [Files], WriteCacheDisabled, WriteCacheEnableUnknown, WriteCacheEnabled, fs.write_cache_enable, winioctl/WRITE_CACHE_ENABLE, winioctl/WriteCacheDisabled, winioctl/WriteCacheEnableUnknown, winioctl/WriteCacheEnabled
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
req.typenames: WRITE_CACHE_ENABLE
req.redist: 
f1_keywords:
 - _WRITE_CACHE_ENABLE
 - winioctl/_WRITE_CACHE_ENABLE
 - WRITE_CACHE_ENABLE
 - winioctl/WRITE_CACHE_ENABLE
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
 - WRITE_CACHE_ENABLE
---

# WRITE_CACHE_ENABLE enumeration


## -description

Indicates whether the write cache is enabled or disabled.

## -enum-fields

### -field WriteCacheEnableUnknown

The system cannot report whether the device's write cache is enabled or disabled.

### -field WriteCacheDisabled

The device's write cache is disabled.

### -field WriteCacheEnabled

The device's write cache is enabled.

## -remarks

The [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) control code reports a **WRITE_CACHE_ENABLE** value in the [STORAGE_WRITE_CACHE_PROPERTY structure](ns-winioctl-storage_write_cache_property.md).

## -see-also

* [Disk Management Enumeration Types](/windows/desktop/FileIO/disk-management-enumeration-types)
* [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md)
* [STORAGE_WRITE_CACHE_PROPERTY structure](ns-winioctl-storage_write_cache_property.md)