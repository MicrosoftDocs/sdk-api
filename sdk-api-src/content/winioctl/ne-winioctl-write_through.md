---
UID: NE:winioctl._WRITE_THROUGH
title: WRITE_THROUGH
author: windows-sdk-content
description: Specifies whether a storage device supports write-through caching.
old-location: fs\write_through.htm
tech.root: FileIO
ms.assetid: 8bb26be1-ad02-4cf0-8505-021f922f34bf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WRITE_THROUGH, WRITE_THROUGH enumeration [Files], WriteThroughNotSupported, WriteThroughSupported, WriteThroughUnknown, fs.write_through, winioctl/WRITE_THROUGH, winioctl/WriteThroughNotSupported, winioctl/WriteThroughSupported, winioctl/WriteThroughUnknown
ms.topic: enum
f1_keywords: ["winioctl/WRITE_THROUGH"]
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
 - WRITE_THROUGH
product: Windows
targetos: Windows
req.typenames: WRITE_THROUGH
req.redist: 
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



The <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control 
     code reports this value in the 
     <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_write_cache_property">STORAGE_WRITE_CACHE_PROPERTY</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-enumeration-types">Disk Management Enumeration Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_write_cache_property">STORAGE_WRITE_CACHE_PROPERTY</a>
 

 

