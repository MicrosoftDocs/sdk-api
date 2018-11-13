---
UID: NF:gdiplusbrush.LinearGradientBrush.MultiplyTransform
title: LinearGradientBrush::MultiplyTransform
author: windows-sdk-content
description: The LinearGradientBrush::MultiplyTransform method updates this brush's transformation matrix with the product of itself and another matrix.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_MultiplyTransform_matrix_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\multiplytransform_12matrix_order.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: LinearGradientBrush class [GDI+],MultiplyTransform method, LinearGradientBrush.MultiplyTransform, LinearGradientBrush::MultiplyTransform, MultiplyTransform, MultiplyTransform method [GDI+], MultiplyTransform method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_MultiplyTransform_matrix_order_, gdiplus._gdiplus_CLASS_LinearGradientBrush_MultiplyTransform_matrix_order_
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
 - LinearGradientBrush.MultiplyTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::MultiplyTransform


## -description


The <b>LinearGradientBrush::MultiplyTransform</b> method updates this brush's transformation matrix with the product of itself and another matrix.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a matrix to be multiplied by the brush's current transformation matrix. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the passed matrix is on the left, and MatrixOrderAppend specifies that the passed matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A single 3
				×3 matrix can store any sequence of affine transformations. If you have several 3
				×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix R represents a rotation, and matrix T represents a translation. If matrix M is the product RT, then matrix M represents a composite transformation: first rotate, then translate.

The order of matrix multiplication is important. In general, the matrix product RT is not the same as the matrix product TR. In the example given in the previous paragraph, the composite transformation represented by RT (first rotate, then translate) is not the same as the composite transformation represented by TR (first translate, then rotate).


#### Examples



The following example creates a linear gradient brush and uses it to fill a rectangle. Next, the code sets the brush's transformation matrix, fills a rectangle with the transformed brush, modifies the brush's transformation matrix, and again fills a rectangle with the transformed brush.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_MultTrans(HDC hdc)
{
   Graphics myGraphics(hdc);

   Matrix S(2, 0, 0, 1, 0, 0);   // horizontal doubling
   Matrix T(1, 0, 0, 1, 50, 0);  // horizontal translation of 50 units

   LinearGradientBrush linGrBrush(
      Rect(0, 0, 200, 100),
      Color(255, 255, 0, 0),     // red
      Color(255, 0, 0, 255),     // blue
      LinearGradientModeHorizontal);

   // Fill a large area with the gradient brush (no transformation).
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 0, 800, 100);

   // Apply the scaling transformation.
   linGrBrush.SetTransform(&amp;S);

   // Fill a large area with the scaled gradient brush.
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 150, 800, 100);

   // Form a composite transformation: first scale, then translate.
   linGrBrush.MultiplyTransform(&amp;T, MatrixOrderAppend);

   // Fill a large area with the scaled and translated gradient brush.
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 300, 800, 100);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/e37b4c3a-b753-483a-990f-da3bcc70acf5">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/03a1a931-36a0-434b-b444-f9a6a01fb5b8">LinearGradientBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/ba56470e-59a4-4021-b9ce-bc13c0371007">LinearGradientBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/ccf868a8-b5ea-40f7-b153-90b082a55374">LinearGradientBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

