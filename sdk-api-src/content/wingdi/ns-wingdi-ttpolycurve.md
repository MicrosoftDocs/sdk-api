---
UID: NS:wingdi.tagTTPOLYCURVE
title: TTPOLYCURVE (wingdi.h)
description: The TTPOLYCURVE structure contains information about a curve in the outline of a TrueType character.
helpviewer_keywords: ["*LPTTPOLYCURVE","LPTTPOLYCURVE","LPTTPOLYCURVE structure pointer [Windows GDI]","TTPOLYCURVE","TTPOLYCURVE structure [Windows GDI]","_win32_TTPOLYCURVE_str","gdi.ttpolycurve","wingdi/LPTTPOLYCURVE","wingdi/TTPOLYCURVE"]
old-location: gdi\ttpolycurve.htm
tech.root: gdi
ms.assetid: 59a26aec-786e-471b-8e08-ddffb04874d6
ms.date: 12/05/2018
ms.keywords: '*LPTTPOLYCURVE, LPTTPOLYCURVE, LPTTPOLYCURVE structure pointer [Windows GDI], TTPOLYCURVE, TTPOLYCURVE structure [Windows GDI], _win32_TTPOLYCURVE_str, gdi.ttpolycurve, wingdi/LPTTPOLYCURVE, wingdi/TTPOLYCURVE'
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
req.typenames: TTPOLYCURVE, *LPTTPOLYCURVE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTTPOLYCURVE
 - wingdi/tagTTPOLYCURVE
 - LPTTPOLYCURVE
 - wingdi/LPTTPOLYCURVE
 - TTPOLYCURVE
 - wingdi/TTPOLYCURVE
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
 - TTPOLYCURVE
---

# TTPOLYCURVE structure


## -description

The <b>TTPOLYCURVE</b> structure contains information about a curve in the outline of a TrueType character.

## -struct-fields

### -field wType

The type of curve described by the structure. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TT_PRIM_LINE</td>
<td>Curve is a polyline.</td>
</tr>
<tr>
<td>TT_PRIM_QSPLINE</td>
<td>Curve is a quadratic Bézier spline.</td>
</tr>
<tr>
<td>TT_PRIM_CSPLINE</td>
<td>Curve is a cubic Bézier spline.</td>
</tr>
</table>

### -field cpfx

The number of <a href="/windows/desktop/api/wingdi/ns-wingdi-pointfx">POINTFX</a> structures in the array.

### -field apfx

Specifies an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-pointfx">POINTFX</a> structures that define the polyline or Bézier spline.

## -remarks

When an application calls the <a href="/windows/desktop/api/wingdi/nf-wingdi-getglyphoutlinea">GetGlyphOutline</a> function, a glyph outline for a TrueType character is returned in a <a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolygonheader">TTPOLYGONHEADER</a> structure, followed by as many <b>TTPOLYCURVE</b> structures as are required to describe the glyph. All points are returned as <a href="/windows/desktop/api/wingdi/ns-wingdi-pointfx">POINTFX</a> structures and represent absolute positions, not relative moves. The starting point specified by the <b>pfxStart</b> member of the <b>TTPOLYGONHEADER</b> structure is the point at which the outline for a contour begins. The <b>TTPOLYCURVE</b> structures that follow can be either polyline records or spline records.

Polyline records are a series of points; lines drawn between the points describe the outline of the character. Spline records represent the quadratic curves (that is, quadratic b-splines) used by TrueType.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getglyphoutlinea">GetGlyphOutline</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pointfx">POINTFX</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolygonheader">TTPOLYGONHEADER</a>