---
UID: NF:winddi.EngQueryPalette
title: EngQueryPalette function (winddi.h)
description: The EngQueryPalette function queries the specified palette for its attributes.
helpviewer_keywords: ["EngQueryPalette","EngQueryPalette function [Display Devices]","display.engquerypalette","gdifncs_e11ff13c-9834-4911-9a02-a7d98f4cdfdc.xml","winddi/EngQueryPalette"]
old-location: display\engquerypalette.htm
tech.root: display
ms.assetid: be4d0547-b71a-49b4-9d2c-12fab67c9412
ms.date: 12/05/2018
ms.keywords: EngQueryPalette, EngQueryPalette function [Display Devices], display.engquerypalette, gdifncs_e11ff13c-9834-4911-9a02-a7d98f4cdfdc.xml, winddi/EngQueryPalette
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
 - EngQueryPalette
 - winddi/EngQueryPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngQueryPalette
---

# EngQueryPalette function


## -description

The <b>EngQueryPalette</b> function queries the specified palette for its attributes.

## -parameters

### -param hpal

Handle to the palette to be queried.

### -param piMode

Pointer to a location that receives the palette mode, as originally specified in <a href="/windows/desktop/api/winddi/nf-winddi-engcreatepalette">EngCreatePalette</a>.

### -param cColors

Specifies the number of entries in the buffer to which <i>pulColors</i> points. The return value depends on whether <i>cColors</i> is negative.

### -param pulColors

Pointer to a buffer that receives the palette color information. If <i>cColors</i> is zero, <i>pulColors</i> can be <b>NULL</b>.

## -returns

When <i>cColors</i> is zero, <b>EngQueryPalette</b> returns the number of palette entries required in the buffer to which <i>pulColors</i> points in order to return the palette color information. When <i>cColors</i> is nonzero and <i>pulColors</i> is not <b>NULL</b>, <b>EngQueryPalette</b> returns the number of entries written in the buffer to which <i>pulColors</i> points.

## -remarks

If the palette mode is PAL_BITFIELDS, PAL_RGB, or PAL_BGR and the buffer that <i>pulColors</i> points to is large enough, <i>pulColors</i> points to three ULONG masks that represent the red, green, and blue color masks of the palette.

If the palette mode is PAL_INDEXED and the buffer that <i>pulColors</i> points to is large enough, <i>pulColors</i> contains all of the 24-bit RGB values that represent the palette colors.

A driver must test for the presence of the GCAPS_PALMANAGED flag to determine whether the colors represent a fixed or a changeable palette.

<b>EngQueryPalette</b> is intended for use by mirroring drivers that need to know the color format of the primary display. A mirroring driver typically calls this function in its <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a> routine.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatepalette">EngCreatePalette</a>