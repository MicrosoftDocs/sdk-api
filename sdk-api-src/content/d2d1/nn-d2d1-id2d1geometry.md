---
UID: NN:d2d1.ID2D1Geometry
title: ID2D1Geometry
author: windows-sdk-content
description: Represents a geometry resource and defines a set of helper methods for manipulating and measuring geometric shapes. Interfaces that inherit from ID2D1Geometry define specific shapes.
old-location: direct2d\ID2D1Geometry.htm
tech.root: direct2d
ms.assetid: be4ab801-64f6-48f9-8f62-d0492cc438b1
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ID2D1Geometry, ID2D1Geometry interface [Direct2D], ID2D1Geometry interface [Direct2D],described, d2d1/ID2D1Geometry, direct2d.ID2D1Geometry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Geometry interface


## -description


Represents a geometry resource and defines a set of helper methods for manipulating and measuring geometric shapes.  Interfaces that inherit from <b>ID2D1Geometry</b> define specific shapes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Geometry</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1Geometry</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5bb45c54-c551-4b54-ae91-41d2c57b9570">CombineWithGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Combines this geometry with the specified geometry and stores the result in an <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>. 



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75ddd674-b50b-4d34-b291-9e7e65828304">CompareWithGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Describes the intersection between this geometry and the specified geometry. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/655f11bc-7435-4d23-b4b1-3d7c2110aa48">ComputeArea</a>
</td>
<td align="left" width="63%">Overloaded. Computes the area of the geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4659d880-0aa3-485d-ac71-044d9ace6759">ComputeLength</a>
</td>
<td align="left" width="63%">Overloaded. Calculates the length of the geometry as though each segment were unrolled into a line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b76aa3db-2967-4baa-a449-f664b080fb74">ComputePointAtLength</a>
</td>
<td align="left" width="63%">Overloaded. Calculates the point and  tangent vector at the specified distance along the geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/533a4423-8494-425f-af8b-674a2abc897c">FillContainsPoint</a>
</td>
<td align="left" width="63%">Overloaded. Indicates whether the area filled by the geometry would contain the specified point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3932189a-7c6b-4144-9d4a-32d2aba70835">GetBounds</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves the bounds of the geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1790ff9d-cb30-4cd4-af0d-385a37cad043">GetWidenedBounds</a>
</td>
<td align="left" width="63%">Overloaded. Gets the bounds of the geometry after it has been widened by the specified stroke width and style and transformed by the specified matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec92db79-a1aa-4661-9e75-45a1763af370">Outline</a>
</td>
<td align="left" width="63%">Overloaded. Computes the outline of the geometry and writes the result to an <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6d1d701-c148-4d5b-bf47-00b355bb03ad">Simplify</a>
</td>
<td align="left" width="63%">Overloaded. Creates a simplified version of the geometry that contains only lines and (optionally) cubic Bezier curves and writes the result to an <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a2b058b-4bab-4fa1-ad98-09d3bd32f5ff">StrokeContainsPoint</a>
</td>
<td align="left" width="63%">Overloaded. Determines whether the geometry's stroke contains the specified point.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e0af188-d14b-43c0-be11-16577f054b90">Tessellate</a>
</td>
<td align="left" width="63%">Overloaded. Creates a set of clockwise-wound triangles that cover the geometry after it has been transformed using the specified matrix and flattened using the specified tolerance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c951ab85-7980-41e3-95c4-291d2fb046c8">Widen</a>
</td>
<td align="left" width="63%">Overloaded. Widens the geometry by the specified stroke and writes the result to an <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>.

</td>
</tr>
</table> 


## -remarks



There are several types of Direct2D geometry objects:  a  simple geometry (<a href="https://msdn.microsoft.com/bb5f65ba-34d4-418b-863c-2431046bce8e">ID2D1RectangleGeometry</a>, <a href="https://msdn.microsoft.com/e49e9be7-155a-4487-9931-035f18771c04">ID2D1RoundedRectangleGeometry</a>, or <a href="https://msdn.microsoft.com/4ab6452c-6df8-46c0-9e0d-0cebc19d84ba">ID2D1EllipseGeometry</a>), a path geometry (<a href="https://msdn.microsoft.com/d200563c-d78e-4fa0-a8f2-242b24480e99">ID2D1PathGeometry</a>), or a composite geometry (<a href="https://msdn.microsoft.com/15c3800c-b57c-4c3c-995f-407beee4cc99">ID2D1GeometryGroup</a> and <a href="https://msdn.microsoft.com/5d48eab6-1229-4e54-bfab-602b471b23a4">ID2D1TransformedGeometry</a>).

 Direct2D geometries enable you to  describe two-dimensional figures and also offer  many uses, such as defining  hit-test regions,  clip regions, and even   animation paths.

Direct2D geometries are immutable and device-independent resources created by <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.




## -see-also




<a href="https://msdn.microsoft.com/aaf16fa7-23fd-4020-ae4c-b7832040732d">Geometry Overview</a>



<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>
 

 

