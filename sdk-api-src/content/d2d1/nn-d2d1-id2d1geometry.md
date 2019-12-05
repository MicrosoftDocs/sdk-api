---
UID: NN:d2d1.ID2D1Geometry
title: ID2D1Geometry (d2d1.h)
description: Represents a geometry resource and defines a set of helper methods for manipulating and measuring geometric shapes. Interfaces that inherit from ID2D1Geometry define specific shapes.
old-location: direct2d\ID2D1Geometry.htm
tech.root: Direct2D
ms.assetid: be4ab801-64f6-48f9-8f62-d0492cc438b1
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry, ID2D1Geometry interface [Direct2D], ID2D1Geometry interface [Direct2D],described, d2d1/ID2D1Geometry, direct2d.ID2D1Geometry
ms.topic: interface
f1_keywords:
- d2d1/ID2D1Geometry
dev_langs:
- c++
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1Geometry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Geometry interface


## -description


Represents a geometry resource and defines a set of helper methods for manipulating and measuring geometric shapes.  Interfaces that inherit from <b>ID2D1Geometry</b> define specific shapes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Geometry</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1Geometry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Geometry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-combinewithgeometry">CombineWithGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Combines this geometry with the specified geometry and stores the result in an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>. 



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-comparewithgeometry">CompareWithGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Describes the intersection between this geometry and the specified geometry. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-computearea">ComputeArea</a>
</td>
<td align="left" width="63%">Overloaded. Computes the area of the geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-computelength">ComputeLength</a>
</td>
<td align="left" width="63%">Overloaded. Calculates the length of the geometry as though each segment were unrolled into a line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-computepointatlength">ComputePointAtLength</a>
</td>
<td align="left" width="63%">Overloaded. Calculates the point and  tangent vector at the specified distance along the geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-fillcontainspoint">FillContainsPoint</a>
</td>
<td align="left" width="63%">Overloaded. Indicates whether the area filled by the geometry would contain the specified point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-getbounds">GetBounds</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves the bounds of the geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-getwidenedbounds">GetWidenedBounds</a>
</td>
<td align="left" width="63%">Overloaded. Gets the bounds of the geometry after it has been widened by the specified stroke width and style and transformed by the specified matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-outline">Outline</a>
</td>
<td align="left" width="63%">Overloaded. Computes the outline of the geometry and writes the result to an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-simplify">Simplify</a>
</td>
<td align="left" width="63%">Overloaded. Creates a simplified version of the geometry that contains only lines and (optionally) cubic Bezier curves and writes the result to an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-strokecontainspoint">StrokeContainsPoint</a>
</td>
<td align="left" width="63%">Overloaded. Determines whether the geometry's stroke contains the specified point.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-tessellate">Tessellate</a>
</td>
<td align="left" width="63%">Overloaded. Creates a set of clockwise-wound triangles that cover the geometry after it has been transformed using the specified matrix and flattened using the specified tolerance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1geometry-widen">Widen</a>
</td>
<td align="left" width="63%">Overloaded. Widens the geometry by the specified stroke and writes the result to an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>.

</td>
</tr>
</table> 


## -remarks



There are several types of Direct2D geometry objects:  a  simple geometry (<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rectanglegeometry">ID2D1RectangleGeometry</a>, <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry">ID2D1RoundedRectangleGeometry</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1ellipsegeometry">ID2D1EllipseGeometry</a>), a path geometry (<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>), or a composite geometry (<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometrygroup">ID2D1GeometryGroup</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1transformedgeometry">ID2D1TransformedGeometry</a>).

 Direct2D geometries enable you to  describe two-dimensional figures and also offer  many uses, such as defining  hit-test regions,  clip regions, and even   animation paths.

Direct2D geometries are immutable and device-independent resources created by <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/resources-and-resource-domains">Resources Overview</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/geometries">Geometry Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>
 

 

