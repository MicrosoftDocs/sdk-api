---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _FILE_LEVEL_TRIM_RANGE structure


## -description


Specifies a range of a file that is to be trimmed.


## -struct-fields




### -field Offset

Offset, in bytes, from the start of the file for the range to be trimmed.


### -field Length

Length, in bytes, for the range to be trimmed.


## -remarks



Before the trim operation is passed to the underlying storage system the input ranges are reduced to be 
    aligned to page boundaries (4,096 bytes on 32-bit and x64-based editions of Windows, 8,192 bytes on Itanium-Based 
    editions of Windows).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh406398">FILE_LEVEL_TRIM</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406402">FILE_LEVEL_TRIM_OUTPUT</a>



<b>FSCTL_FILE_LEVEL_TRIM</b>
 

 

