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

# BRUSHOBJ_pvAllocRbrush function


## -description


The <b>BRUSHOBJ_pvAllocRbrush</b> function allocates memory for the driver's realization of a specified brush.


## -parameters




### -param pbo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure for which the realization is to be allocated.


### -param cj

Specifies the size, in bytes, required for the realization.


## -returns



The return value is a pointer to the allocated memory if the function is successful. Otherwise, it is null, and an error code is logged.




## -remarks



<b>BRUSHOBJ_pvAllocRbrush</b> allocates memory for the brush realization. GDI manages the memory and discards it when the brush is no longer needed.

This function should be called only by an implementation of a brush realization following a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556273">DrvRealizeBrush</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556273">DrvRealizeBrush</a>
 

 

