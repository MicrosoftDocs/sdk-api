---
UID: NF:wingdi.GetPath
title: GetPath function (wingdi.h)
description: The GetPath function retrieves the coordinates defining the endpoints of lines and the control points of curves found in the path that is selected into the specified device context.
helpviewer_keywords: ["GetPath","GetPath function [Windows GDI]","PT_BEZIERTO","PT_CLOSEFIGURE","PT_LINETO","PT_MOVETO","_win32_GetPath","gdi.getpath","wingdi/GetPath"]
old-location: gdi\getpath.htm
tech.root: gdi
ms.assetid: 2dc7736a-03fc-4623-a566-6c3e368da174
ms.date: 12/05/2018
ms.keywords: GetPath, GetPath function [Windows GDI], PT_BEZIERTO, PT_CLOSEFIGURE, PT_LINETO, PT_MOVETO, _win32_GetPath, gdi.getpath, wingdi/GetPath
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
 - GetPath
 - wingdi/GetPath
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
 - GetPath
---

# GetPath function


## -description

The <b>GetPath</b> function retrieves the coordinates defining the endpoints of lines and the control points of curves found in the path that is selected into the specified device context.

## -parameters

### -param hdc [in]

A handle to a device context that contains a closed path.

### -param apt [out]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that receives the line endpoints and curve control points, in logical coordinates.

### -param aj [out]

A pointer to an array of bytes that receives the vertex types. This parameter can be one of the following values.

<table>
<tr>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="PT_MOVETO"></a><a id="pt_moveto"></a><dl>
<dt><b>PT_MOVETO</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the corresponding point in the <i>lpPoints</i> parameter starts a disjoint figure.

</td>
</tr>
<tr>
<td width="40%"><a id="PT_LINETO"></a><a id="pt_lineto"></a><dl>
<dt><b>PT_LINETO</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the previous point and the corresponding point in <i>lpPoints</i> are the endpoints of a line.

</td>
</tr>
<tr>
<td width="40%"><a id="PT_BEZIERTO"></a><a id="pt_bezierto"></a><dl>
<dt><b>PT_BEZIERTO</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the corresponding point in <i>lpPoints</i> is a control point or ending point for a Bézier curve.

PT_BEZIERTO values always occur in sets of three. The point in the path immediately preceding them defines the starting point for the Bézier curve. The first two PT_BEZIERTO points are the control points, and the third PT_BEZIERTO point is the ending (if hard-coded) point.

</td>
</tr>
</table>
 

A PT_LINETO or PT_BEZIERTO value may be combined with the following value (by using the bitwise operator OR) to indicate that the corresponding point is the last point in a figure and the figure should be closed.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="PT_CLOSEFIGURE"></a><a id="pt_closefigure"></a><dl>
<dt><b>PT_CLOSEFIGURE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the figure is automatically closed after the corresponding line or curve is drawn. The figure is closed by drawing a line from the line or curve endpoint to the point corresponding to the last PT_MOVETO.

</td>
</tr>
</table>

### -param cpt [in]

The total number of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that can be stored in the array pointed to by <i>lpPoints</i>. This value must be the same as the number of bytes that can be placed in the array pointed to by <i>lpTypes</i>.

## -returns

If the <i>nSize</i> parameter is nonzero, the return value is the number of points enumerated. If <i>nSize</i> is 0, the return value is the total number of points in the path (and <b>GetPath</b> writes nothing to the buffers). If <i>nSize</i> is nonzero and is less than the number of points in the path, the return value is 1.

## -remarks

The device context identified by the <i>hdc</i> parameter must contain a closed path.

The points of the path are returned in logical coordinates. Points are stored in the path in device coordinates, so <b>GetPath</b> changes the points from device coordinates to logical coordinates by using the inverse of the current transformation.

The <a href="/windows/desktop/api/wingdi/nf-wingdi-flattenpath">FlattenPath</a> function may be called before <b>GetPath</b> to convert all curves in the path into line segments.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-flattenpath">FlattenPath</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polydraw">PolyDraw</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-widenpath">WidenPath</a>