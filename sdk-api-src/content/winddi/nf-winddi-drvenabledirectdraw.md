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

# DrvEnableDirectDraw function


## -description


The <b>DrvEnableDirectDraw</b> function enables hardware for DirectDraw use.


## -parameters




### -param dhpdev

Handle to the <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> returned by the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a> routine.


### -param pCallBacks

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550485">DD_CALLBACKS</a> structure to be initialized by the driver.


### -param pSurfaceCallBacks

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a> structure to be initialized by the driver.


### -param pPaletteCallBacks

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a> structure to be initialized by the driver.


## -returns



<b>DrvEnableDirectDraw</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



GDI calls the driver's <b>DrvEnableDirectDraw</b> function to obtain pointers to the DirectDraw callbacks that the driver supports. The driver should set the function pointer members of <a href="https://msdn.microsoft.com/library/windows/hardware/ff550485">DD_CALLBACKS</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a> to point to those functions that it implements. A driver should also set the corresponding bitfields in the <b>dwFlags</b> members of these structures for all supported callbacks.

A driver's <b>DrvEnableDirectDraw</b> implementation can also dedicate hardware resources such as display memory for use by DirectDraw only.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550485">DD_CALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556195">DrvDisableDirectDraw</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a>
 

 

