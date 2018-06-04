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

# PFREEMEM callback function


## -description


The 
<i>PFREEMEM</i> function is a memory-freeing function provided by the PCM. 
<i>PFREEMEM</i> frees memory buffers that were allocated using 
<a href="https://msdn.microsoft.com/e7b38820-4a7e-4f17-a67d-b94caa9037f5">PALLOCMEM</a>. The 
<i>PFREEMEM</i> function is supplied as a parameter of the 
<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a> function. The combination of 
<i>PALLOCMEM</i> and 
<i>PFREEMEM</i> allows the SBM to experiment with different memory-management schemes without requiring recompilation of LPMs.


## -parameters




### -param *pv [in]

Pointer to the memory buffer to free.


### -param *szFileName


### -param nLine








## -returns



This callback function does not return a value.




## -remarks



LPMs do not need to use this function to manage their local buffers. LPMs need to use this function to free buffers that were allocated, but were not sent to the PCM. For example, if a buffer is allocated in anticipation of a PCM's response to a request, but a response is never returned (perhaps the remote policy store is unavailable or unresponsive), that buffer must be freed with this function, or a memory leak will ensue.




## -see-also




<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a>



<a href="https://msdn.microsoft.com/e7b38820-4a7e-4f17-a67d-b94caa9037f5">PALLOCMEM</a>
 

 

