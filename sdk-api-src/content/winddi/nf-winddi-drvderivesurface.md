---
UID: NF:winddi.DrvDeriveSurface
title: DrvDeriveSurface function
author: windows-sdk-content
description: The DrvDeriveSurface function derives a GDI surface from the specified DirectDraw surface.
old-location: display\drvderivesurface.htm
tech.root: display
ms.assetid: 7cd0acf8-34ef-425b-9967-43008d77b900
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: DrvDeriveSurface, DrvDeriveSurface function [Display Devices], ddifncs_b38de767-eeaf-4120-8711-6f3319a53058.xml, display.drvderivesurface, winddi/DrvDeriveSurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvDeriveSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvDeriveSurface function


## -description


The <b>DrvDeriveSurface</b> function derives a GDI surface from the specified DirectDraw surface.


## -parameters




### -param pDirectDraw

Pointer to a <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the DirectDraw object.


### -param pSurface

Pointer to a <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure that describes the DirectDraw surface around which to wrap a GDI surface.


## -returns



<b>DrvDeriveSurface</b> returns a handle to the derived GDI surface upon success. It returns <b>NULL</b> if the call fails or if the driver cannot accelerate GDI drawing to the specified DirectDraw surface.




## -remarks



<b>DrvDeriveSurface</b> allows the driver to create a GDI surface wrapped around a DirectDraw video memory or AGP surface object in order to allow accelerated GDI drawing to the surface. If the driver does not hook this call, all GDI drawing to DirectDraw surfaces is done in software using the DIB engine.

GDI calls <b>DrvDeriveSurface</b> with RGB surfaces only.

The driver should call <a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a> to create a GDI surface of the same size and format as that of the DirectDraw surface. Space for the actual pixels need not be allocated since it already exists.




## -see-also




<a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a>



<a href="https://msdn.microsoft.com/dc9d7154-30b9-4462-9161-6df03946308d">EngCreateDeviceBitmap</a>



<a href="https://msdn.microsoft.com/176f51c0-0075-4afb-8b5c-5d0b6b64a3ad">EngModifySurface</a>
 

 

