---
UID: NF:winddi.EngLineTo
title: EngLineTo function
author: windows-sdk-content
description: The EngLineTo function draws a single, solid, integer-only cosmetic line.
old-location: display\englineto.htm
old-project: display
ms.assetid: 989ac941-496e-4433-a871-f541fdced45f
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: EngLineTo, EngLineTo function [Display Devices], display.englineto, gdifncs_7f51ef7a-df4c-4482-a411-101dff0711d7.xml, winddi/EngLineTo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngLineTo
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngLineTo function


## -description


The <b>EngLineTo</b> function draws a single, solid, integer-only cosmetic line.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface on which to draw.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure that defines the clip region in which the rendering must be done. No pixels can be affected outside this clip region.


### -param pbo

Pointer to a <a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a> structure that specifies the brush to use when drawing the line.


### -param x1

Specify the integer x-coordinate of the line's beginning point.


### -param y1

Specify the integer y-coordinate of the line's beginning point.


### -param x2

Specify the integer x-coordinate of the line's end point.


### -param y2

Specify the integer x- and y-coordinate of the line's end point.


### -param prclBounds

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that describes the rectangle that bounds the unclipped line. Drivers that support hardware line drawing can use this rectangle to quickly determine whether the line fits in a coordinate space small enough to be rendered by the hardware.


### -param mix

Defines how the incoming pattern should be mixed with the data already on the device surface. The low-order byte defines the raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.


## -returns



<b>EngLineTo</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



The driver that has hooked <a href="https://msdn.microsoft.com/e1e5dd93-444d-4176-9f7f-8aa220cddf78">DrvLineTo</a> can call <b>EngLineTo</b> when the rendering surface is a device-independent bitmap (DIB).




## -see-also




<a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/e1e5dd93-444d-4176-9f7f-8aa220cddf78">DrvLineTo</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 

