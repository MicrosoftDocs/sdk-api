---
UID: NF:wingdi.FloodFill
title: FloodFill function (wingdi.h)
description: The FloodFill function fills an area of the display surface with the current brush. The area is assumed to be bounded as specified by the color parameter.
helpviewer_keywords: ["FloodFill","FloodFill function [Windows GDI]","_win32_FloodFill","gdi.floodfill","wingdi/FloodFill"]
old-location: gdi\floodfill.htm
tech.root: gdi
ms.assetid: e53bebb5-4e46-4ea4-8d41-c12f4c6645ef
ms.date: 12/05/2018
ms.keywords: FloodFill, FloodFill function [Windows GDI], _win32_FloodFill, gdi.floodfill, wingdi/FloodFill
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FloodFill
 - wingdi/FloodFill
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - FloodFill
---

# FloodFill function


## -description

The <b>FloodFill</b> function fills an area of the display surface with the current brush. The area is assumed to be bounded as specified by the <i>color</i> parameter.
<div class="alert"><b>Note</b>  The <b>FloodFill</b> function is included only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/wingdi/nf-wingdi-extfloodfill">ExtFloodFill</a> function with FLOODFILLBORDER specified.</div><div> </div>

## -parameters

### -param hdc [in]

A handle to a device context.

### -param x [in]

The x-coordinate, in logical units, of the point where filling is to start.

### -param y [in]

The y-coordinate, in logical units, of the point where filling is to start.

### -param color [in]

The color of the boundary or the area to be filled. To create a <a href="/windows/desktop/gdi/colorref">COLORREF</a> color value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The following are reasons this function might fail:

<ul>
<li>The fill could not be completed.</li>
<li>The given point has the boundary color specified by the <i>color</i> parameter.</li>
<li>The given point lies outside the current clipping region, that is, it is not visible on the device.</li>
</ul>

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/gdi/colorref">COLORREF
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extfloodfill">ExtFloodFill
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB
      </a>
