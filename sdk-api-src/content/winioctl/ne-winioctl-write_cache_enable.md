---
UID: NE:winioctl._WRITE_CACHE_ENABLE
title: WRITE_CACHE_ENABLE
description: Indicates whether the write cache is enabled or disabled.helpviewer_keywords: ["WRITE_CACHE_ENABLE","WRITE_CACHE_ENABLE enumeration [Files]","WriteCacheDisabled","WriteCacheEnableUnknown","WriteCacheEnabled","fs.write_cache_enable","winioctl/WRITE_CACHE_ENABLE","winioctl/WriteCacheDisabled","winioctl/WriteCacheEnableUnknown","winioctl/WriteCacheEnabled"]
old-location: fs\write_cache_enable.htm
tech.root: FileIO
ms.assetid: 3ed8bc79-d8f9-4a57-a37c-46202d639a63
ms.date: 12/05/2018
ms.keywords: WRITE_CACHE_ENABLE, WRITE_CACHE_ENABLE enumeration [Files], WriteCacheDisabled, WriteCacheEnableUnknown, WriteCacheEnabled, fs.write_cache_enable, winioctl/WRITE_CACHE_ENABLE, winioctl/WriteCacheDisabled, winioctl/WriteCacheEnableUnknown, winioctl/WriteCacheEnabled
f1_keywords:
- winioctl/WRITE_CACHE_ENABLE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoCtl.h
api_name:
- WRITE_CACHE_ENABLE
targetos: Windows
req.typenames: WRITE_CACHE_ENABLE
req.redist: 
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



The <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control 
    code reports a <b>WRITE_CACHE_ENABLE</b> value in the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_write_cache_property">STORAGE_WRITE_CACHE_PROPERTY</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-enumeration-types">Disk Management Enumeration Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_write_cache_property">STORAGE_WRITE_CACHE_PROPERTY</a>
 

 

