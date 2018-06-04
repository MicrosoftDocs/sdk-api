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

# RtlPcToFileHeader function


## -description


Retrieves the base address of the image that contains the specified PC value.


## -parameters




### -param PcValue [in]

The PC value. The function searches all modules mapped into the address space of the calling process for a module that contains this value.


### -param BaseOfImage [out]

The base address of the image containing the PC value. This value must be added to any relative addresses in the headers to locate the image.


## -returns



If the PC value is found, the function returns the base address of the image that contains the PC value.

If no image contains the PC value, the function returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/624b97fb-0453-4f47-b6bd-92aa14705e78">RtlLookupFunctionEntry</a>
 

 

