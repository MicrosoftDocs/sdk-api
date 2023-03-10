---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0011
title: XPS_SEGMENT_TYPE (xpsobjectmodel.h)
description: Describes a line segment.
helpviewer_keywords: ["XPS_SEGMENT_TYPE","XPS_SEGMENT_TYPE enumeration [XPS Documents and Packaging]","XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE","XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE","XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE","XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE","XPS_SEGMENT_TYPE_BEZIER","XPS_SEGMENT_TYPE_LINE","XPS_SEGMENT_TYPE_QUADRATIC_BEZIER","xps.xps_segment_type","xpsobjectmodel/XPS_SEGMENT_TYPE","xpsobjectmodel/XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE","xpsobjectmodel/XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE","xpsobjectmodel/XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE","xpsobjectmodel/XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE","xpsobjectmodel/XPS_SEGMENT_TYPE_BEZIER","xpsobjectmodel/XPS_SEGMENT_TYPE_LINE","xpsobjectmodel/XPS_SEGMENT_TYPE_QUADRATIC_BEZIER"]
old-location: xps\xps_segment_type.htm
tech.root: xps
ms.assetid: dc36e80f-0c49-4317-a545-d50c9cbefd03
ms.date: 12/05/2018
ms.keywords: XPS_SEGMENT_TYPE, XPS_SEGMENT_TYPE enumeration [XPS Documents and Packaging], XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE, XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE, XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE, XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE, XPS_SEGMENT_TYPE_BEZIER, XPS_SEGMENT_TYPE_LINE, XPS_SEGMENT_TYPE_QUADRATIC_BEZIER, xps.xps_segment_type, xpsobjectmodel/XPS_SEGMENT_TYPE, xpsobjectmodel/XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE, xpsobjectmodel/XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE, xpsobjectmodel/XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE, xpsobjectmodel/XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE, xpsobjectmodel/XPS_SEGMENT_TYPE_BEZIER, xpsobjectmodel/XPS_SEGMENT_TYPE_LINE, xpsobjectmodel/XPS_SEGMENT_TYPE_QUADRATIC_BEZIER
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_SEGMENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0011
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0011
 - XPS_SEGMENT_TYPE
 - xpsobjectmodel/XPS_SEGMENT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_SEGMENT_TYPE
---

# XPS_SEGMENT_TYPE enumeration


## -description

Describes a line segment.

## -enum-fields

### -field XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE:1

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
XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE figure segment" src="./images/segment_type_arc_lc.png"/>

</td>
<td>
XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE figure segment" src="./images/segment_type_arc_lcc.png"/> 

</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE<img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE figure segment" src="./images/segment_type_arc_sc.png"/> 

</td>
<td>
XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE figure segment" src="./images/segment_type_arc_scc.png"/> 

</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_BEZIER <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_BEZIER figure segment" src="./images/segment_type_bezier.png"/> 

</td>
<td>
  XPS_SEGMENT_TYPE_LINE <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_LINE figure segment" src="./images/segment_type_line.png"/> 

</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_QUADRATIC_BEZIER <img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_QUADRATIC_BEZIER figure segment" src="./images/segment_type_quad_bezier.png"/> 

</td>
<td></td>
</tr>
</table>

## -see-also

<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>

