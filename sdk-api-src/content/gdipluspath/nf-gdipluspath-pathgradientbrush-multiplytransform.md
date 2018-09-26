---
UID: NF:gdipluspath.PathGradientBrush.MultiplyTransform
title: PathGradientBrush::MultiplyTransform
author: windows-sdk-content
description: ThePathGradientBrush::MultiplyTransform method updates the brush's transformation matrix with the product of itself and another matrix.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_MultiplyTransform_matrix_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\multiplytransform_47matrix_order.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
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

Type: <b><a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to the matrix that will be multiplied by the brush's current transformation matrix. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a> specifies that the passed matrix is on the left, and <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderAppend</a> specifies that the passed matrix is on the right. The default value is <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a>. 


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
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix R represents a rotation and matrix T represents a translation. If matrix M is the product RT, then matrix M represents a composite transformation: first rotate, then translate.

The order of matrix multiplication is important. In general, the matrix product RT is not the same as the matrix product TR. In the example given in the previous paragraph, the composite transformation represented by RT (first rotate, then translate) is not the same as the composite transformation represented by TR (first translate, then rotate).


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object based on a triangular path. The code calls the <a href="https://msdn.microsoft.com/085a33da-b9d6-4707-b368-200250b0823c">PathGradientBrush::ScaleTransform</a> method of the 
						<b>PathGradientBrush</b>object to fill the brush's transformation matrix with the elements that represent a horizontal scaling by a factor of 3. Then the code calls the <b>PathGradientBrush::MultiplyTransform</b> method of that same 
						<b>PathGradientBrush</b>object to multiply the brush's existing transformation matrix by a matrix that represents a translation (10 right, 30 down). The MatrixOrderAppend argument indicates that the multiplication is performed with the translation matrix on the right.

After the multiplication, the brush's transformation matrix represents a composite transformation: first scale, then translate. That composite transformation is applied to the brush's boundary path during the call to 
						<a href="https://msdn.microsoft.com/eff3454e-f4d7-4cc2-9385-268d9ced2715">FillRectangle</a>, so it is the area inside the transformed path that gets painted.


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




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/f74e7b87-4b8b-4f2e-81a5-d8905b5e6351">PathGradientBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/41b3160d-ce08-413e-b2f6-3d7ad11dbde5">PathGradientBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/00f7172b-2967-4d17-b6a6-daeec6d3eb33">PathGradientBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/085a33da-b9d6-4707-b368-200250b0823c">PathGradientBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/b31fe59b-33fb-4d8a-8b95-fd8b1ed78ac8">PathGradientBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/3e6d8b19-92a7-4e3c-983d-8f13e4a8f4ee">PathGradientBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

