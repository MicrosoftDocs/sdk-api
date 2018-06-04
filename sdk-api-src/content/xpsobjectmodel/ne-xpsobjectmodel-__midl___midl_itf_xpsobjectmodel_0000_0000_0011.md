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

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0011 enumeration


## -description


Describes a line segment.


## -enum-fields




### -field XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE

The line segment is an arc that covers more than 180 degrees and is drawn in a clockwise direction from the start point to the end point.


### -field XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE

The line segment is an arc that covers more than 180 degrees and is drawn in a counterclockwise direction from the start point to the end point.


### -field XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE

The line segment is an arc that covers at most 180 degrees and is drawn in a clockwise direction from the start point to the end point.


### -field XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE

The line segment is an arc that covers at most 180 degrees and is drawn in a counterclockwise direction from the start point to the end point.


### -field XPS_SEGMENT_TYPE_BEZIER

The line segment is a cubic Bezier curve that is drawn between two points.


### -field XPS_SEGMENT_TYPE_LINE

The line segment is a straight line that is drawn between two points.


### -field XPS_SEGMENT_TYPE_QUADRATIC_BEZIER

The line segment is a quadratic Bezier curve that is drawn between two points.


## -remarks



A geometry segment is described by the start point, the segment type, and additional parameters whose values are determined by the segment type. The coordinates for the start point of the first segment are a property of the geometry figure. The start point of each subsequent segment is the end point of the preceding segment.

The table that follows shows an example of each segment type.

<table>
<tr>
<th colspan="2">Examples</th>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE figure segment" src="../images/segment_type_arc_lc.png"/>

</td>
<td>
XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE figure segment" src="../images/segment_type_arc_lcc.png"/> 

</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE<img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE figure segment" src="../images/segment_type_arc_sc.png"/> 

</td>
<td>
XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE figure segment" src="../images/segment_type_arc_scc.png"/> 

</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_BEZIER <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_BEZIER figure segment" src="../images/segment_type_bezier.png"/> 

</td>
<td>
  XPS_SEGMENT_TYPE_LINE <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_LINE figure segment" src="../images/segment_type_line.png"/> 

</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_QUADRATIC_BEZIER <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_QUADRATIC_BEZIER figure segment" src="../images/segment_type_quad_bezier.png"/> 

</td>
<td></td>
</tr>
</table>
 




## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

