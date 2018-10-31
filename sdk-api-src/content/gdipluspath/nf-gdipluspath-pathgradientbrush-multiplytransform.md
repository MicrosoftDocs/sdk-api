---
UID: NF:gdipluspath.PathGradientBrush.MultiplyTransform
title: PathGradientBrush::MultiplyTransform
author: windows-sdk-content
description: ThePathGradientBrush::MultiplyTransform method updates the brush's transformation matrix with the product of itself and another matrix.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_MultiplyTransform_matrix_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\multiplytransform_47matrix_order.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: MultiplyTransform, MultiplyTransform method [GDI+], MultiplyTransform method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],MultiplyTransform method, PathGradientBrush.MultiplyTransform, PathGradientBrush::MultiplyTransform, _gdiplus_CLASS_PathGradientBrush_MultiplyTransform_matrix_order_, gdiplus._gdiplus_CLASS_PathGradientBrush_MultiplyTransform_matrix_order_
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
 - PathGradientBrush.MultiplyTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::MultiplyTransform


## -description


The<b>PathGradientBrush::MultiplyTransform</b> method updates the brush's transformation matrix with the product of itself and another matrix.


## -parameters




### -param matrix [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Pointer to the matrix that will be multiplied by the brush's current transformation matrix. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrderPrepend</a> specifies that the passed matrix is on the left, and <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrderAppend</a> specifies that the passed matrix is on the right. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrderPrepend</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



A single 3
				×3 matrix can store any sequence of affine transformations. If you have several 3
				×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix R represents a rotation and matrix T represents a translation. If matrix M is the product RT, then matrix M represents a composite transformation: first rotate, then translate.

The order of matrix multiplication is important. In general, the matrix product RT is not the same as the matrix product TR. In the example given in the previous paragraph, the composite transformation represented by RT (first rotate, then translate) is not the same as the composite transformation represented by TR (first translate, then rotate).


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>object based on a triangular path. The code calls the <a href="https://msdn.microsoft.com/en-us/library/ms535081(v=VS.85).aspx">PathGradientBrush::ScaleTransform</a> method of the 
						<b>PathGradientBrush</b>object to fill the brush's transformation matrix with the elements that represent a horizontal scaling by a factor of 3. Then the code calls the <b>PathGradientBrush::MultiplyTransform</b> method of that same 
						<b>PathGradientBrush</b>object to multiply the brush's existing transformation matrix by a matrix that represents a translation (10 right, 30 down). The MatrixOrderAppend argument indicates that the multiplication is performed with the translation matrix on the right.

After the multiplication, the brush's transformation matrix represents a composite transformation: first scale, then translate. That composite transformation is applied to the brush's boundary path during the call to 
						<a href="https://msdn.microsoft.com/en-us/library/ms535957(v=VS.85).aspx">FillRectangle</a>, so it is the area inside the transformed path that gets painted.


```cpp
VOID Example_MultiplyTransform(HDC hdc)
{
   Graphics graphics(hdc);
   Point pts[] = {Point(0, 0), Point(50, 0), Point(50, 50)};

   // Translate 10 right, 30 down.
   Matrix matrix(1.0f, 0.0f, 0.0f, 1.0f, 10.0f, 30.0f);

   PathGradientBrush pthGrBrush(pts, 3);
   pthGrBrush.ScaleTransform(3.0f, 1.0f);
   pthGrBrush.MultiplyTransform(&matrix, MatrixOrderAppend);

   graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);  
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535073(v=VS.85).aspx">PathGradientBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535079(v=VS.85).aspx">PathGradientBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535080(v=VS.85).aspx">PathGradientBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535081(v=VS.85).aspx">PathGradientBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535091(v=VS.85).aspx">PathGradientBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535093(v=VS.85).aspx">PathGradientBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

