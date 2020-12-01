---
UID: NF:gdiplusbrush.TextureBrush.SetTransform
title: TextureBrush::SetTransform (gdiplusbrush.h)
description: The TextureBrush::SetTransform method sets the transformation matrix of this texture brush.
helpviewer_keywords: ["SetTransform","SetTransform method [GDI+]","SetTransform method [GDI+]","TextureBrush class","TextureBrush class [GDI+]","SetTransform method","TextureBrush.SetTransform","TextureBrush::SetTransform","_gdiplus_CLASS_TextureBrush_SetTransform_matrix_","gdiplus._gdiplus_CLASS_TextureBrush_SetTransform_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_SetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\settransform_41matrix.htm
ms.date: 12/05/2018
ms.keywords: SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],SetTransform method, TextureBrush.SetTransform, TextureBrush::SetTransform, _gdiplus_CLASS_TextureBrush_SetTransform_matrix_, gdiplus._gdiplus_CLASS_TextureBrush_SetTransform_matrix_
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
 - TextureBrush::SetTransform
 - gdiplusbrush/TextureBrush::SetTransform
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
 - TextureBrush.SetTransform
---

# TextureBrush::SetTransform


## -description

The <b>TextureBrush::SetTransform</b> method sets the transformation matrix of this texture brush.

## -parameters

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies the transformation matrix to use.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A 
				<b>TextureBrush</b> object maintains a transformation matrix that can store any affine transformation. When you use a texture brush to fill an area, Windows GDI+ transforms the brush's image according to the brush's transformation matrix and then fills the area. The transformed image exists only during rendering; the image stored in the 
				<b>TextureBrush</b> object is not transformed. For example, suppose you call  and then paint an area with <i>someTextureBrush.ScaleTransform(3)</i> and then paint an area with <i>someTextureBrush</i>. The width of the brush's image triples when the area is painted, but the image stored in <i>someTextureBrush</i> remains unchanged.


#### Examples



The following example creates a texture brush and sets the transformation of the brush. The code then uses the transformed brush to fill an ellipse.


```cpp
VOID Example_SetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Matrix matrix(2, 0, 0, 1, 0, 0);  // Horizontal stretch

   Image image(L"HouseAndTree.gif");
   TextureBrush textureBrush(&image);
   textureBrush.SetTransform(&matrix);
   graphics.FillEllipse(&textureBrush, 0, 0, 400, 200); 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-an-image-texture-use">Filling a Shape with an Image Texture</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-gettransform">TextureBrush::GetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-resettransform">TextureBrush::ResetTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>