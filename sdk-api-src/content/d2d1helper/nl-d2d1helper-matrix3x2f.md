---
UID: NL:d2d1helper.Matrix3x2F
title: Matrix3x2F
author: windows-sdk-content
description: The Matrix3x2F class represents a 3-by-2 matrix and provides convenience methods for creating matrices.
old-location: direct2d\matrix3x2f.htm
tech.root: Direct2D
ms.assetid: 54b9e75c-6316-44d3-b725-2039f39eeda5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Matrix3x2F, Matrix3x2F class [Direct2D], Matrix3x2F class [Direct2D],described, d2d1/Matrix3x2F, direct2d.matrix3x2f
ms.topic: class
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - Matrix3x2F
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Matrix3x2F class


## -description


The <b>Matrix3x2F</b> class represents a 3-by-2 matrix and provides convenience methods for creating matrices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Matrix3x2F</b> class inherits from <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>. <b>Matrix3x2F</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Operators</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Matrix3x2F</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a78374f-8163-4323-a62d-beeb25cd5bea">Matrix3x2F() Constructor</a>
</td>
<td align="left" width="63%">
Instantiates a new instance of the <b>Matrix3x2F</b> class without initializing the matrix values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4701597-9473-4333-9e6d-60000ccea40e">Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT) Constructor(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)</a>
</td>
<td align="left" width="63%">
Instantiates a new instance of the <b>Matrix3x2F</b> class that contains the specified values.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>Matrix3x2F</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b403b67-11a7-48cf-9e29-ce29f8511749">Determinant</a>
</td>
<td align="left" width="63%">
Calculates the determinant of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4596d43-fbc8-489e-a8fd-d33fb26461cc">Identity</a>
</td>
<td align="left" width="63%">
Creates an identity matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44c5229e-778c-431a-b812-cf2f59c2280c">Invert</a>
</td>
<td align="left" width="63%">
Inverts the matrix, if it is invertible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0af1a04-efcb-4613-9715-f3d6ab60afed">IsIdentity</a>
</td>
<td align="left" width="63%">
Indicates whether this matrix is the identity matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c82752f-1287-45c9-8eec-ad924f650045">IsInvertible</a>
</td>
<td align="left" width="63%">
Indicates whether the matrix is invertible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b78e2d9a-c5a8-4c2b-9e45-c1e95ff3be06">ReinterpretBaseType(*D2D1_MATRIX_3X2_F)(D2D1_MATRIX_3X2_F)</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a> matrix to a <b>Matrix3x2F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bf93ed8-4ca7-4e6f-b2fb-68f896469667">ReinterpretBaseType(const *D2D1_MATRIX_3X2_F )(const D2D1_MATRIX_3X2_F)</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a> matrix to a <b>Matrix3x2F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bb3ee14-3637-41fc-9164-1114619a59e4">Rotation</a>
</td>
<td align="left" width="63%">
Creates a rotation transformation that has the specified angle and center point. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2aa64eb-c69a-4938-91de-1541f1c7844f">Scale(D2D1_SIZE_F,D2D1_POINT_2F)(D2D1_SIZE_F,D2D1_POINT_2F)</a>
</td>
<td align="left" width="63%">
Creates a scale transformation that has the specified scale factors and center point. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/401b8710-c486-44b0-b79c-d7238279fdef">Scale(FLOAT,FLOAT,D2D1_POINT_2F)(FLOAT,FLOAT,D2D1_POINT_2F)</a>
</td>
<td align="left" width="63%">
Creates a scale transformation that has the specified scale factors and center point. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/922524f0-e058-47da-8eaa-ee5a8bc1e315">SetProduct</a>
</td>
<td align="left" width="63%">
Multiplies the two matrices and stores the result in this matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d53aaff-3a6f-4949-9835-a30027d247dd">Skew</a>
</td>
<td align="left" width="63%">
Creates a skew transformation that has the specified x-axis and y-axis values and center point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7c31524-5c29-4c09-b863-6b511ef9ce70">TransformPoint</a>
</td>
<td align="left" width="63%">
Uses this matrix to transform the specified point and returns the result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb289287-4f33-42cf-a306-120adda70371">Translation(D2D1_SIZE_F)(D2D1_SIZE_F)</a>
</td>
<td align="left" width="63%">
Creates a translation transformation that has the specified x and y displacements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec1a15f1-e2d5-482e-b688-10461e736934">Translation(FLOAT,FLOAT)</a>
</td>
<td align="left" width="63%">
Creates a translation transformation that has the specified x and y displacements.

</td>
</tr>
</table> 
<h3><a id="operators"></a>Operators</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Matrix3x2F</b> class has these operators.
<table>
<tr>
<th align="left" width="37%">Operator</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc7eba3e-f97c-4d03-8a83-0c4fd25ef4ce">operator*</a>
</td>
<td align="left" width="63%">
Multiplies this matrix with the specified matrix and returns the result.

</td>
</tr>
</table> 


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
<a href="https://msdn.microsoft.com/7d53aaff-3a6f-4949-9835-a30027d247dd">Skew</a>
</td>
<td>
<a href="https://msdn.microsoft.com/bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff">How to Skew an Object</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9bb3ee14-3637-41fc-9164-1114619a59e4">Rotation</a>
</td>
<td>
<a href="https://msdn.microsoft.com/468e29b6-941b-4cf8-8649-9e513326ccb2"> How to Rotate an Object</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c2aa64eb-c69a-4938-91de-1541f1c7844f">Scale</a>
</td>
<td>
<a href="https://msdn.microsoft.com/3da749e2-50d5-4f4e-9ccd-8c230efe3436"> How to Scale an Object</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/eb289287-4f33-42cf-a306-120adda70371">Translation</a>
</td>
<td>
<a href="https://msdn.microsoft.com/0fc48801-de14-4398-816d-6e7ddf4ffdd7"> How to Translate an Object</a>
</td>
</tr>
</table>
 

Transforms can be applied to objects or to an entire drawing surface.  To apply transforms to an entire drawing surface, call the <a href="https://msdn.microsoft.com/8987ed2c-aafe-43f0-ae56-5915067c8561">ID2D1RenderTarget::SetTransform</a> method. For individual objects, such as brushes or geometries, call the <a href="https://msdn.microsoft.com/8feb644a-26ea-4718-abd4-6990ffd97a50"> ID2D1Brush::SetTransform</a> method  or the <a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>    methods.


#### Examples

The following example uses the <a href="https://msdn.microsoft.com/9bb3ee14-3637-41fc-9164-1114619a59e4">D2D1::Matrix3x2F::Rotation</a>  method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the <a href="https://msdn.microsoft.com/en-us/library/Dd742690(v=VS.85).aspx">SetTransform</a> method of the render target (<i>m_pRenderTarget</i>).

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


Code has been omitted from this example. For more information about transforms, see the <a href="https://msdn.microsoft.com/eea8177d-c19e-4972-a9a6-ad5d541b090f">Transforms Overview</a>. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>



<a href="https://msdn.microsoft.com/eea8177d-c19e-4972-a9a6-ad5d541b090f">Transforms Overview</a>
 

 

