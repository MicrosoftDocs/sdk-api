---
UID: NF:gdiplusbrush.TextureBrush.GetTransform
title: TextureBrush::GetTransform (gdiplusbrush.h)
description: The TextureBrush::GetTransform method gets the transformation matrix of this texture brush.
helpviewer_keywords: ["GetTransform","GetTransform method [GDI+]","GetTransform method [GDI+]","TextureBrush class","TextureBrush class [GDI+]","GetTransform method","TextureBrush.GetTransform","TextureBrush::GetTransform","_gdiplus_CLASS_TextureBrush_GetTransform_matrix_","gdiplus._gdiplus_CLASS_TextureBrush_GetTransform_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_GetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\gettransform_92matrix.htm
ms.date: 12/05/2018
ms.keywords: GetTransform, GetTransform method [GDI+], GetTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],GetTransform method, TextureBrush.GetTransform, TextureBrush::GetTransform, _gdiplus_CLASS_TextureBrush_GetTransform_matrix_, gdiplus._gdiplus_CLASS_TextureBrush_GetTransform_matrix_
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
 - TextureBrush::GetTransform
 - gdiplusbrush/TextureBrush::GetTransform
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
 - TextureBrush.GetTransform
---

# TextureBrush::GetTransform


## -description

The <b>TextureBrush::GetTransform</b> method gets the transformation matrix of this texture brush.

## -parameters

### -param matrix [out]

Type: <b><a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that receives the transformation matrix.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A 
				<b>TextureBrush</b> object maintains a transformation matrix that can store any affine transformation. When you use a texture brush to fill an area, GDI+ transforms the brush's image according to the brush's transformation matrix and then fills the area. The transformed image exists only during rendering; the image stored in the 
				<b>TextureBrush</b> object is not transformed. For example, suppose you call <i>someTextureBrush.ScaleTransform(3)</i> and then paint an area with <i>someTextureBrush</i>. The width of the brush's image triples when the area is painted, but the image stored in <i>someTextureBrush</i> remains unchanged.


#### Examples



The following example creates a texture brush and sets the transformation of the brush. The code then gets the brush's transformation matrix and proceeds to inspect or use the elements.


```cpp
VOID Example_GetTransform(HDC hdc)
{
   Graphics graphics(hdc);
  
   // Create a texture brush, and set its transform.
   Image image(L"marble.jpg");
   TextureBrush textureBrush(&image);
   textureBrush.ScaleTransform(3, 2);

   // Obtain information about the texture brush.
   Matrix matrix;
   REAL elements[6];

   textureBrush.GetTransform(&matrix);
   matrix.GetElements(elements);

   for(INT j = 0; j <=5; ++j)
   {
      // Inspect or use the value in elements[j].
   }
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-an-image-texture-use">Filling a Shape with an Image Texture</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-resettransform">TextureBrush::ResetTransform</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform">TextureBrush::SetTransform</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>