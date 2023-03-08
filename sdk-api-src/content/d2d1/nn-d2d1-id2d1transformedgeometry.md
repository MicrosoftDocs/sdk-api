---
UID: NN:d2d1.ID2D1TransformedGeometry
title: ID2D1TransformedGeometry (d2d1.h)
description: Represents a geometry that has been transformed.
helpviewer_keywords: ["ID2D1TransformedGeometry","ID2D1TransformedGeometry interface [Direct2D]","ID2D1TransformedGeometry interface [Direct2D]","described","d2d1/ID2D1TransformedGeometry","direct2d.ID2D1TransformedGeometry"]
old-location: direct2d\ID2D1TransformedGeometry.htm
tech.root: Direct2D
ms.assetid: 5d48eab6-1229-4e54-bfab-602b471b23a4
ms.date: 12/05/2018
ms.keywords: ID2D1TransformedGeometry, ID2D1TransformedGeometry interface [Direct2D], ID2D1TransformedGeometry interface [Direct2D],described, d2d1/ID2D1TransformedGeometry, direct2d.ID2D1TransformedGeometry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1TransformedGeometry
 - d2d1/ID2D1TransformedGeometry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1TransformedGeometry
---

# ID2D1TransformedGeometry interface


## -description

Represents a geometry that has been transformed.

## -inheritance

The <b>ID2D1TransformedGeometry</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>. <b>ID2D1TransformedGeometry</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Using an <b>ID2D1TransformedGeometry</b> rather than transforming a geometry by using a render target's transform enables you to transform a geometry without transforming its stroke.

<h3><a id="Creating_ID2D1TransformedGeometry_Objects"></a><a id="creating_id2d1transformedgeometry_objects"></a><a id="CREATING_ID2D1TRANSFORMEDGEOMETRY_OBJECTS"></a>Creating ID2D1TransformedGeometry Objects</h3>
To create an <b>ID2D1TransformedGeometry</b>, call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)">ID2D1Factory::CreateTransformedGeometry</a> method.

Direct2D geometries are immutable and device-independent resources created by <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.


## Examples

The following example creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry">ID2D1RectangleGeometry</a>, then draws it without transforming it. It produces the output shown in the following illustration.

<img alt="Illustration of a rectangle" src="./images/transformedgeometry2_step1.png"/>

```cpp
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );

```


The next example uses the render target to scale the geometry by a factor of 3, then draws it. The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.

<img alt="Illustration of a smaller rectangle inside a larger rectangle with a thicker stroke" src="./images/transformedgeometry2_step2.png"/>

```cpp
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);

```


The next example uses the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)">CreateTransformedGeometry</a> method to scale the geometry by a factor of 3, then draws it. It produces the output shown in the following illustration. Notice that, although the rectangle is larger, its stroke hasn't increased.

<img alt="Illustration of a smaller rectangle inside a larger rectangle with the same stroke" src="./images/transformedgeometry2_step3.png"/>

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

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

