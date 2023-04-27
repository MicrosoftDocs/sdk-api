---
UID: NF:d2d1.ID2D1Brush.SetTransform(constD2D1_MATRIX_3X2_F&)
title: ID2D1Brush::SetTransform(const D2D1_MATRIX_3X2_F &) (d2d1.h)
description: Sets the transformation applied to the brush. (overload 2/2)
helpviewer_keywords: ["ID2D1Brush interface [Direct2D]","SetTransform method","ID2D1Brush.SetTransform","ID2D1Brush.SetTransform(const D2D1_MATRIX_3X2_F &)","ID2D1Brush::SetTransform","ID2D1Brush::SetTransform(const D2D1_MATRIX_3X2_F &)","ID2D1Brush::SetTransform(const D2D1_MATRIX_3X2_F&)","SetTransform","SetTransform method [Direct2D]","SetTransform method [Direct2D]","ID2D1Brush interface","d2d1/ID2D1Brush::SetTransform","direct2d.ID2D1Brush_SetTransform_ref_D2D_MATRIX_3X2_F"]
old-location: direct2d\ID2D1Brush_SetTransform_ref_D2D_MATRIX_3X2_F.htm
tech.root: Direct2D
ms.assetid: 8feb644a-26ea-4718-abd4-6990ffd97a50
ms.date: 12/05/2018
ms.keywords: ID2D1Brush interface [Direct2D],SetTransform method, ID2D1Brush.SetTransform, ID2D1Brush.SetTransform(const D2D1_MATRIX_3X2_F &), ID2D1Brush::SetTransform, ID2D1Brush::SetTransform(const D2D1_MATRIX_3X2_F &), ID2D1Brush::SetTransform(const D2D1_MATRIX_3X2_F&), SetTransform, SetTransform method [Direct2D], SetTransform method [Direct2D],ID2D1Brush interface, d2d1/ID2D1Brush::SetTransform, direct2d.ID2D1Brush_SetTransform_ref_D2D_MATRIX_3X2_F
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
 - ID2D1Brush::SetTransform
 - d2d1/ID2D1Brush::SetTransform
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
 - ID2D1Brush.SetTransform
---

# ID2D1Brush::SetTransform(const D2D1_MATRIX_3X2_F &)


## -description

Sets the transformation applied to the brush.

## -parameters

### -param transform [ref]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transformation to apply to this brush.

## -remarks

When you paint with a brush, it paints in the coordinate space of the render target. Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target. 

You can "move" the gradient defined by an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a> to a target area by setting its start point and end point. Likewise, you can move the gradient defined by an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a> by changing its center and radii. 

To align the content of an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> to the area being painted, you can use the **SetTransform** method to translate the bitmap to the desired location. This transform only affects the brush; it does not affect any other content drawn by the render target. 

The following illustrations show the effect of using an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> to fill a rectangle located at (100, 100). The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin. As a result, only a portion of the bitmap appears in the rectangle.

The illustration on the right shows the result of transforming the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> so that its content is shifted 50 pixels to the right and 50 pixels down. The bitmap now fills the rectangle.

<img alt="Illustration of two squares, one painted with a bitmap without a transformed brush and one painted with a transformed brush" src="images/brushes_ovw_transform.png"/>


## Examples

The following code examples show how to create the transformation shown in the right diagram in the preceding illustration. First apply a translation to the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>, moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis. Then use the <b>ID2D1BitmapBrush</b> to fill  the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).   


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

```



```cpp
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

```



```cpp
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);


```

```cpp
 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);

```

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>

