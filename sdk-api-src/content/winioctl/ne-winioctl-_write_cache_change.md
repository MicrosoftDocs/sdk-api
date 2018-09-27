---
UID: NE:winioctl._WRITE_CACHE_CHANGE
title: "_WRITE_CACHE_CHANGE"
author: windows-sdk-content
description: Indicates whether the write cache features of a device are changeable.
old-location: fs\write_cache_change.htm
tech.root: fileio
ms.assetid: a6974092-fa4f-4524-96ec-b4fad0b8c5ea
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WRITE_CACHE_CHANGE, WRITE_CACHE_CHANGE enumeration [Files], WriteCacheChangeUnknown, WriteCacheChangeable, WriteCacheNotChangeable, _WRITE_CACHE_CHANGE, fs.write_cache_change, winioctl/WRITE_CACHE_CHANGE, winioctl/WriteCacheChangeUnknown, winioctl/WriteCacheChangeable, winioctl/WriteCacheNotChangeable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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

# _WRITE_CACHE_CHANGE enumeration


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



The <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request 
    returns a <b>WRITE_CACHE_CHANGE</b> value in the 
    <a href="https://msdn.microsoft.com/5248be70-229d-42e6-923a-5a6ffd5268b1">STORAGE_WRITE_CACHE_PROPERTY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ed8fe5c1-dbdf-43bc-a0a7-17e541eba950">Disk Management Enumeration Types</a>



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/5248be70-229d-42e6-923a-5a6ffd5268b1">STORAGE_WRITE_CACHE_PROPERTY</a>
 

 

