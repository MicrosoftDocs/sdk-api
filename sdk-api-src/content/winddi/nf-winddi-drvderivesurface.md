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

# DrvDeriveSurface function


## -description


The <b>DrvDeriveSurface</b> function derives a GDI surface from the specified DirectDraw surface.


## -parameters




### -param pDirectDraw

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550586">DD_DIRECTDRAW_GLOBAL</a> structure that describes the DirectDraw object.


### -param pSurface

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that describes the DirectDraw surface around which to wrap a GDI surface.


## -returns



<b>DrvDeriveSurface</b> returns a handle to the derived GDI surface upon success. It returns <b>NULL</b> if the call fails or if the driver cannot accelerate GDI drawing to the specified DirectDraw surface.




## -remarks



<b>DrvDeriveSurface</b> allows the driver to create a GDI surface wrapped around a DirectDraw video memory or AGP surface object in order to allow accelerated GDI drawing to the surface. If the driver does not hook this call, all GDI drawing to DirectDraw surfaces is done in software using the DIB engine.

GDI calls <b>DrvDeriveSurface</b> with RGB surfaces only.

The driver should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a> to create a GDI surface of the same size and format as that of the DirectDraw surface. Space for the actual pixels need not be allocated since it already exists.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564204">EngCreateDeviceBitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564976">EngModifySurface</a>
 

 

