---
UID: NF:gdipluspath.PathGradientBrush.RotateTransform
title: PathGradientBrush::RotateTransform
author: windows-sdk-content
description: The PathGradientBrush::RotateTransform method updates this brush's current transformation matrix with the product of itself and a rotation matrix.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_RotateTransform_angle_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\rotatetransform_38angle_order.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: PathGradientBrush class [GDI+],RotateTransform method, PathGradientBrush.RotateTransform, PathGradientBrush::RotateTransform, RotateTransform, RotateTransform method [GDI+], RotateTransform method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_RotateTransform_angle_order_, gdiplus._gdiplus_CLASS_PathGradientBrush_RotateTransform_angle_order_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.RotateTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# PathGradientBrush::RotateTransform


## -description


The <b>PathGradientBrush::RotateTransform</b> method updates this brush's current transformation matrix with the product of itself and a rotation matrix.


## -parameters




### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle of rotation in degrees. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a> specifies that the rotation matrix is on the left, and <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderAppend</a> specifies that the rotation matrix is on the right. The default value is <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A single 3
				×3 matrix can store any sequence of affine transformations. If you have several 3
				×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix T represents a translation and matrix R represents a rotation. If matrix M is the product TR, then matrix M represents a composite transformation: first translate, then rotate.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object based on a triangular path. The calls to the <a href="https://msdn.microsoft.com/085a33da-b9d6-4707-b368-200250b0823c">PathGradientBrush::ScaleTransform</a> and <b>PathGradientBrush::RotateTransform</b> methods of the 
						<b>PathGradientBrush</b>object set the elements of the brush's transformation matrix so that it represents a composite transformation: first scale, then rotate. The code uses the path gradient brush twice to paint a rectangle: once before the transformation is set and once after the transformation is set.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_RotateTransform(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path gradient brush based on an array of points.
   Point pts[] = {Point(0, 0), Point(50, 0), Point(50, 50)};
   PathGradientBrush pthGrBrush(pts, 3);

   // Fill an area with the path gradient brush (no transformation).
   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 500, 500);

   pthGrBrush.ScaleTransform(3.0f, 1.0f);                 // first scale
   pthGrBrush.RotateTransform(60.0f, MatrixOrderAppend);  // then rotate

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



<a href="https://msdn.microsoft.com/085a33da-b9d6-4707-b368-200250b0823c">PathGradientBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/b31fe59b-33fb-4d8a-8b95-fd8b1ed78ac8">PathGradientBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/3e6d8b19-92a7-4e3c-983d-8f13e4a8f4ee">PathGradientBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

