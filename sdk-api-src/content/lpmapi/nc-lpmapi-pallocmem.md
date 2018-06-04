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

# PALLOCMEM callback function


## -description


The 
<i>PALLOCMEM</i> function is a memory allocation function provided by the PCM, used for allocating memory when returning policy information to the PCM. The 
<i>PALLOCMEM</i> function is supplied as a parameter of the 
<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a> function, and allows the SBM to experiment with different memory-management schemes without requiring recompilation of LPMs.


## -parameters




### -param Size [in]

Size of the memory buffer required by the LPM.


### -param *szFileName


### -param nLine








## -returns



Returns a pointer to the requested memory allocation.




## -remarks



LPMs do not need to use this function to manage their local buffers.




## -see-also




<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a>
 

 

