---
UID: NS:winioctl._STORAGE_DESCRIPTOR_HEADER
title: "_STORAGE_DESCRIPTOR_HEADER"
author: windows-driver-content
description: Used in conjunction with the IOCTL_STORAGE_QUERY_PROPERTY control code to retrieve the properties of a storage device or adapter.
old-location: fs\storage_descriptor_header.htm
old-project: FileIO
ms.assetid: f98e53d5-45cb-4c3f-b04d-8eecd98655d2
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: PSTORAGE_DESCRIPTOR_HEADER, PSTORAGE_DESCRIPTOR_HEADER structure pointer [Files], STORAGE_DESCRIPTOR_HEADER, STORAGE_DESCRIPTOR_HEADER structure [Files], _STORAGE_DESCRIPTOR_HEADER, fs.storage_descriptor_header, winioctl/PSTORAGE_DESCRIPTOR_HEADER, winioctl/STORAGE_DESCRIPTOR_HEADER
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: STORAGE_DESCRIPTOR_HEADER, PSTORAGE_DESCRIPTOR_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	STORAGE_DESCRIPTOR_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_DESCRIPTOR_HEADER structure


## -description


Used in conjunction with the 
   <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> control code to 
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
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> is reported in 
     the buffer immediately following this structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552549">DEVICE_SEEK_PENALTY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552562">DEVICE_TRIM_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566344">STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566346">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566971">STORAGE_DEVICE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566972">STORAGE_DEVICE_ID_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt668772">STORAGE_MINIPORT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566997">STORAGE_PROPERTY_QUERY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567017">STORAGE_WRITE_CACHE_PROPERTY</a>
 

 

