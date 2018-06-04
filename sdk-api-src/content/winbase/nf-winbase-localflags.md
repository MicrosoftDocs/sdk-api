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

# LocalFlags function


## -description


Retrieves information about the specified local memory object.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a>. For more information, see Remarks.</div><div> </div>

## -parameters




### -param hMem [in]

A handle to the local memory object. This handle is returned by either the 
<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> or 
<a href="https://msdn.microsoft.com/88527ddd-e0c2-4a41-825e-d3a6df77fd2a">LocalReAlloc</a> function.


## -returns



If the function succeeds, the return value specifies the allocation values and the lock count for the memory object.

If the function fails, the return value is <b>LMEM_INVALID_HANDLE</b>, indicating that the local handle is not valid. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The low-order byte of the low-order word of the return value contains the lock count of the object. To retrieve the lock count from the return value, use the <b>LMEM_LOCKCOUNT</b> mask with the bitwise AND (&amp;) operator. The lock count of memory objects allocated with <b>LMEM_FIXED</b> is always zero.

The high-order byte of the low-order word of the return value indicates the allocation values of the memory object. It can be zero or <b>LMEM_DISCARDABLE</b>.

The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.




## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/647fc9a2-0522-42ab-ab8b-43c648f27d90">GlobalFlags</a>



<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>



<a href="https://msdn.microsoft.com/05842fa7-0438-4237-962f-055dc338368c">LocalDiscard</a>



<a href="https://msdn.microsoft.com/a9432e28-9fbd-4a7e-8dce-fad3da04804a">LocalLock</a>



<a href="https://msdn.microsoft.com/88527ddd-e0c2-4a41-825e-d3a6df77fd2a">LocalReAlloc</a>



<a href="https://msdn.microsoft.com/eac40b69-5fb6-4523-826d-a012f6f4e5ce">LocalUnlock</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

