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

# MFHeapAlloc function


## -description



Allocates a block of memory.




## -parameters




### -param nSize [in]

Number of bytes to allocate.


### -param dwFlags [in]

Zero or more flags. For a list of valid flags, see <b>HeapAlloc</b> in the Windows SDK documentation.


### -param pszFile [in]


            Reserved. Set to <b>NULL</b>.
          


### -param line [in]


            Reserved. Set to zero.
          


### -param eat [in]


            Reserved. Set to <b>eAllocationTypeIgnore</b>.
          


## -returns



If the function succeeds, it returns a pointer to the allocated memory block. If the function fails, it returns <b>NULL</b>.




## -remarks



In the current version of Media Foundation, this function is equivalent to calling the <b>HeapAlloc</b> function and specifying the heap of the calling process.

To free the allocated memory, call <a href="https://msdn.microsoft.com/c4a03a20-5398-4fe0-9a1f-3bc162c624cd">MFHeapFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

