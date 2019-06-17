---
UID: NF:d2d1.ID2D1Factory.CreateTransformedGeometry
title: ID2D1Factory::CreateTransformedGeometry (d2d1.h)
author: windows-sdk-content
description: Transforms the specified geometry and stores the result as an ID2D1TransformedGeometry object.
old-location: direct2d\id2d1factory_createtransformedgeometry.htm
tech.root: Direct2D
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateTransformedGeometry, CreateTransformedGeometry methods [Direct2D], ID2D1Factory.CreateTransformedGeometry, ID2D1Factory::CreateTransformedGeometry, d2d1/CreateTransformedGeometry, direct2d.id2d1factory_createtransformedgeometry
ms.topic: method
f1_keywords: ["d2d1/ID2D1Factory::CreateTransformedGeometry"]
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory::CreateTransformedGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Factory::CreateTransformedGeometry


## -description


<span>Transforms the specified geometry and stores the result as an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1transformedgeometry">ID2D1TransformedGeometry</a> object. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)">CreateTransformedGeometry(ID2D1Geometry*,D2D_MATRIX_3X2_F*,ID2D1TransformedGeometry**)</a>
</td>
<td align="left" width="63%">
Transforms the specified geometry and stores the result as an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1transformedgeometry">ID2D1TransformedGeometry</a> object. 

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)">CreateTransformedGeometry(ID2D1Geometry*,D2D_MATRIX_3X2_F&,ID2D1TransformedGeometry**)</a>
</td>
<td align="left" width="63%">
Transforms the specified geometry and stores the result as an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1transformedgeometry">ID2D1TransformedGeometry</a> object. 

</td>
</tr>
</table>

## -parameters


## -remarks



Like other resources, a transformed geometry inherits the resource space and threading policy of the factory that created it. This object is immutable.

When stroking a transformed geometry with the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry">DrawGeometry</a> method, the stroke width is not affected by the transform applied to the geometry.  The stroke width is only affected by the world transform.


#### Examples

The following example creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rectanglegeometry">ID2D1RectangleGeometry</a>, then draws it without transforming it. It produces the output shown in the following illustration.

<img alt="Illustration of a rectangle" src="images/transformedgeometry2_step1.png"/>

```cpp
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );

```


The next example uses the render target to scale the geometry by a factor of 3, then draws it. The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.

<img alt="Illustration of a smaller rectangle inside a larger rectangle with a thicker stroke" src="images/transformedgeometry2_step2.png"/>

```cpp
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);

```


The next example uses the <b>CreateTransformedGeometry</b> method to scale the geometry by a factor of 3, then draws it. It produces the output shown in the following illustration. Notice that, although the rectangle is larger, its stroke hasn't increased.

<img alt="Illustration of a smaller rectangle inside a larger rectangle with the same stroke" src="images/transformedgeometry2_step3.png"/>

```cpp
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );

```

```cpp
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>
 

 

