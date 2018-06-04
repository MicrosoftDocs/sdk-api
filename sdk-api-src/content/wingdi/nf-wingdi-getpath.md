---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# GetPath function


## -description


The <b>GetPath</b> function retrieves the coordinates defining the endpoints of lines and the control points of curves found in the path that is selected into the specified device context.


## -parameters




### -param hdc [in]

A handle to a device context that contains a closed path.


### -param apt

TBD


### -param aj

TBD


### -param cpt

TBD




#### - lpPoints [out]

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structures that receives the line endpoints and curve control points, in logical coordinates.


#### - lpTypes [out]

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
 


#### - nSize [in]

The total number of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structures that can be stored in the array pointed to by <i>lpPoints</i>. This value must be the same as the number of bytes that can be placed in the array pointed to by <i>lpTypes</i>.


## -returns



If the <i>nSize</i> parameter is nonzero, the return value is the number of points enumerated. If <i>nSize</i> is 0, the return value is the total number of points in the path (and <b>GetPath</b> writes nothing to the buffers). If <i>nSize</i> is nonzero and is less than the number of points in the path, the return value is 1.




## -remarks



The device context identified by the <i>hdc</i> parameter must contain a closed path.

The points of the path are returned in logical coordinates. Points are stored in the path in device coordinates, so <b>GetPath</b> changes the points from device coordinates to logical coordinates by using the inverse of the current transformation.

The <a href="https://msdn.microsoft.com/267b0c9a-25d4-4b04-95d3-6b0856bed022">FlattenPath</a> function may be called before <b>GetPath</b> to convert all curves in the path into line segments.




## -see-also




<a href="https://msdn.microsoft.com/267b0c9a-25d4-4b04-95d3-6b0856bed022">FlattenPath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>



<a href="https://msdn.microsoft.com/5fd3f285-dcf3-4cd0-915a-236ba7902353">PolyDraw</a>



<a href="https://msdn.microsoft.com/c994bd1b-c5e8-46e6-a6a6-59e2d9106d75">WidenPath</a>
 

 

