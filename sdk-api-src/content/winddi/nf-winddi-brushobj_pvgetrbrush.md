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

# BRUSHOBJ_pvGetRbrush function


## -description


The <b>BRUSHOBJ_pvGetRbrush</b> function retrieves a pointer to the driver's realization of a specified brush.


## -parameters




### -param pbo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure whose realization is requested.


## -returns



The return value is a pointer to the realized brush if the function is successful. If the brush cannot be realized, the return value is null and an error code is logged.




## -remarks



<b>BRUSHOBJ_pvGetRbrush</b> is called when the brush is a pattern brush that has not yet been realized; that is, it is called when the <b>iSolidColor</b> member of the BRUSHOBJ structure is 0xFFFFFFFF and the <b>pvRbrush</b> member is null.

If the brush has not been realized when <b>BRUSHOBJ_pvGetRbrush</b> is called, GDI calls the driver-supplied <a href="https://msdn.microsoft.com/library/windows/hardware/ff556273">DrvRealizeBrush</a> function to obtain the driver's realization of the brush. As an acceleration, GDI caches this realization in the <b>pvRbrush</b> member of the BRUSHOBJ structure. Then, when an application reuses this brush for another drawing operation, the driver doesn't have to call <b>BRUSHOBJ_pvGetRbrush</b> again.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538263">BRUSHOBJ_pvAllocRbrush</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556273">DrvRealizeBrush</a>
 

 

