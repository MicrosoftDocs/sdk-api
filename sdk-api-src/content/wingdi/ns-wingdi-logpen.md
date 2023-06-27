---
UID: NS:wingdi.tagLOGPEN
title: LOGPEN (wingdi.h)
description: The LOGPEN structure defines the style, width, and color of a pen. The CreatePenIndirect function uses the LOGPEN structure.
helpviewer_keywords: ["*LPLOGPEN","*NPLOGPEN","*PLOGPEN","LOGPEN","LOGPEN structure [Windows GDI]","PLOGPEN","PLOGPEN structure pointer [Windows GDI]","_win32_LOGPEN_str","gdi.logpen","wingdi/LOGPEN","wingdi/PLOGPEN"]
old-location: gdi\logpen.htm
tech.root: gdi
ms.assetid: 0e098b5a-e249-43ad-a6d8-2509b6562453
ms.date: 12/05/2018
ms.keywords: '*LPLOGPEN, *NPLOGPEN, *PLOGPEN, LOGPEN, LOGPEN structure [Windows GDI], PLOGPEN, PLOGPEN structure pointer [Windows GDI], _win32_LOGPEN_str, gdi.logpen, wingdi/LOGPEN, wingdi/PLOGPEN'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LOGPEN, *PLOGPEN, *NPLOGPEN, *LPLOGPEN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLOGPEN
 - wingdi/tagLOGPEN
 - PLOGPEN
 - wingdi/PLOGPEN
 - LOGPEN
 - wingdi/LOGPEN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - LOGPEN
---

# LOGPEN structure


## -description

The <b>LOGPEN</b> structure defines the style, width, and color of a pen. The <a href="/windows/desktop/api/wingdi/nf-wingdi-createpenindirect">CreatePenIndirect</a> function uses the <b>LOGPEN</b> structure.

## -struct-fields

### -field lopnStyle

The pen style, which can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PS_SOLID</td>
<td>The pen is solid.</td>
</tr>
<tr>
<td>PS_DASH</td>
<td>The pen is dashed.</td>
</tr>
<tr>
<td>PS_DOT</td>
<td>The pen is dotted.</td>
</tr>
<tr>
<td>PS_DASHDOT</td>
<td>The pen has alternating dashes and dots.</td>
</tr>
<tr>
<td>PS_DASHDOTDOT</td>
<td>The pen has dashes and double dots.</td>
</tr>
<tr>
<td>PS_NULL</td>
<td>The pen is invisible.</td>
</tr>
<tr>
<td>PS_INSIDEFRAME</td>
<td>The pen is solid. When this pen is used in any GDI drawing function that takes a bounding rectangle, the dimensions of the figure are shrunk so that it fits entirely in the bounding rectangle, taking into account the width of the pen. This applies only to geometric pens.</td>
</tr>
</table>

### -field lopnWidth

The [POINT](/windows/win32/api/windef/ns-windef-point) structure that contains the pen width, in logical units. If the **x** member is **NULL**, then the pen is one pixel wide on raster devices. The **y** member in the **POINT** structure for **lopnWidth** isn't used.

### -field lopnColor

The pen color. To generate a <a href="/windows/desktop/gdi/colorref">COLORREF</a> structure, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -remarks

If the width of the pen is greater than 1 and the pen style is PS_INSIDEFRAME, the line is drawn inside the frame of all GDI objects except polygons and polylines. If the pen color does not match an available RGB value, the pen is drawn with a logical (dithered) color. If the pen width is less than or equal to 1, the PS_INSIDEFRAME style is identical to the PS_SOLID style.

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpenindirect">CreatePenIndirect</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/gdi/pen-structures">Pen Structures</a>



<a href="/windows/desktop/gdi/pens">Pens Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
