---
UID: NF:gdiplusbrush.TextureBrush.RotateTransform
title: TextureBrush::RotateTransform (gdiplusbrush.h)
description: The TextureBrush::RotateTransform method updates this texture brush's current transformation matrix with the product of itself and a rotation matrix.
helpviewer_keywords: ["RotateTransform","RotateTransform method [GDI+]","RotateTransform method [GDI+]","TextureBrush class","TextureBrush class [GDI+]","RotateTransform method","TextureBrush.RotateTransform","TextureBrush::RotateTransform","_gdiplus_CLASS_TextureBrush_RotateTransform_angle_order_","gdiplus._gdiplus_CLASS_TextureBrush_RotateTransform_angle_order_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_RotateTransform_angle_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\rotatetransform_9angle_order.htm
ms.date: 12/05/2018
ms.keywords: RotateTransform, RotateTransform method [GDI+], RotateTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],RotateTransform method, TextureBrush.RotateTransform, TextureBrush::RotateTransform, _gdiplus_CLASS_TextureBrush_RotateTransform_angle_order_, gdiplus._gdiplus_CLASS_TextureBrush_RotateTransform_angle_order_
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
 - TextureBrush::RotateTransform
 - gdiplusbrush/TextureBrush::RotateTransform
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
 - TextureBrush.RotateTransform
---

# TextureBrush::RotateTransform


## -description

The <b>TextureBrush::RotateTransform</b> method updates this texture brush's current transformation matrix with the product of itself and a rotation matrix.

## -parameters

### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, of rotation.

### -param order [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a> specifies that the rotation matrix is on the left, and <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderAppend</a> specifies that the rotation matrix is on the right. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrderPrepend</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A single 3×3 matrix can store any sequence of affine transformations. If you have several 3×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix R represents a rotation, and matrix T represents a translation. If matrix <i>M</i> is the product <i>RT</i>, then matrix <i>M</i> represents a composite transformation: first rotate, then translate.

The order of matrix multiplication is important. In general, the matrix product <i>RT</i> is not the same as the matrix product <i>TR</i>. In the example given in the previous paragraph, the composite transformation represented by <i>RT</i> (first rotate, then translate) is not the same as the composite transformation represented by <i>TR</i> (first translate, then rotate).


#### Examples



The following example creates a texture brush and sets the transformation of the brush. The code then uses the transformed brush to fill a rectangle.


```cpp
VOID Example_RotateTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"HouseAndTree.Gif");
   TextureBrush textureBrush(&image);
   textureBrush.ScaleTransform(3, 1);                    // first scale
   textureBrush.RotateTransform(30, MatrixOrderAppend);  // then rotate
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



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-scaletransform">TextureBrush::ScaleTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform">TextureBrush::SetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-translatetransform">TextureBrush::TranslateTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>