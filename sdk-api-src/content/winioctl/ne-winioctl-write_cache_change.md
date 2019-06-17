---
UID: NE:winioctl._WRITE_CACHE_CHANGE
title: WRITE_CACHE_CHANGE
author: windows-sdk-content
description: Indicates whether the write cache features of a device are changeable.
old-location: fs\write_cache_change.htm
tech.root: FileIO
ms.assetid: a6974092-fa4f-4524-96ec-b4fad0b8c5ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WRITE_CACHE_CHANGE, WRITE_CACHE_CHANGE enumeration [Files], WriteCacheChangeUnknown, WriteCacheChangeable, WriteCacheNotChangeable, fs.write_cache_change, winioctl/WRITE_CACHE_CHANGE, winioctl/WriteCacheChangeUnknown, winioctl/WriteCacheChangeable, winioctl/WriteCacheNotChangeable
ms.topic: enum
f1_keywords: ["winioctl/WRITE_CACHE_CHANGE"]
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
 - WRITE_CACHE_CHANGE
product: Windows
targetos: Windows
req.typenames: WRITE_CACHE_CHANGE
req.redist: 
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



The <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> request 
    returns a <b>WRITE_CACHE_CHANGE</b> value in the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_write_cache_property">STORAGE_WRITE_CACHE_PROPERTY</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-enumeration-types">Disk Management Enumeration Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_write_cache_property">STORAGE_WRITE_CACHE_PROPERTY</a>
 

 

