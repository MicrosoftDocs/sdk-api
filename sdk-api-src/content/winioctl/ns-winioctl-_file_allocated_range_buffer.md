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

# _FILE_ALLOCATED_RANGE_BUFFER structure


## -description


Indicates a range of bytes in a file. This structure is used with the 
<a href="https://msdn.microsoft.com/053e26ec-1529-41b3-aeb6-128b3085bafc">FSCTL_QUERY_ALLOCATED_RANGES</a> control code. On input, the structure indicates the range of the file to search. On output, the operation retrieves an array of 
<b>FILE_ALLOCATED_RANGE_BUFFER</b> structures to indicate the allocated ranges within the search range.


## -struct-fields




### -field FileOffset

The file offset of the start of a range of bytes in a file, in bytes.


### -field Length

The size of the range, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/053e26ec-1529-41b3-aeb6-128b3085bafc">FSCTL_QUERY_ALLOCATED_RANGES</a>



<a href="https://msdn.microsoft.com/7326041d-f11e-4b80-ac4e-07173e418ce7">Sparse Files</a>
 

 

