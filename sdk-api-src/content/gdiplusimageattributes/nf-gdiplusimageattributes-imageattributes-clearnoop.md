---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearNoOp
title: ImageAttributes::ClearNoOp (gdiplusimageattributes.h)
description: The ImageAttributes::ClearNoOp method clears the NoOp setting for a specified category.
helpviewer_keywords: ["ClearNoOp","ClearNoOp method [GDI+]","ClearNoOp method [GDI+]","ImageAttributes class","ImageAttributes class [GDI+]","ClearNoOp method","ImageAttributes.ClearNoOp","ImageAttributes::ClearNoOp","_gdiplus_CLASS_ImageAttributes_ClearNoOp_type_","gdiplus._gdiplus_CLASS_ImageAttributes_ClearNoOp_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearNoOp_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearnoop.htm
ms.date: 12/05/2018
ms.keywords: ClearNoOp, ClearNoOp method [GDI+], ClearNoOp method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearNoOp method, ImageAttributes.ClearNoOp, ImageAttributes::ClearNoOp, _gdiplus_CLASS_ImageAttributes_ClearNoOp_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearNoOp_type_
req.header: gdiplusimageattributes.h
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
 - ImageAttributes::ClearNoOp
 - gdiplusimageattributes/ImageAttributes::ClearNoOp
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
 - ImageAttributes.ClearNoOp
---

# ImageAttributes::ClearNoOp


## -description

The <b>ImageAttributes::ClearNoOp</b> method clears the NoOp setting for a specified category.

## -parameters

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the NoOp setting is cleared. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

You can disable color adjustment for a certain object type by calling the <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setnoop">ImageAttributes::SetNoOp</a> method. Later, you can reinstate color adjustment for that object type by calling the <b>ImageAttributes::ClearNoOp</b> method. For example, the following statement disables color adjustment for brushes:

<code>myImageAttributes.SetNoOp(ColorAdjustTypeBrush);</code>

The following statement reinstates the brush color adjustment that was in place before the call to <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setnoop">ImageAttributes::SetNoOp</a>:
				
				

<code>myImageAttributes.ClearNoOp(ColorAdjustTypeBrush);</code>


#### Examples

The following example creates an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object from a .emf file. The code also creates an <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object. The <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix">ImageAttributes::SetColorMatrix</a> call sets the brush color-adjustment matrix of that <b>ImageAttributes</b> object to a matrix that converts red to green. 

The code calls <a href="/previous-versions/ms536037(v=vs.85)">DrawImage</a> three times, each time passing the address of the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object and the address of the <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object. When the image is drawn the first time, all the red painted by brushes is converted to green. (The red drawn by pens is not changed.) Before the image is drawn the second time, the code calls the <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setnoop">ImageAttributes::SetNoOp</a> method of the <b>ImageAttributes</b> object. So when the image is drawn the second time, no color adjustment is applied to brushes. Before the image is drawn the third time, the code calls the <b>ImageAttributes::ClearNoOp</b> method, which reinstates the brush color-adjustment settings. So when the image is drawn the third time, all the red painted by brushes is converted to green.


```cpp

VOID Example_SetClearNoOp(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"TestMetafile4.emf");
   ImageAttributes imAtt;

    ColorMatrix brushMatrix = {     // red converted to green
      0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
      0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
      0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
      0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
      0.0f, 0.0f, 0.0f, 0.0f, 1.0f};

   imAtt.SetColorMatrix(
      &brushMatrix, 
      ColorMatrixFlagsDefault, 
      ColorAdjustTypeBrush);

   // Draw the image (metafile) using brush color adjustment.
   // Items filled with a brush change from red to green.
   graphics.DrawImage(
      &image,
      Rect(0, 0, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),        // source rect
      UnitPixel,
      &imAtt);

   // Temporarily disable brush color adjustment.
   imAtt.SetNoOp(ColorAdjustTypeBrush);

   // Draw the image (metafile) without brush color adjustment.
   // There is no change from red to green.
   graphics.DrawImage(
      &image,
      Rect(0, 80, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &imAtt);

   // Reinstate brush color adjustment.
   imAtt.ClearNoOp(ColorAdjustTypeBrush);

   // Draw the image (metafile) using brush color adjustment.
   // Items filled with a brush change from red to green.
   graphics.DrawImage(
      &image,
      Rect(0, 160, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &imAtt);
}
				
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-reset">ImageAttributes::Reset</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setnoop">ImageAttributes::SetNoOp</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-settoidentity">ImageAttributes::SetToIdentity</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>