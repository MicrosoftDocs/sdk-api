---
UID: NF:wingdi.PolyDraw
title: PolyDraw function
author: windows-sdk-content
description: The PolyDraw function draws a set of line segments and B&#233;zier curves.
old-location: gdi\polydraw.htm
tech.root: gdi
ms.assetid: 5fd3f285-dcf3-4cd0-915a-236ba7902353
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PT_BEZIERTO, PT_CLOSEFIGURE, PT_LINETO, PT_MOVETO, PolyDraw, PolyDraw function [Windows GDI], _win32_PolyDraw, gdi.polydraw, wingdi/PolyDraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PolyDraw function


## -description


The <b>PolyDraw</b> function draws a set of line segments and Bézier curves.


## -parameters




### -param hdc [in]

A handle to a device context.


### -param apt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structures that contains the endpoints for each line segment and the endpoints and control points for each Bézier curve, in logical units.


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
Specifies that the figure is automatically closed after the PT_LINETO or PT_BEZIERTO type for this point is done. A line is drawn from this point to the most recent PT_MOVETO or <a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a> point.

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



The <b>PolyDraw</b> function can be used in place of consecutive calls to <a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>, <a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a>, and <a href="https://msdn.microsoft.com/0c8d6d6d-d0a3-4188-91ad-934e6f054862">PolyBezierTo</a> functions to draw disjoint figures. The lines and curves are drawn using the current pen and figures are not filled. If there is an active path started by calling <a href="https://msdn.microsoft.com/88be3405-a420-4eb1-935b-099dc3067530">BeginPath</a>, <b>PolyDraw</b> adds to the path.

The points contained in the <i>lppt</i> array and in the <i>lpbTypes</i> array indicate whether each point is part of a <a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveTo</a>, <a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a>, or <a href="https://msdn.microsoft.com/0c8d6d6d-d0a3-4188-91ad-934e6f054862">PolyBezierTo</a> operation. It is also possible to close figures.

This function updates the current position.




## -see-also




<a href="https://msdn.microsoft.com/88be3405-a420-4eb1-935b-099dc3067530">BeginPath</a>



<a href="https://msdn.microsoft.com/0b4daf81-d1d6-45c1-b081-855b7cd8527a">EndPath</a>



<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/0c8d6d6d-d0a3-4188-91ad-934e6f054862">PolyBezierTo</a>



<a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">PolyLine</a>
 

 

