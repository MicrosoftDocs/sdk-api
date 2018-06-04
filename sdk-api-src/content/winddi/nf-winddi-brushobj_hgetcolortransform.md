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

# BRUSHOBJ_hGetColorTransform function


## -description


The <b>BRUSHOBJ_hGetColorTransform</b> function retrieves the color transform for the specified brush.


## -parameters




### -param pbo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure whose color transform is being queried. The color transform was created in a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>.


## -returns



<b>BRUSHOBJ_hGetColorTransform</b> returns a handle to the color transform for the specified BRUSHOBJ structure upon success. Otherwise, it returns <b>NULL</b>.




## -remarks



<b>BRUSHOBJ_hGetColorTransform</b> returns <b>NULL</b> when ICM is disabled.

The color transform for a translation object is obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff570639">XLATEOBJ_hGetColorTransform</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570639">XLATEOBJ_hGetColorTransform</a>
 

 

