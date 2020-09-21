---
UID: NF:gdiplusbrush.TextureBrush.ScaleTransform
title: TextureBrush::ScaleTransform (gdiplusbrush.h)
description: The TextureBrush::ScaleTransform method updates this texture brush's current transformation matrix with the product of itself and a scaling matrix.
helpviewer_keywords: ["ScaleTransform","ScaleTransform method [GDI+]","ScaleTransform method [GDI+]","TextureBrush class","TextureBrush class [GDI+]","ScaleTransform method","TextureBrush.ScaleTransform","TextureBrush::ScaleTransform","_gdiplus_CLASS_TextureBrush_ScaleTransform_sx_sy_order_","gdiplus._gdiplus_CLASS_TextureBrush_ScaleTransform_sx_sy_order_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_ScaleTransform_sx_sy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\scaletransform_32sx_sy_order.htm
ms.date: 12/05/2018
ms.keywords: ScaleTransform, ScaleTransform method [GDI+], ScaleTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],ScaleTransform method, TextureBrush.ScaleTransform, TextureBrush::ScaleTransform, _gdiplus_CLASS_TextureBrush_ScaleTransform_sx_sy_order_, gdiplus._gdiplus_CLASS_TextureBrush_ScaleTransform_sx_sy_order_
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
 - TextureBrush::ScaleTransform
 - gdiplusbrush/TextureBrush::ScaleTransform
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
 - TextureBrush.ScaleTransform
---

# TextureBrush::ScaleTransform


## -description

The <b>TextureBrush::ScaleTransform</b> method updates this texture brush's current transformation matrix with the product of itself and a scaling matrix.

## -parameters

### -param sx [in]

Type: <b>REAL</b>

Real number that specifies the amount to scale in the x direction.

### -param sy [in]

Type: <b>REAL</b>

Real number that specifies the amount to scale in the y direction.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a> specifies that the scaling matrix is on the left, and <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderAppend</a> specifies that the scaling matrix is on the right. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A single 3×3 matrix can store any sequence of affine transformations. If you have several 3×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix <i>T</i> represents a translation, and matrix <i>S</i> represents a scaling. If matrix <i>M</i> is the product <i>TS</i>, then matrix <i>M</i> represents a composite transformation: first translate, then scale.

The order of matrix multiplication is important. In general, the matrix product <i>RT</i> is not the same as the matrix product <i>TR</i>. In the example given in the previous paragraph, the composite transformation represented by <i>RT</i> (first rotate, then translate) is not the same as the composite transformation represented by <i>TR</i> (first translate, then rotate).


#### Examples



The following example creates a texture brush and sets the transformation of the brush. The code then uses the transformed brush to fill a rectangle.


```cpp
VOID Example_ScaleTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"HouseAndTree.Gif");
   TextureBrush textureBrush(&image);
   textureBrush.RotateTransform(30);                      // first rotate
   textureBrush.ScaleTransform(3, 1, MatrixOrderAppend);  // then scale
   graphics.FillRectangle(&textureBrush, 0, 0, 400, 200);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-shapes-with-a-gradient-brush-use">Filling Shapes with a Gradient Brush</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-gettransform">TextureBrush::GetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-multiplytransform">TextureBrush::MultiplyTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-rotatetransform">TextureBrush::RotateTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform">TextureBrush::SetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-translatetransform">TextureBrush::TranslateTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>