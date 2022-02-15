---
UID: NF:gdipluspath.PathGradientBrush.MultiplyTransform
title: PathGradientBrush::MultiplyTransform (gdipluspath.h)
description: ThePathGradientBrush::MultiplyTransform method updates the brush's transformation matrix with the product of itself and another matrix.
helpviewer_keywords: ["MultiplyTransform","MultiplyTransform method [GDI+]","MultiplyTransform method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","MultiplyTransform method","PathGradientBrush.MultiplyTransform","PathGradientBrush::MultiplyTransform","_gdiplus_CLASS_PathGradientBrush_MultiplyTransform_matrix_order_","gdiplus._gdiplus_CLASS_PathGradientBrush_MultiplyTransform_matrix_order_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_MultiplyTransform_matrix_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\multiplytransform_47matrix_order.htm
ms.date: 12/05/2018
ms.keywords: MultiplyTransform, MultiplyTransform method [GDI+], MultiplyTransform method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],MultiplyTransform method, PathGradientBrush.MultiplyTransform, PathGradientBrush::MultiplyTransform, _gdiplus_CLASS_PathGradientBrush_MultiplyTransform_matrix_order_, gdiplus._gdiplus_CLASS_PathGradientBrush_MultiplyTransform_matrix_order_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - PathGradientBrush::MultiplyTransform
 - gdipluspath/PathGradientBrush::MultiplyTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.MultiplyTransform
---

# PathGradientBrush::MultiplyTransform


## -description

The <b>PathGradientBrush::MultiplyTransform</b> method updates the brush's transformation matrix with the product of itself and another matrix.

## -parameters

### -param matrix [in]

Type: <b><a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to the matrix that will be multiplied by the brush's current transformation matrix.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a> specifies that the passed matrix is on the left, and <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderAppend</a> specifies that the passed matrix is on the right. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A single 3
				×3 matrix can store any sequence of affine transformations. If you have several 3
				×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix R represents a rotation and matrix T represents a translation. If matrix M is the product RT, then matrix M represents a composite transformation: first rotate, then translate.

The order of matrix multiplication is important. In general, the matrix product RT is not the same as the matrix product TR. In the example given in the previous paragraph, the composite transformation represented by RT (first rotate, then translate) is not the same as the composite transformation represented by TR (first translate, then rotate).


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on a triangular path. The code calls the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-scaletransform">PathGradientBrush::ScaleTransform</a> method of the 
						<b>PathGradientBrush</b> object to fill the brush's transformation matrix with the elements that represent a horizontal scaling by a factor of 3. Then the code calls the <b>PathGradientBrush::MultiplyTransform</b> method of that same 
						<b>PathGradientBrush</b> object to multiply the brush's existing transformation matrix by a matrix that represents a translation (10 right, 30 down). The MatrixOrderAppend argument indicates that the multiplication is performed with the translation matrix on the right.

After the multiplication, the brush's transformation matrix represents a composite transformation: first scale, then translate. That composite transformation is applied to the brush's boundary path during the call to 
						<a href="/previous-versions/ms535957(v=vs.85)">FillRectangle</a>, so it is the area inside the transformed path that gets painted.


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

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-gettransform">PathGradientBrush::GetTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-resettransform">PathGradientBrush::ResetTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-rotatetransform">PathGradientBrush::RotateTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-scaletransform">PathGradientBrush::ScaleTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-settransform">PathGradientBrush::SetTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-translatetransform">PathGradientBrush::TranslateTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>