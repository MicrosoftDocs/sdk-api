---
UID: NF:wingdi.PolyDraw
title: PolyDraw function (wingdi.h)
description: The PolyDraw function draws a set of line segments and Bézier curves.
helpviewer_keywords: ["PT_BEZIERTO","PT_CLOSEFIGURE","PT_LINETO","PT_MOVETO","PolyDraw","PolyDraw function [Windows GDI]","_win32_PolyDraw","gdi.polydraw","wingdi/PolyDraw"]
old-location: gdi\polydraw.htm
tech.root: gdi
ms.assetid: 5fd3f285-dcf3-4cd0-915a-236ba7902353
ms.date: 12/05/2018
ms.keywords: PT_BEZIERTO, PT_CLOSEFIGURE, PT_LINETO, PT_MOVETO, PolyDraw, PolyDraw function [Windows GDI], _win32_PolyDraw, gdi.polydraw, wingdi/PolyDraw
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
 - PolyDraw
 - wingdi/PolyDraw
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
api_name:
 - PolyDraw
---

# PolyDraw function


## -description

The <b>PolyDraw</b> function draws a set of line segments and Bézier curves.

## -parameters

### -param hdc [in]

A handle to a device context.

### -param apt [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that contains the endpoints for each line segment and the endpoints and control points for each Bézier curve, in logical units.

### -param aj [in]

A pointer to an array that specifies how each point in the <i>lppt</i> array is used. This parameter can be one of the following values.

<table>
<tr>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PT_MOVETO"></a><a id="pt_moveto"></a><dl>
<dt><b>PT_MOVETO</b></dt>
</dl>
</td>
<td width="60%">
Specifies that this point starts a disjoint figure. This point becomes the new current position.

</td>
</tr>
<tr>
<td width="40%"><a id="PT_LINETO"></a><a id="pt_lineto"></a><dl>
<dt><b>PT_LINETO</b></dt>
</dl>
</td>
<td width="60%">
Specifies that a line is to be drawn from the current position to this point, which then becomes the new current position.

</td>
</tr>
<tr>
<td width="40%"><a id="PT_BEZIERTO"></a><a id="pt_bezierto"></a><dl>
<dt><b>PT_BEZIERTO</b></dt>
</dl>
</td>
<td width="60%">
Specifies that this point is a control point or ending point for a Bézier curve.

PT_BEZIERTO types always occur in sets of three. The current position defines the starting point for the Bézier curve. The first two PT_BEZIERTO points are the control points, and the third PT_BEZIERTO point is the ending point. The ending point becomes the new current position. If there are not three consecutive PT_BEZIERTO points, an error results.

</td>
</tr>
</table>
 

A PT_LINETO or PT_BEZIERTO type can be combined with the following value by using the bitwise operator OR to indicate that the corresponding point is the last point in a figure and the figure is closed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PT_CLOSEFIGURE"></a><a id="pt_closefigure"></a><dl>
<dt><b>PT_CLOSEFIGURE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the figure is automatically closed after the PT_LINETO or PT_BEZIERTO type for this point is done. A line is drawn from this point to the most recent PT_MOVETO or <a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a> point.

This value is combined with the PT_LINETO type for a line, or with the PT_BEZIERTO type of the ending point for a Bézier curve, by using the bitwise operator OR.

The current position is set to the ending point of the closing line.

</td>
</tr>
</table>

### -param cpt [in]

The total number of points in the <i>lppt</i> array, the same as the number of bytes in the <i>lpbTypes</i> array.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>PolyDraw</b> function can be used in place of consecutive calls to <a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-polybezierto">PolyBezierTo</a> functions to draw disjoint figures. The lines and curves are drawn using the current pen and figures are not filled. If there is an active path started by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>, <b>PolyDraw</b> adds to the path.

The points contained in the <i>lppt</i> array and in the <i>lpbTypes</i> array indicate whether each point is part of a <a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveTo</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a>, or <a href="/windows/desktop/api/wingdi/nf-wingdi-polybezierto">PolyBezierTo</a> operation. It is also possible to close figures.

This function updates the current position.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-endpath">EndPath</a>



<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polybezierto">PolyBezierTo</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polyline">PolyLine</a>