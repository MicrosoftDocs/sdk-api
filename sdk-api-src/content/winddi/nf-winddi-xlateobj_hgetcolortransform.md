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

# XLATEOBJ_hGetColorTransform function


## -description


The <b>XLATEOBJ_hGetColorTransform</b> function returns the color transform for the specified translation object.


## -parameters




### -param pxlo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a> structure whose color transform is being queried. The color transform was created in a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>.


## -returns



<b>XLATEOBJ_hGetColorTransform</b> returns a handle to the color transform for the specified XLATEOBJ upon success. Otherwise, it returns <b>NULL</b>.




## -remarks



<b>XLATEOBJ_hGetColorTransform</b> returns <b>NULL</b> when it is called in host ICM context or when ICM is disabled.

The color transform for a brush is obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff538262">BRUSHOBJ_hGetColorTransform</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538262">BRUSHOBJ_hGetColorTransform</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a>
 

 

