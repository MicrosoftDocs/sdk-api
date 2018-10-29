---
UID: NS:wingdi.tagTTPOLYCURVE
title: tagTTPOLYCURVE
author: windows-sdk-content
description: The TTPOLYCURVE structure contains information about a curve in the outline of a TrueType character.
old-location: gdi\ttpolycurve.htm
tech.root: gdi
ms.assetid: 59a26aec-786e-471b-8e08-ddffb04874d6
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPTTPOLYCURVE, LPTTPOLYCURVE, LPTTPOLYCURVE structure pointer [Windows GDI], TTPOLYCURVE, TTPOLYCURVE structure [Windows GDI], _win32_TTPOLYCURVE_str, gdi.ttpolycurve, tagTTPOLYCURVE, wingdi/LPTTPOLYCURVE, wingdi/TTPOLYCURVE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - TTPOLYCURVE
product: Windows
targetos: Windows
req.typenames: TTPOLYCURVE, *LPTTPOLYCURVE
req.redist: 
---

# tagTTPOLYCURVE structure


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

The number of <a href="https://msdn.microsoft.com/a8736c6c-7944-42ed-811c-308f41f1ab2f">POINTFX</a> structures in the array.


### -field apfx

Specifies an array of <a href="https://msdn.microsoft.com/a8736c6c-7944-42ed-811c-308f41f1ab2f">POINTFX</a> structures that define the polyline or Bézier spline.


## -remarks



When an application calls the <a href="https://msdn.microsoft.com/08f06007-5b21-44ab-b234-21a58c94ed4e">GetGlyphOutline</a> function, a glyph outline for a TrueType character is returned in a <a href="https://msdn.microsoft.com/eea54aeb-7847-4393-87fa-86de93017be8">TTPOLYGONHEADER</a> structure, followed by as many <b>TTPOLYCURVE</b> structures as are required to describe the glyph. All points are returned as <a href="https://msdn.microsoft.com/a8736c6c-7944-42ed-811c-308f41f1ab2f">POINTFX</a> structures and represent absolute positions, not relative moves. The starting point specified by the <b>pfxStart</b> member of the <b>TTPOLYGONHEADER</b> structure is the point at which the outline for a contour begins. The <b>TTPOLYCURVE</b> structures that follow can be either polyline records or spline records.

Polyline records are a series of points; lines drawn between the points describe the outline of the character. Spline records represent the quadratic curves (that is, quadratic b-splines) used by TrueType.




## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/08f06007-5b21-44ab-b234-21a58c94ed4e">GetGlyphOutline</a>



<a href="https://msdn.microsoft.com/a8736c6c-7944-42ed-811c-308f41f1ab2f">POINTFX</a>



<a href="https://msdn.microsoft.com/eea54aeb-7847-4393-87fa-86de93017be8">TTPOLYGONHEADER</a>
 

 

