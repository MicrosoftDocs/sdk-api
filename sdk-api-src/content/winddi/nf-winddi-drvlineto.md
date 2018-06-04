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

# DrvLineTo function


## -description


The <b>DrvLineTo</b> function draws a single, solid, integer-only cosmetic line.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the surface on which to draw.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure that defines the clip region in which the rendering must be done. No pixels can be affected outside this clip region.


### -param pbo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure that specifies the brush to use when drawing the line.


### -param x1

Specify the integer x-coodinates of the line's beginning point.


### -param y1

Specify the integer y-coodinates of the line's beginning point.


### -param x2

Specify the integer x-coordinates of the line's end point.


### -param y2

Specify the integer y-coordinates of the line's end point.


### -param prclBounds

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that defines the integer rectangle that bounds the unclipped line. Drivers that support hardware line drawing can use this rectangle to quickly determine whether the line fits in a coordinate space small enough to be rendered by the hardware.


### -param mix

The mix mode that defines the foreground and background raster operations to use for the brush. In the call to <b>DrvLineTo</b>, the foreground and background raster-operation values are the same. For more information about mix mode, see Remarks.


## -returns



<b>DrvLineTo</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



<b>DrvLineTo</b> is an optional entry point that a driver can supply as an optimization for application calls to the Win32 <b>LineTo</b> function. If the driver doesn't hook <b>DrvLineTo</b>, or if the driver returns <b>FALSE</b> from a call to this function, GDI will automatically call <a href="https://msdn.microsoft.com/library/windows/hardware/ff556316">DrvStrokePath</a> instead. A driver that has hooked <b>DrvLineTo</b> can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564962">EngLineTo</a> when the rendering surface is a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">DIB</a>.

This function is simpler than <a href="https://msdn.microsoft.com/library/windows/hardware/ff556316">DrvStrokePath</a> because it supports only integer end-points and solid cosmetic lines. GDI has less overhead when calling <b>DrvLineTo</b> instead of <b>DrvStrokePath</b>; consequently, <b>DrvLineTo</b> is intended to be used as a simple optimization by drivers that can accelerate nominal width lines in hardware.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556316">DrvStrokePath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564962">EngLineTo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

