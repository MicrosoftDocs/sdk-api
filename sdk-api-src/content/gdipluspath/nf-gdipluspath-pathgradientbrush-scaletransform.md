---
UID: NF:gdipluspath.PathGradientBrush.ScaleTransform
title: PathGradientBrush::ScaleTransform (gdipluspath.h)
description: The PathGradientBrush::ScaleTransform method updates this brush's current transformation matrix with the product of itself and a scaling matrix.
helpviewer_keywords: ["PathGradientBrush class [GDI+]","ScaleTransform method","PathGradientBrush.ScaleTransform","PathGradientBrush::ScaleTransform","ScaleTransform","ScaleTransform method [GDI+]","ScaleTransform method [GDI+]","PathGradientBrush class","_gdiplus_CLASS_PathGradientBrush_ScaleTransform_sx_sy_order_","gdiplus._gdiplus_CLASS_PathGradientBrush_ScaleTransform_sx_sy_order_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_ScaleTransform_sx_sy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\scaletransform_38sx_sy_order.htm
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],ScaleTransform method, PathGradientBrush.ScaleTransform, PathGradientBrush::ScaleTransform, ScaleTransform, ScaleTransform method [GDI+], ScaleTransform method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_ScaleTransform_sx_sy_order_, gdiplus._gdiplus_CLASS_PathGradientBrush_ScaleTransform_sx_sy_order_
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
 - PathGradientBrush::ScaleTransform
 - gdipluspath/PathGradientBrush::ScaleTransform
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
 - PathGradientBrush.ScaleTransform
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

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a> specifies that the scaling matrix is on the left, and <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderAppend</a> specifies that the scaling matrix is on the right. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a>.

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
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix T represents a translation and matrix S represents a scaling. If matrix M is the product TS, then matrix M represents a composite transformation: first translate, then scale.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on a triangular path. The calls to the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-translatetransform">PathGradientBrush::TranslateTransform</a> and <b>PathGradientBrush::ScaleTransform</b> methods of the 
						<b>PathGradientBrush</b> object set the elements of the brush's transformation matrix so that it represents a composite transformation: first translate, then scale. The code uses the path gradient brush twice to paint a rectangle: once before the transformation is set and once after the transformation is set.


```cpp
VOID Example_ScaleTransform(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path gradient brush based on an array of points.
   Point pts[] = {Point(0, 0), Point(50, 0), Point(50, 50)};
   PathGradientBrush pthGrBrush(pts, 3);

   // Fill an area with the path gradient brush (no transformation).
   graphics.FillRectangle(&pthGrBrush, 0, 0, 500, 500);

   pthGrBrush.TranslateTransform(50.0f, 40.0f);               // translate
   pthGrBrush.ScaleTransform(3.0f, 2.0f, MatrixOrderAppend);  // then scale

   // Fill the same area with the transformed path gradient brush.
   graphics.FillRectangle(&pthGrBrush, 0, 0, 500, 500); 
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



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-multiplytransform">PathGradientBrush::MultiplyTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-resettransform">PathGradientBrush::ResetTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-rotatetransform">PathGradientBrush::RotateTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-settransform">PathGradientBrush::SetTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-translatetransform">PathGradientBrush::TranslateTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>