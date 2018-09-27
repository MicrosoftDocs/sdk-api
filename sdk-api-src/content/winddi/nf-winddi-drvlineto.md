---
UID: NF:winddi.DrvLineTo
title: DrvLineTo function
author: windows-sdk-content
description: The DrvLineTo function draws a single, solid, integer-only cosmetic line.
old-location: display\drvlineto.htm
tech.root: display
ms.assetid: e1e5dd93-444d-4176-9f7f-8aa220cddf78
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DrvLineTo, DrvLineTo function [Display Devices], ddifncs_85694fcd-95b7-4b3e-8f00-bec09b3d9a32.xml, display.drvlineto, winddi/DrvLineTo
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
 - DrvLineTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvLineTo function


## -description


The <b>DrvLineTo</b> function draws a single, solid, integer-only cosmetic line.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface on which to draw.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure that defines the clip region in which the rendering must be done. No pixels can be affected outside this clip region.


### -param pbo

Pointer to a <a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a> structure that specifies the brush to use when drawing the line.


### -param x1

Specify the integer x-coodinates of the line's beginning point.


### -param y1

Specify the integer y-coodinates of the line's beginning point.


### -param x2

Specify the integer x-coordinates of the line's end point.


### -param y2

Specify the integer y-coordinates of the line's end point.


### -param prclBounds

Pointer to the <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that defines the integer rectangle that bounds the unclipped line. Drivers that support hardware line drawing can use this rectangle to quickly determine whether the line fits in a coordinate space small enough to be rendered by the hardware.


### -param mix

The mix mode that defines the foreground and background raster operations to use for the brush. In the call to <b>DrvLineTo</b>, the foreground and background raster-operation values are the same. For more information about mix mode, see Remarks.


## -returns



<b>DrvLineTo</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



<b>DrvLineTo</b> is an optional entry point that a driver can supply as an optimization for application calls to the Win32 <b>LineTo</b> function. If the driver doesn't hook <b>DrvLineTo</b>, or if the driver returns <b>FALSE</b> from a call to this function, GDI will automatically call <a href="https://msdn.microsoft.com/c931a39d-c0ae-4f40-b70f-f51d5621c228">DrvStrokePath</a> instead. A driver that has hooked <b>DrvLineTo</b> can call <a href="https://msdn.microsoft.com/989ac941-496e-4433-a871-f541fdced45f">EngLineTo</a> when the rendering surface is a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">DIB</a>.

This function is simpler than <a href="https://msdn.microsoft.com/c931a39d-c0ae-4f40-b70f-f51d5621c228">DrvStrokePath</a> because it supports only integer end-points and solid cosmetic lines. GDI has less overhead when calling <b>DrvLineTo</b> instead of <b>DrvStrokePath</b>; consequently, <b>DrvLineTo</b> is intended to be used as a simple optimization by drivers that can accelerate nominal width lines in hardware.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation. 




## -see-also




<a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/c931a39d-c0ae-4f40-b70f-f51d5621c228">DrvStrokePath</a>



<a href="https://msdn.microsoft.com/989ac941-496e-4433-a871-f541fdced45f">EngLineTo</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 

