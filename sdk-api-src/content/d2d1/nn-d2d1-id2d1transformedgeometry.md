---
UID: NN:d2d1.ID2D1TransformedGeometry
title: ID2D1TransformedGeometry
author: windows-sdk-content
description: Represents a geometry that has been transformed.
old-location: direct2d\ID2D1TransformedGeometry.htm
tech.root: direct2d
ms.assetid: 5d48eab6-1229-4e54-bfab-602b471b23a4
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ID2D1TransformedGeometry, ID2D1TransformedGeometry interface [Direct2D], ID2D1TransformedGeometry interface [Direct2D],described, d2d1/ID2D1TransformedGeometry, direct2d.ID2D1TransformedGeometry
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
 - ID2D1TransformedGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1TransformedGeometry interface


## -description


Represents a geometry that has been transformed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1TransformedGeometry</b> interface inherits from <a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>. <b>ID2D1TransformedGeometry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1TransformedGeometry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e07c2e4-5f34-4949-bca1-92183652d2fb">GetSourceGeometry</a>
</td>
<td align="left" width="63%">
Retrieves the source geometry of this transformed geometry object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d448af2-49ad-4209-b3a6-b07b40bb3e9d">GetTransform</a>
</td>
<td align="left" width="63%">
Retrieves the matrix used to transform the <b>ID2D1TransformedGeometry</b> object's source geometry.

</td>
</tr>
</table> 


## -remarks



Using an <b>ID2D1TransformedGeometry</b> rather than transforming a geometry by using a render target's transform enables you to transform a geometry without transforming its stroke.

<h3><a id="Creating_ID2D1TransformedGeometry_Objects"></a><a id="creating_id2d1transformedgeometry_objects"></a><a id="CREATING_ID2D1TRANSFORMEDGEOMETRY_OBJECTS"></a>Creating ID2D1TransformedGeometry Objects</h3>
To create an <b>ID2D1TransformedGeometry</b>, call the <a href="https://msdn.microsoft.com/71f26200-0f35-49d7-951d-2962768d16bc">ID2D1Factory::CreateTransformedGeometry</a> method.

Direct2D geometries are immutable and device-independent resources created by <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.


#### Examples

The following example creates an <a href="https://msdn.microsoft.com/bb5f65ba-34d4-418b-863c-2431046bce8e">ID2D1RectangleGeometry</a>, then draws it without transforming it. It produces the output shown in the following illustration.

<img alt="Illustration of a rectangle" src="images/transformedgeometry2_step1.png"/>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>hr = m_pD2DFactory-&gt;CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &amp;m_pRectangleGeometry
    );
</pre>
</td>
</tr>
</table></span></div>
The next example uses the render target to scale the geometry by a factor of 3, then draws it. The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.

<img alt="Illustration of a smaller rectangle inside a larger rectangle with a thicker stroke" src="images/transformedgeometry2_step2.png"/>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget-&gt;SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget-&gt;DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
</pre>
</td>
</tr>
</table></span></div>
The next example uses the <a href="https://msdn.microsoft.com/71f26200-0f35-49d7-951d-2962768d16bc">CreateTransformedGeometry</a> method to scale the geometry by a factor of 3, then draws it. It produces the output shown in the following illustration. Notice that, although the rectangle is larger, its stroke hasn't increased.

<img alt="Illustration of a smaller rectangle inside a larger rectangle with the same stroke" src="images/transformedgeometry2_step3.png"/>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre> // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory-&gt;CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &amp;m_pTransformedGeometry
     );
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Replace the previous render target transform.
m_pRenderTarget-&gt;SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget-&gt;DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

