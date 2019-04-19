---
UID: NF:d2d1helper.Matrix3x2F.Rotation
title: Matrix3x2F::Rotation (d2d1helper.h)
author: windows-sdk-content
description: Creates a rotation transformation that has the specified angle and center point.
old-location: direct2d\matrix3x2f_rotate.htm
tech.root: Direct2D
ms.assetid: 9bb3ee14-3637-41fc-9164-1114619a59e4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D2D1.Matrix3x2F.Rotation, D2D1::Matrix3x2F::Rotation, Matrix3x2F interface [Direct2D],Rotation method, Matrix3x2F.Rotation, Matrix3x2F::Rotation, Rotation, Rotation method [Direct2D], Rotation method [Direct2D],Matrix3x2F interface, d2d1helper/Matrix3x2F::Rotation, direct2d.matrix3x2f_rotate
ms.topic: method
req.header: d2d1helper.h
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
req.namespace: D2D1
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
 - Matrix3x2F.Rotation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Matrix3x2F::Rotation


## -description


Creates a rotation transformation that has the specified angle and center point. 


## -parameters




### -param angle

Type: <b>FLOAT</b>

The rotation angle in degrees. A positive angle creates a clockwise rotation, and a negative angle creates a counterclockwise rotation.


### -param center

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The point about which the rotation is performed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a></b>

The new rotation transformation.




## -remarks



When calling this method, specify a <i>centerPoint</i> to rotate the object about, and the rotation <i>angle</i> in degrees. The following illustration shows a square rotated 45 degrees about its center point.

<img alt="Illustration a square rotated clockwise 45 degrees about the center of the original square" src="./images/rotate_ovw.PNG"/>

#### Examples

The following example uses the <b>D2D1::Matrix3x2F::Rotation</b>  method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the <a href="https://msdn.microsoft.com/en-us/library/Dd742690(v=VS.85).aspx">SetTransform</a> method of the render target (<i>m_pRenderTarget</i>).

The following illustration shows the effect of applying the  preceding rotation transformation to the square. The original square is a dotted outline, and the rotated square is a solid outline. 

<img alt="Illustration a square rotated 45 degrees about the center of the original square" src="./images/rotate_ovw.png"/>


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




<a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a>
 

 

