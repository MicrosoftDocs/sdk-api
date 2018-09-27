---
UID: NS:winioctl._STORAGE_DESCRIPTOR_HEADER
title: "_STORAGE_DESCRIPTOR_HEADER"
author: windows-sdk-content
description: Used in conjunction with the IOCTL_STORAGE_QUERY_PROPERTY control code to retrieve the properties of a storage device or adapter.
old-location: fs\storage_descriptor_header.htm
tech.root: fileio
ms.assetid: f98e53d5-45cb-4c3f-b04d-8eecd98655d2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PSTORAGE_DESCRIPTOR_HEADER, PSTORAGE_DESCRIPTOR_HEADER, PSTORAGE_DESCRIPTOR_HEADER structure pointer [Files], STORAGE_DESCRIPTOR_HEADER, STORAGE_DESCRIPTOR_HEADER structure [Files], _STORAGE_DESCRIPTOR_HEADER, fs.storage_descriptor_header, winioctl/PSTORAGE_DESCRIPTOR_HEADER, winioctl/STORAGE_DESCRIPTOR_HEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - STORAGE_DESCRIPTOR_HEADER
product: Windows
targetos: Windows
req.typenames: STORAGE_DESCRIPTOR_HEADER, *PSTORAGE_DESCRIPTOR_HEADER
req.redist: 
---

# _STORAGE_DESCRIPTOR_HEADER structure


## -description


Used in conjunction with the 
   <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> control code to 
   retrieve the properties of a storage device or adapter.


## -struct-fields




### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.


### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.


## -remarks



The data retrieved by 
     <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> is reported in 
     the buffer immediately following this structure.




## -see-also




<a href="https://msdn.microsoft.com/b3fbf27a-dac8-4fd2-8c0d-f621f0123c98">DEVICE_SEEK_PENALTY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/60b38d08-5869-442f-845b-b3d8667d069f">DEVICE_TRIM_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/99f33d12-5da0-4ed9-a20f-5e808a610545">STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/8a5059d3-09a4-4411-8d86-d1257edb409a">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/f84f8a88-b6fc-4b22-b858-52955c8d537d">STORAGE_DEVICE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/67b346fd-8976-4cd7-bb2f-a44ef6d56bc4">STORAGE_DEVICE_ID_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/b962666d-60ae-4e0b-813e-7b22e1670644">STORAGE_MINIPORT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>



<a href="https://msdn.microsoft.com/5248be70-229d-42e6-923a-5a6ffd5268b1">STORAGE_WRITE_CACHE_PROPERTY</a>
 

 

