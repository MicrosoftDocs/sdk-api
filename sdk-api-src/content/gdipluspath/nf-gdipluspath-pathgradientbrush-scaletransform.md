---
UID: NF:gdipluspath.PathGradientBrush.ScaleTransform
title: PathGradientBrush::ScaleTransform
author: windows-sdk-content
description: The PathGradientBrush::ScaleTransform method updates this brush's current transformation matrix with the product of itself and a scaling matrix.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_ScaleTransform_sx_sy_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\scaletransform_38sx_sy_order.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: PathGradientBrush class [GDI+],ScaleTransform method, PathGradientBrush.ScaleTransform, PathGradientBrush::ScaleTransform, ScaleTransform, ScaleTransform method [GDI+], ScaleTransform method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_ScaleTransform_sx_sy_order_, gdiplus._gdiplus_CLASS_PathGradientBrush_ScaleTransform_sx_sy_order_
ms.prod: windows
ms.technology: windows-sdk
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
 - PathGradientBrush.ScaleTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# PathGradientBrush::ScaleTransform


## -description


The <b>PathGradientBrush::ScaleTransform</b> method updates this brush's current transformation matrix with the product of itself and a scaling matrix.


## -parameters




### -param sx [in]

Type: <b>REAL</b>

Real number that specifies the horizontal scale factor. 


### -param sy [in]

Type: <b>REAL</b>

Real number that specifies the vertical scale factor. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrderPrepend</a> specifies that the scaling matrix is on the left, and <a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrderAppend</a> specifies that the scaling matrix is on the right. The default value is <a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrderPrepend</a>. 


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
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix T represents a translation and matrix S represents a scaling. If matrix M is the product TS, then matrix M represents a composite transformation: first translate, then scale.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>
 object based on a triangular path. The calls to the <a href="https://msdn.microsoft.com/library/ms535093(v=VS.85).aspx">PathGradientBrush::TranslateTransform</a> and <b>PathGradientBrush::ScaleTransform</b> methods of the 
						<b>PathGradientBrush</b>
 object set the elements of the brush's transformation matrix so that it represents a composite transformation: first translate, then scale. The code uses the path gradient brush twice to paint a rectangle: once before the transformation is set and once after the transformation is set.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_ScaleTransform(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path gradient brush based on an array of points.
   Point pts[] = {Point(0, 0), Point(50, 0), Point(50, 50)};
   PathGradientBrush pthGrBrush(pts, 3);

   // Fill an area with the path gradient brush (no transformation).
   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 500, 500);

   pthGrBrush.TranslateTransform(50.0f, 40.0f);               // translate
   pthGrBrush.ScaleTransform(3.0f, 2.0f, MatrixOrderAppend);  // then scale

   // Fill the same area with the transformed path gradient brush.
   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 500, 500); 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/library/ms535073(v=VS.85).aspx">PathGradientBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/library/ms535075(v=VS.85).aspx">PathGradientBrush::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/library/ms535079(v=VS.85).aspx">PathGradientBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/library/ms535080(v=VS.85).aspx">PathGradientBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/library/ms535091(v=VS.85).aspx">PathGradientBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/library/ms535093(v=VS.85).aspx">PathGradientBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

