---
UID: NE:winioctl._WRITE_CACHE_TYPE
title: WRITE_CACHE_TYPE
description: Specifies the cache type.
old-location: fs\write_cache_type.htm
tech.root: FileIO
ms.assetid: fb861a65-5207-4af3-b994-0883febcbb0a
ms.date: 12/05/2018
ms.keywords: WRITE_CACHE_TYPE, WRITE_CACHE_TYPE enumeration [Files], WriteCacheTypeNone, WriteCacheTypeUnknown, WriteCacheTypeWriteBack, WriteCacheTypeWriteThrough, fs.write_cache_type, winioctl/WRITE_CACHE_TYPE, winioctl/WriteCacheTypeNone, winioctl/WriteCacheTypeUnknown, winioctl/WriteCacheTypeWriteBack, winioctl/WriteCacheTypeWriteThrough
f1_keywords:
- winioctl/WRITE_CACHE_TYPE
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
- WRITE_CACHE_TYPE
targetos: Windows
req.typenames: WRITE_CACHE_TYPE
req.redist: 
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



There are two main types of write cache: <i>write back</i> and <i>write through</i>. With a 
    write-back cache, the device does not copy cache data to nonvolatile media until absolutely necessary. This type 
    of operation improves the performance of write operations. With a write-through cache, the device writes data to 
    the cache and the media in parallel. This type of operation does not improve write performance, but it makes 
    subsequent read operations faster.

The <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control 
    code reports a <b>WRITE_CACHE_TYPE</b> value in the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_write_cache_property">STORAGE_WRITE_CACHE_PROPERTY</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-enumeration-types">Disk Management Enumeration Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_write_cache_property">STORAGE_WRITE_CACHE_PROPERTY</a>
 

 

