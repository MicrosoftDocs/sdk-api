---
UID: NF:gdipluspath.PathGradientBrush.RotateTransform
title: PathGradientBrush::RotateTransform (gdipluspath.h)
description: The PathGradientBrush::RotateTransform method updates this brush's current transformation matrix with the product of itself and a rotation matrix.
helpviewer_keywords: ["PathGradientBrush class [GDI+]","RotateTransform method","PathGradientBrush.RotateTransform","PathGradientBrush::RotateTransform","RotateTransform","RotateTransform method [GDI+]","RotateTransform method [GDI+]","PathGradientBrush class","_gdiplus_CLASS_PathGradientBrush_RotateTransform_angle_order_","gdiplus._gdiplus_CLASS_PathGradientBrush_RotateTransform_angle_order_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_RotateTransform_angle_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\rotatetransform_38angle_order.htm
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],RotateTransform method, PathGradientBrush.RotateTransform, PathGradientBrush::RotateTransform, RotateTransform, RotateTransform method [GDI+], RotateTransform method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_RotateTransform_angle_order_, gdiplus._gdiplus_CLASS_PathGradientBrush_RotateTransform_angle_order_
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
 - PathGradientBrush::RotateTransform
 - gdipluspath/PathGradientBrush::RotateTransform
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
 - PathGradientBrush.RotateTransform
---

# PathGradientBrush::RotateTransform


## -description

The <b>PathGradientBrush::RotateTransform</b> method updates this brush's current transformation matrix with the product of itself and a rotation matrix.

## -parameters

### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle of rotation in degrees.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a> specifies that the rotation matrix is on the left, and <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderAppend</a> specifies that the rotation matrix is on the right. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a>.

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
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix T represents a translation and matrix R represents a rotation. If matrix M is the product TR, then matrix M represents a composite transformation: first translate, then rotate.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on a triangular path. The calls to the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-scaletransform">PathGradientBrush::ScaleTransform</a> and <b>PathGradientBrush::RotateTransform</b> methods of the 
						<b>PathGradientBrush</b> object set the elements of the brush's transformation matrix so that it represents a composite transformation: first scale, then rotate. The code uses the path gradient brush twice to paint a rectangle: once before the transformation is set and once after the transformation is set.


```cpp
VOID Example_RotateTransform(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path gradient brush based on an array of points.
   Point pts[] = {Point(0, 0), Point(50, 0), Point(50, 50)};
   PathGradientBrush pthGrBrush(pts, 3);

   // Fill an area with the path gradient brush (no transformation).
   graphics.FillRectangle(&pthGrBrush, 0, 0, 500, 500);

   pthGrBrush.ScaleTransform(3.0f, 1.0f);                 // first scale
   pthGrBrush.RotateTransform(60.0f, MatrixOrderAppend);  // then rotate

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



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-scaletransform">PathGradientBrush::ScaleTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-settransform">PathGradientBrush::SetTransform</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-translatetransform">PathGradientBrush::TranslateTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>