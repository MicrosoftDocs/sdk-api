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

# DrvStartBanding function


## -description


The <b>DrvStartBanding</b> function is called by GDI when it is ready to start sending bands of a physical page to the driver for rendering.


## -parameters




### -param pso [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure, which identifies the banding surface.


### -param pptl [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure to receive the function-supplied origin of the first band.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.




## -remarks



If a printer graphics DLL uses GDI-managed surfaces, and if it supports surface banding, it must provide a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556250">DrvNextBand</a> function. GDI calls <b>DrvStartBanding</b> only if the printer graphics DLL's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a> function previously called <a href="https://msdn.microsoft.com/library/windows/hardware/ff564975">EngMarkBandingSurface</a> to specify a banding surface.

The <b>DrvStartBanding</b> function's purpose is to allow the printer graphics DLL to perform any initializations needed before banding operations begin on a physical page, and to provide GDI with the indices of the first band's origin.

The <b>DrvStartBanding</b> function is called once per page. Each time GDI has finished drawing a band, it calls <a href="https://msdn.microsoft.com/library/windows/hardware/ff556250">DrvNextBand</a> so the driver can send the band to the printer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556250">DrvNextBand</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564975">EngMarkBandingSurface</a>
 

 

