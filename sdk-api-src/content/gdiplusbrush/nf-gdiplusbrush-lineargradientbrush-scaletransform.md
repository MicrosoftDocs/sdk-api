---
UID: NF:gdiplusbrush.LinearGradientBrush.ScaleTransform
title: LinearGradientBrush::ScaleTransform (gdiplusbrush.h)
description: The LinearGradientBrush::ScaleTransform method updates this brush's current transformation matrix with the product of itself and a scaling matrix.
helpviewer_keywords: ["LinearGradientBrush class [GDI+]","ScaleTransform method","LinearGradientBrush.ScaleTransform","LinearGradientBrush::ScaleTransform","ScaleTransform","ScaleTransform method [GDI+]","ScaleTransform method [GDI+]","LinearGradientBrush class","_gdiplus_CLASS_LinearGradientBrush_ScaleTransform_sx_sy_order_","gdiplus._gdiplus_CLASS_LinearGradientBrush_ScaleTransform_sx_sy_order_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_ScaleTransform_sx_sy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\scaletransform_12sx_sy_order.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush class [GDI+],ScaleTransform method, LinearGradientBrush.ScaleTransform, LinearGradientBrush::ScaleTransform, ScaleTransform, ScaleTransform method [GDI+], ScaleTransform method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_ScaleTransform_sx_sy_order_, gdiplus._gdiplus_CLASS_LinearGradientBrush_ScaleTransform_sx_sy_order_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - LinearGradientBrush::ScaleTransform
 - gdiplusbrush/LinearGradientBrush::ScaleTransform
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
 - LinearGradientBrush.ScaleTransform
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

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the scaling matrix is on the left, and MatrixOrderAppend specifies that the scaling matrix is on the right. The default value is MatrixOrderPrepend.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A single 3
				×3 matrix can store any sequence of affine transformations. If you have several 3
				×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3
				×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix T represents a translation, and matrix S represents a scaling. If matrix M is the product TS, then matrix M represents a composite transformation: first translate, then scale.

The order of matrix multiplication is important. In general, the matrix product RT is not the same as the matrix product TR. In the example given in the previous paragraph, the composite transformation represented by RT (first rotate, then translate) is not the same as the composite transformation represented by TR (first translate, then rotate).


#### Examples



The following example creates a linear gradient brush and uses it to fill a rectangle. Next, the code modifies the brush's transformation matrix, applying a composite transformation, and then fills a rectangle with the transformed brush.


```cpp
VOID Example_ScaleTrans(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush(
      Rect(0, 0, 80, 40),
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 0, 255),  // blue
      LinearGradientModeHorizontal);

   // Fill a large area with the linear gradient brush (no transformation).
   myGraphics.FillRectangle(&linGrBrush, 0, 0, 800, 150);

   // Apply a composite transformation: first translate, then scale.
   linGrBrush.TranslateTransform(60, 0);            // horizontal translation
   linGrBrush.ScaleTransform(2, MatrixOrderAppend); // horizontal doubling

   // Fill a large area with the transformed linear gradient brush.
   myGraphics.FillRectangle(&linGrBrush, 0, 200, 800, 150);  
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-shapes-with-a-gradient-brush-use">Filling Shapes with a Gradient Brush</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-multiplytransform">LinearGradientBrush::MultiplyTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-rotatetransform">LinearGradientBrush::RotateTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-translatetransform">LinearGradientBrush::TranslateTransform</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-lineargradientmode">LinearGradientMode</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>