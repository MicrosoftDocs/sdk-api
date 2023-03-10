---
UID: NF:gdiplusbrush.TextureBrush.ResetTransform
title: TextureBrush::ResetTransform (gdiplusbrush.h)
description: The TextureBrush::ResetTransform method resets the transformation matrix of this texture brush to the identity matrix. This means that no transformation takes place.
helpviewer_keywords: ["ResetTransform","ResetTransform method [GDI+]","ResetTransform method [GDI+]","TextureBrush class","TextureBrush class [GDI+]","ResetTransform method","TextureBrush.ResetTransform","TextureBrush::ResetTransform","_gdiplus_CLASS_TextureBrush_ResetTransform_","gdiplus._gdiplus_CLASS_TextureBrush_ResetTransform_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_ResetTransform_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\resettransform_13.htm
ms.date: 12/05/2018
ms.keywords: ResetTransform, ResetTransform method [GDI+], ResetTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],ResetTransform method, TextureBrush.ResetTransform, TextureBrush::ResetTransform, _gdiplus_CLASS_TextureBrush_ResetTransform_, gdiplus._gdiplus_CLASS_TextureBrush_ResetTransform_
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
 - TextureBrush::ResetTransform
 - gdiplusbrush/TextureBrush::ResetTransform
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
 - TextureBrush.ResetTransform
---

# TextureBrush::ResetTransform


## -description

The <b>TextureBrush::ResetTransform</b> method resets the transformation matrix of this texture brush to the identity matrix. This means that no transformation takes place.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Setting the transformation matrix to the identity matrix guarantees that no transformation is done. This method is often used to reset the transformation before making any adjustments (scaling, rotating, and so on) to it.


#### Examples



The following example creates a texture brush and sets the transformation of the brush. Next, the code uses the transformed brush to fill a rectangle. Then, the code resets the transformation of the brush and uses the untransformed brush to fill a rectangle.


```cpp
VOID Example_ResetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a texture brush, and set its transformation.
   Image image(L"HouseAndTree.Gif");
   TextureBrush textureBrush(&image);
   textureBrush.RotateTransform(30);

   // Fill a rectangle with the transformed texture brush.
   graphics.FillRectangle(&textureBrush, 0, 0, 200, 100);

   textureBrush.ResetTransform();
   
   // Fill a rectangle with the texture brush (no transformation).
   graphics.FillRectangle(&textureBrush, 250, 0, 200, 100);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-an-image-texture-use">Filling a Shape with an Image Texture</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-gettransform">TextureBrush::GetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-multiplytransform">TextureBrush::MultiplyTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-rotatetransform">TextureBrush::RotateTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-scaletransform">TextureBrush::ScaleTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform">TextureBrush::SetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-translatetransform">TextureBrush::TranslateTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
