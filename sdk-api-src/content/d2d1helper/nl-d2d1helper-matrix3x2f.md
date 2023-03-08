---
UID: NL:d2d1helper.Matrix3x2F
title: Matrix3x2F (d2d1helper.h)
description: The Matrix3x2F class represents a 3-by-2 matrix and provides convenience methods for creating matrices.
helpviewer_keywords: ["Matrix3x2F","Matrix3x2F class [Direct2D]","Matrix3x2F class [Direct2D]","described","d2d1/Matrix3x2F","direct2d.matrix3x2f"]
old-location: direct2d\matrix3x2f.htm
tech.root: Direct2D
ms.assetid: 54b9e75c-6316-44d3-b725-2039f39eeda5
ms.date: 12/05/2018
ms.keywords: Matrix3x2F, Matrix3x2F class [Direct2D], Matrix3x2F class [Direct2D],described, d2d1/Matrix3x2F, direct2d.matrix3x2f
req.header: d2d1helper.h
req.include-header: D2d1helper.h
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
 - Matrix3x2F
 - d2d1helper/Matrix3x2F
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
 - Matrix3x2F
---

# Matrix3x2F class


## -description

The <b>Matrix3x2F</b> class represents a 3-by-2 matrix and provides convenience methods for creating matrices.

## -inheritance

The <b>Matrix3x2F</b> class inherits from <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>.

## -remarks

The <b>Matrix3x2F</b> class 
	  provides many static methods to create 
		  transformation matrices. The following table provides frequently used  methods and the how-to topics associated with them.
		  

<table>
<tr>
<th>Method
		  </th>
<th>How-To
		  </th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew">Skew</a>
</td>
<td>
<a href="/windows/desktop/Direct2D/how-to-skew">How to Skew an Object</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation">Rotation</a>
</td>
<td>
<a href="/windows/desktop/Direct2D/how-to-rotate"> How to Rotate an Object</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)">Scale</a>
</td>
<td>
<a href="/windows/desktop/Direct2D/how-to-scale"> How to Scale an Object</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)">Translation</a>
</td>
<td>
<a href="/windows/desktop/Direct2D/how-to-translate"> How to Translate an Object</a>
</td>
</tr>
</table>
 

Transforms can be applied to objects or to an entire drawing surface.  To apply transforms to an entire drawing surface, call the <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_)">ID2D1RenderTarget::SetTransform</a> method. For individual objects, such as brushes or geometries, call the <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)"> ID2D1Brush::SetTransform</a> method  or the <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>    methods.


#### Examples

The following example uses the <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation">D2D1::Matrix3x2F::Rotation</a>  method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the <a href="/windows/win32/direct2d/id2d1rendertarget-settransform">SetTransform</a> method of the render target (<i>m_pRenderTarget</i>).

The following illustration shows the effect of applying the  preceding rotation transformation to the square. The original square is a dotted outline, and the rotated square is a solid outline. 

<img alt="Illustration a square rotated clockwise 45 degrees about the center of the original square" src="images/rotate_ovw.png"/>


```cpp
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);


```


Code has been omitted from this example. For more information about transforms, see the <a href="/windows/desktop/Direct2D/direct2d-transforms-overview">Transforms Overview</a>. 

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>



<a href="/windows/desktop/Direct2D/direct2d-transforms-overview">Transforms Overview</a>
