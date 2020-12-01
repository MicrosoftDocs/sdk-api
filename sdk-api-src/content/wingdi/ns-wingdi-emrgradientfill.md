---
UID: NS:wingdi.tagEMRGRADIENTFILL
title: EMRGRADIENTFILL (wingdi.h)
description: The EMRGRADIENTFILL structure contains members for the GradientFill enhanced metafile record.
helpviewer_keywords: ["*PEMRGRADIENTFILL","EMRGRADIENTFILL","EMRGRADIENTFILL structure [Windows GDI]","GRADIENT_FILL_RECT_H","GRADIENT_FILL_RECT_V","GRADIENT_FILL_TRIANGLE","PEMRGRADIENTFILL","PEMRGRADIENTFILL structure pointer [Windows GDI]","_win32_EMRGRADIENTFILL_str","gdi.emrgradientfill","wingdi/EMRGRADIENTFILL","wingdi/PEMRGRADIENTFILL"]
old-location: gdi\emrgradientfill.htm
tech.root: gdi
ms.assetid: efd12e71-ee26-4fc8-8e9f-5b0105ebe057
ms.date: 12/05/2018
ms.keywords: '*PEMRGRADIENTFILL, EMRGRADIENTFILL, EMRGRADIENTFILL structure [Windows GDI], GRADIENT_FILL_RECT_H, GRADIENT_FILL_RECT_V, GRADIENT_FILL_TRIANGLE, PEMRGRADIENTFILL, PEMRGRADIENTFILL structure pointer [Windows GDI], _win32_EMRGRADIENTFILL_str, gdi.emrgradientfill, wingdi/EMRGRADIENTFILL, wingdi/PEMRGRADIENTFILL'
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
req.typenames: EMRGRADIENTFILL, *PEMRGRADIENTFILL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRGRADIENTFILL
 - wingdi/tagEMRGRADIENTFILL
 - PEMRGRADIENTFILL
 - wingdi/PEMRGRADIENTFILL
 - EMRGRADIENTFILL
 - wingdi/EMRGRADIENTFILL
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
 - EMRGRADIENTFILL
---

# EMRGRADIENTFILL structure


## -description

The <b>EMRGRADIENTFILL</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field rclBounds

The bounding rectangle, in device units.

### -field nVer

The number of vertices.

### -field nTri

The number of rectangles or triangles to be passed to <a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a>.

### -field ulMode

The gradient fill mode. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_RECT_H"></a><a id="gradient_fill_rect_h"></a><dl>
<dt><b>GRADIENT_FILL_RECT_H</b></dt>
</dl>
</td>
<td width="60%">
In this mode, two endpoints describe a rectangle. The rectangle is defined to have a constant color (specified by the <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structure) for the left and right edges. GDI interpolates the color from the left to right edge and fills the interior.

</td>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_RECT_V"></a><a id="gradient_fill_rect_v"></a><dl>
<dt><b>GRADIENT_FILL_RECT_V</b></dt>
</dl>
</td>
<td width="60%">
In this mode, two endpoints describe a rectangle. The rectangle is defined to have a constant color (specified by the <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structure) for the top and bottom edges. GDI interpolates the color from the top to bottom edge and fills the interior.

</td>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_TRIANGLE"></a><a id="gradient_fill_triangle"></a><dl>
<dt><b>GRADIENT_FILL_TRIANGLE</b></dt>
</dl>
</td>
<td width="60%">
In this mode, an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structures is passed to GDI along with a list of array indexes that describe separate triangles. GDI performs linear interpolation between triangle vertices and fills the interior. Drawing is done directly in 24- and 32-bpp modes. Dithering is performed in 16-, 8-, 4-, and 1-bpp mode.

</td>
</tr>
</table>

### -field Ver

An array of <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structures that each define a vertex.

## -remarks

This is a variable-length structure. The <b>Ver</b> member designates the beginning of the variable-length area. First comes an array of <b>nVer</b> <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structures to pass the vertices. Next comes an array of either <b>nTri</b> <a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_triangle">GRADIENT_TRIANGLE</a> structures or <b>nTri</b> <a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_rect">GRADIENT_RECT</a> structures, depending on the value of <b>ulMode</b> (triangles or rectangles).

This structure is to be used during metafile playback.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_rect">GRADIENT_RECT</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_triangle">GRADIENT_TRIANGLE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



Metafiles



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>