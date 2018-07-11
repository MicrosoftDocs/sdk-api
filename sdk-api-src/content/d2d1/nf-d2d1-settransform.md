---
UID: NF:d2d1.SetTransform
title: SetTransform function
author: windows-sdk-content
description: Sets the transformation applied to the brush.
old-location: direct2d\id2d1brush_settransform.htm
old-project: direct2d
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: ID2D1Brush::SetTransform, SetTransform, SetTransform methods [Direct2D], d2d1_1/SetTransform, direct2d.id2d1brush_settransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1.h
req.include-header: D2d1.h
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
tech.root: 
req.typenames: D2D1_WINDOW_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1Brush::SetTransform
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# SetTransform function


## -description


<span>Sets the transformation applied to the brush.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8feb644a-26ea-4718-abd4-6990ffd97a50">SetTransform(D2D1_MATRIX_3X2_F&)</a>
</td>
<td align="left" width="63%">

    Sets the transformation applied to the brush.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef9fdd4f-6338-498e-bbed-5fc676fc53b3">SetTransform(D2D1_MATRIX_3X2_F*)</a>
</td>
<td align="left" width="63%">
Sets the transformation applied to the brush.

</td>
</tr>
</table>

## -parameters


## -remarks



When you paint with a brush, it paints in the coordinate space of the render target. Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target. 

You can "move" the gradient defined by an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> to a target area by setting its start point and end point. Likewise, you can move the gradient defined by an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a> by changing its center and radii. 

To align the content of an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> to the area being painted, you can use the <b>SetTransform</b> method to translate the bitmap to the desired location. This transform only affects the brush; it does not affect any other content drawn by the render target. 

The following illustrations show the effect of using an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> to fill a rectangle located at (100, 100). The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin. As a result, only a portion of the bitmap appears in the rectangle.

The illustration on the right shows the result of transforming the <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> so that its content is shifted 50 pixels to the right and 50 pixels down. The bitmap now fills the rectangle.

<img alt="Illustration of two squares, one painted with a bitmap without a transformed brush and one painted with a transformed brush" src="images/brushes_ovw_transform.png"/>


#### Examples

The following code examples show how to create the transformation shown in the right diagram in the preceding illustration. First apply a translation to the <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>, moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis. Then use the <b>ID2D1BitmapBrush</b> to fill  the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).   

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget-&gt;CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre> // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush-&gt;SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget-&gt;FillRectangle(
     &amp;rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>
 

 

