---
UID: NE:winioctl._WRITE_THROUGH
title: "_WRITE_THROUGH"
author: windows-sdk-content
description: Specifies whether a storage device supports write-through caching.
old-location: fs\write_through.htm
tech.root: fileio
ms.assetid: 8bb26be1-ad02-4cf0-8505-021f922f34bf
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: WRITE_THROUGH, WRITE_THROUGH enumeration [Files], WriteThroughNotSupported, WriteThroughSupported, WriteThroughUnknown, _WRITE_THROUGH, fs.write_through, winioctl/WRITE_THROUGH, winioctl/WriteThroughNotSupported, winioctl/WriteThroughSupported, winioctl/WriteThroughUnknown
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
 - WRITE_THROUGH
product: Windows
targetos: Windows
req.typenames: WRITE_THROUGH
req.redist: 
---

# _WRITE_THROUGH enumeration


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



The <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> control 
     code reports this value in the 
     <a href="https://msdn.microsoft.com/5248be70-229d-42e6-923a-5a6ffd5268b1">STORAGE_WRITE_CACHE_PROPERTY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ed8fe5c1-dbdf-43bc-a0a7-17e541eba950">Disk Management Enumeration Types</a>



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/5248be70-229d-42e6-923a-5a6ffd5268b1">STORAGE_WRITE_CACHE_PROPERTY</a>
 

 

