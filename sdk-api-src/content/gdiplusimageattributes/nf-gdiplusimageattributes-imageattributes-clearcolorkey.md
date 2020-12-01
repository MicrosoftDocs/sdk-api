---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearColorKey
title: ImageAttributes::ClearColorKey (gdiplusimageattributes.h)
description: The ImageAttributes::ClearColorKey method clears the color key (transparency range) for a specified category.
helpviewer_keywords: ["ClearColorKey","ClearColorKey method [GDI+]","ClearColorKey method [GDI+]","ImageAttributes class","ImageAttributes class [GDI+]","ClearColorKey method","ImageAttributes.ClearColorKey","ImageAttributes::ClearColorKey","_gdiplus_CLASS_ImageAttributes_ClearColorKey_type_","gdiplus._gdiplus_CLASS_ImageAttributes_ClearColorKey_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearColorKey_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearcolorkey.htm
ms.date: 12/05/2018
ms.keywords: ClearColorKey, ClearColorKey method [GDI+], ClearColorKey method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearColorKey method, ImageAttributes.ClearColorKey, ImageAttributes::ClearColorKey, _gdiplus_CLASS_ImageAttributes_ClearColorKey_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearColorKey_type_
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
 - ImageAttributes::ClearColorKey
 - gdiplusimageattributes/ImageAttributes::ClearColorKey
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
 - ImageAttributes.ClearColorKey
---

# ImageAttributes::ClearColorKey


## -description

The <b>ImageAttributes::ClearColorKey</b> method clears the color key (transparency range) for a specified category.

## -parameters

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the color key is cleared. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

An <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify one color key for the default category, a different color key for the bitmap category, and still a different color key for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a default color key that makes any color with a red component from 200 through 255 transparent and you specify a default gamma value of 1.8. If you set the color key of the pen category by calling <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolorkey">ImageAttributes::SetColorKey</a>, then the default color key and the default gamma value will not apply to pens. If you later clear the pen color key by calling <b>ImageAttributes::ClearColorKey</b>, the pen category will not revert to the default color key; rather, the pen category will have no color key. Similarly, the pen category will not revert to the default gamma value; rather, the pen category will have no gamma value.


#### Examples



The following example creates an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object from a .emf file. The code also creates an <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object. The first call to <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolorkey">ImageAttributes::SetColorKey</a> sets the default color key of the 
<b>ImageAttributes</b> object so that colors with a red component from 80 through 120 are transparent. The second call to <b>ImageAttributes::SetColorKey</b> sets the pen color key of the <b>ImageAttributes</b> object so that all colors with a red component from 135 through 175 are transparent.

The code calls <a href="/previous-versions/ms536045(v=vs.85)">DrawImage</a> once to draw the image with no color adjustment. Then the code calls <b>DrawImage</b> three more times, each time passing the address of the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object and the address of the <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object. The second time the image is drawn (after the call that sets the default color key), all of the red from 80 through 120 is transparent. The third time the image is drawn (after the call that sets the pen color key), all of the red from 135 through 175 that is drawn with a pen is transparent. Also, all of the red from 80 through 120 that is not drawn with a pen is transparent. The fourth time the image is drawn (after the call to <b>ImageAttributes::ClearColorKey</b>), none of the red drawn with a pen is transparent. Also, all of the red from 80 through 120 that is not drawn with a pen is transparent.


```cpp

VOID Example_SetClearColorKey(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"TestMetafile5.emf");
   ImageAttributes imAtt;

   // Draw the image (metafile) using no color adjustment.
   graphics.DrawImage(
      &image,
      Rect(0, 0, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),        // source rect
      UnitPixel);

   // Set the default color key.
   imAtt.SetColorKey(
      Color(0, 80, 0, 0),
      Color(255, 120, 255, 255),
      ColorAdjustTypeDefault);

   // Draw the image (metafile) using default color adjustment.
   // Colors with red components from 80 through 120 are transparent.
   graphics.DrawImage(
      &image,
      Rect(0, 100, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &imAtt);

   // Set the pen color key.
   imAtt.SetColorKey(
      Color(0, 135, 0, 0),
      Color(255, 175, 255, 255),
      ColorAdjustTypePen);

   // Draw the image (metafile) using default and pen adjustment.
   // Colors drawn with a pen that have red components from 135 through 175
   // are transparent. Colors not drawn with a pen that have red components
   // from 80 to 120 are transparent.
   graphics.DrawImage(
      &image,
      Rect(0, 200, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &imAtt);

   // Clear the pen color key.
   imAtt.ClearColorKey(ColorAdjustTypePen);

   // Draw the image (metafile) using only default color adjustment.
   // No colors drawn with a pen are transparent. Colors not drawn with 
   // a pen that have red components from 80 to 120 are transparent.
   graphics.DrawImage(
      &image,
      Rect(0, 300, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &imAtt); 
}
				
```


The preceding code, along with a particular file, TestMetafile5.png, produced the following output. The bars in the left column were drawn with a pen, and the bars in the right column were filled with a brush. The default color key applies to the bars filled with a brush. The color key that applies to the bars drawn with a pen varies according to the <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolorkey">ImageAttributes::SetColorKey</a> and <b>ImageAttributes::ClearColorKey</b> calls.

<img alt="Illustration showing bars in four rows of two columns each; the last two have unequal numbers of bars in each row" src="./images/imageattributesclearcolorkey.png"/>

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearthreshold">ImageAttributes::ClearThreshold</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolorkey">ImageAttributes::SetColorKey</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setthreshold">ImageAttributes::SetThreshold</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>