---
UID: NF:winddi.EngLineTo
title: EngLineTo function (winddi.h)
description: The EngLineTo function draws a single, solid, integer-only cosmetic line.
helpviewer_keywords: ["EngLineTo","EngLineTo function [Display Devices]","display.englineto","gdifncs_7f51ef7a-df4c-4482-a411-101dff0711d7.xml","winddi/EngLineTo"]
old-location: display\englineto.htm
tech.root: display
ms.assetid: 989ac941-496e-4433-a871-f541fdced45f
ms.date: 12/05/2018
ms.keywords: EngLineTo, EngLineTo function [Display Devices], display.englineto, gdifncs_7f51ef7a-df4c-4482-a411-101dff0711d7.xml, winddi/EngLineTo
req.header: winddi.h
req.include-header: Winddi.h
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngLineTo
 - winddi/EngLineTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-common-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngLineTo
---

# EngLineTo function


## -description

The <b>EngLineTo</b> function draws a single, solid, integer-only cosmetic line.

## -parameters

### -param pso

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param pco

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that defines the clip region in which the rendering must be done. No pixels can be affected outside this clip region.

### -param pbo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that specifies the brush to use when drawing the line.

### -param x1

Specify the integer x-coordinate of the line's beginning point.

### -param y1

Specify the integer y-coordinate of the line's beginning point.

### -param x2

Specify the integer x-coordinate of the line's end point.

### -param y2

Specify the integer x- and y-coordinate of the line's end point.

### -param prclBounds

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that describes the rectangle that bounds the unclipped line. Drivers that support hardware line drawing can use this rectangle to quickly determine whether the line fits in a coordinate space small enough to be rendered by the hardware.

### -param mix

Defines how the incoming pattern should be mixed with the data already on the device surface. The low-order byte defines the raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.

## -returns

<b>EngLineTo</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.

## -remarks

The driver that has hooked <a href="/windows/desktop/api/winddi/nf-winddi-drvlineto">DrvLineTo</a> can call <b>EngLineTo</b> when the rendering surface is a device-independent bitmap (DIB).

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvlineto">DrvLineTo</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>