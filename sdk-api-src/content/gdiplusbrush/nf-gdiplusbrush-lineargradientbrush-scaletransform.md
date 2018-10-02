---
UID: NF:gdiplusbrush.LinearGradientBrush.ScaleTransform
title: LinearGradientBrush::ScaleTransform
author: windows-sdk-content
description: The LinearGradientBrush::ScaleTransform method updates this brush's current transformation matrix with the product of itself and a scaling matrix.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_ScaleTransform_sx_sy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\scaletransform_12sx_sy_order.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: LinearGradientBrush class [GDI+],ScaleTransform method, LinearGradientBrush.ScaleTransform, LinearGradientBrush::ScaleTransform, ScaleTransform, ScaleTransform method [GDI+], ScaleTransform method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_ScaleTransform_sx_sy_order_, gdiplus._gdiplus_CLASS_LinearGradientBrush_ScaleTransform_sx_sy_order_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusbrush.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - LinearGradientBrush.ScaleTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::ScaleTransform


## -description


The <b>LinearGradientBrush::ScaleTransform</b> method updates this brush's current transformation matrix with the product of itself and a scaling matrix.


## -parameters




### -param sx [in]

Type: <b>REAL</b>

Real number that specifies the amount to scale in the x direction. 


### -param sy [in]

Type: <b>REAL</b>

Real number that specifies the amount to scale in the y direction. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the scaling matrix is on the left, and MatrixOrderAppend specifies that the scaling matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



A single 3
				×3 matrix can store any sequence of affine transformations. If you have several 3
				×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix T represents a translation, and matrix S represents a scaling. If matrix M is the product TS, then matrix M represents a composite transformation: first translate, then scale.

The order of matrix multiplication is important. In general, the matrix product RT is not the same as the matrix product TR. In the example given in the previous paragraph, the composite transformation represented by RT (first rotate, then translate) is not the same as the composite transformation represented by TR (first translate, then rotate).


#### Examples



The following example creates a linear gradient brush and uses it to fill a rectangle. Next, the code modifies the brush's transformation matrix, applying a composite transformation, and then fills a rectangle with the transformed brush.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_ScaleTrans(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush(
      Rect(0, 0, 80, 40),
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 0, 255),  // blue
      LinearGradientModeHorizontal);

   // Fill a large area with the linear gradient brush (no transformation).
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 0, 800, 150);

   // Apply a composite transformation: first translate, then scale.
   linGrBrush.TranslateTransform(60, 0);            // horizontal translation
   linGrBrush.ScaleTransform(2, MatrixOrderAppend); // horizontal doubling

   // Fill a large area with the transformed linear gradient brush.
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 200, 800, 150);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533806(v=VS.85).aspx">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535338(v=VS.85).aspx">LinearGradientBrush::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535340(v=VS.85).aspx">LinearGradientBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535350(v=VS.85).aspx">LinearGradientBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534144(v=VS.85).aspx">LinearGradientMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

