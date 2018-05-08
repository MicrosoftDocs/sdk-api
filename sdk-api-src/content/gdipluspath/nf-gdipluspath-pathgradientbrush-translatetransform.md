---
UID: NF:gdipluspath.PathGradientBrush.TranslateTransform
title: PathGradientBrush::TranslateTransform
author: windows-driver-content
description: The PathGradientBrush::TranslateTransform method updates this brush's current transformation matrix with the product of itself and a translation matrix.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_TranslateTransform_dx_dy_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\translatetransform_44dx_dy_order.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: PathGradientBrush class [GDI+],TranslateTransform method, PathGradientBrush.TranslateTransform, PathGradientBrush::TranslateTransform, TranslateTransform, TranslateTransform method [GDI+], TranslateTransform method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_TranslateTransform_dx_dy_order_, gdiplus._gdiplus_CLASS_PathGradientBrush_TranslateTransform_dx_dy_order_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
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
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	PathGradientBrush.TranslateTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# PathGradientBrush::TranslateTransform


## -description


The <b>PathGradientBrush::TranslateTransform</b> method updates this brush's current transformation matrix with the product of itself and a translation matrix.


## -parameters




### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the horizontal component of the translation. 


### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the vertical component of the translation. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a> specifies that the translation matrix is on the left, and <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderAppend</a> specifies that the translation matrix is on the right. The default value is <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A single 3
				×3 matrix can store any sequence of affine transformations. If you have several 3
				×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix S represents a scaling and matrix T represents a translation. If matrix M is the product ST, then matrix M represents a composite transformation: first scale, then translate.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>
 object based on a triangular path. The calls to the <a href="https://msdn.microsoft.com/085a33da-b9d6-4707-b368-200250b0823c">PathGradientBrush::ScaleTransform</a> and <b>PathGradientBrush::TranslateTransform</b> methods of the 
						<b>PathGradientBrush</b>
 object set the elements of the brush's transformation matrix so that it represents a composite transformation: first scale, then translate. The code uses the path gradient brush twice to paint a rectangle: once before the transformation is set and once after the transformation is set.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_TranslateTrans(HDC hdc)
{
   Graphics graphics(hdc);

   Point pts[] = {Point(0, 0), Point(50, 0), Point(50, 50)};
   PathGradientBrush pthGrBrush(pts, 3);

   // Fill an area with the path gradient brush (no transformation).
   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 500, 500);

   pthGrBrush.ScaleTransform(3.0f, 1.0f);
   pthGrBrush.TranslateTransform(100.0f, 50.0f, MatrixOrderAppend);

   // Fill the same area with the transformed path gradient brush.
   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 500, 500);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/f74e7b87-4b8b-4f2e-81a5-d8905b5e6351">PathGradientBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/96bb8813-1dbf-48ae-adf8-a9a0f3bc210f">PathGradientBrush::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/41b3160d-ce08-413e-b2f6-3d7ad11dbde5">PathGradientBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/00f7172b-2967-4d17-b6a6-daeec6d3eb33">PathGradientBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/085a33da-b9d6-4707-b368-200250b0823c">PathGradientBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/b31fe59b-33fb-4d8a-8b95-fd8b1ed78ac8">PathGradientBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

