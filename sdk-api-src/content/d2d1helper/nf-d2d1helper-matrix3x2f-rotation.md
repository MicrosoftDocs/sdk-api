---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# Matrix3x2F::Rotation


## -description


Creates a rotation transformation that has the specified angle and center point. 


## -parameters




### -param angle

Type: <b>FLOAT</b>

The rotation angle in degrees. A positive angle creates a clockwise rotation, and a negative angle creates a counterclockwise rotation.


### -param center






#### - centerPoint

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The point about which the rotation is performed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a></b>

The new rotation transformation.




## -remarks



When calling this method, specify a <i>centerPoint</i> to rotate the object about, and the rotation <i>angle</i> in degrees. The following illustration shows a square rotated 45 degrees about its center point.

<img alt="Illustration a square rotated clockwise 45 degrees about the center of the original square" src="images/rotate_ovw.PNG"/>

#### Examples

The following example uses the <b>D2D1::Matrix3x2F::Rotation</b>  method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the <a href="https://msdn.microsoft.com/57afadc1-88c9-4a5b-a83f-63c4c69182a7">SetTransform</a> method of the render target (<i>m_pRenderTarget</i>).

The following illustration shows the effect of applying the  preceding rotation transformation to the square. The original square is a dotted outline, and the rotated square is a solid outline. 

<img alt="Illustration a square rotated 45 degrees about the center of the original square" src="images/rotate_ovw.png"/>

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget-&gt;DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget-&gt;SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget-&gt;FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget-&gt;DrawRectangle(rectangle, m_pTransformedShapeBrush);

</pre>
</td>
</tr>
</table></span></div>
Code has been omitted from this example. For more information about transforms, see the <a href="https://msdn.microsoft.com/eea8177d-c19e-4972-a9a6-ad5d541b090f">Transforms Overview</a>. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a>
 

 

