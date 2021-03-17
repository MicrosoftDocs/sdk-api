---
UID: NF:gdiplusimageattributes.ImageAttributes.SetColorKey
title: ImageAttributes::SetColorKey (gdiplusimageattributes.h)
description: The ImageAttributes::SetColorKey method sets the color key (transparency range) for a specified category.
helpviewer_keywords: ["ImageAttributes class [GDI+]","SetColorKey method","ImageAttributes.SetColorKey","ImageAttributes::SetColorKey","SetColorKey","SetColorKey method [GDI+]","SetColorKey method [GDI+]","ImageAttributes class","_gdiplus_CLASS_ImageAttributes_SetColorKey_colorLow_colorHigh_type_","gdiplus._gdiplus_CLASS_ImageAttributes_SetColorKey_colorLow_colorHigh_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetColorKey_colorLow_colorHigh_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setcolorkey.htm
ms.date: 12/05/2018
ms.keywords: ImageAttributes class [GDI+],SetColorKey method, ImageAttributes.SetColorKey, ImageAttributes::SetColorKey, SetColorKey, SetColorKey method [GDI+], SetColorKey method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetColorKey_colorLow_colorHigh_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetColorKey_colorLow_colorHigh_type_
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
 - ImageAttributes::SetColorKey
 - gdiplusimageattributes/ImageAttributes::SetColorKey
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
 - ImageAttributes.SetColorKey
---

# ImageAttributes::SetColorKey


## -description

The <b>ImageAttributes::SetColorKey</b> method sets the color key (transparency range) for a specified category.

## -parameters

### -param colorLow [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the low color-key value.

### -param colorHigh [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the high color-key value.

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the color key is set. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

This method sets the high and low color-key values so that arange of colors can be made transparent. Any color that has each of its three components (red, green, blue) between the corresponding components of the high and low color keys is made transparent.

An 
				<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color key for the default category, a different color key for the bitmap category, and still a different color key for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the color key for the pen category by passing <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetColorKey</b> method, then none of the default adjustment settings will apply to pens.


#### Examples



The following example creates an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object from a .bmp file. The code also creates an 
						<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object. The call to <b>ImageAttributes::SetColorKey</b> sets the bitmap color key of the 
						<b>ImageAttributes</b> object so that any color that satisfies all three of the following conditions is made transparent: 
						<ul>
<li>The red component is in the range 100 through 250.</li>
<li>The green component is in the range 95 through 245.</li>
<li>The blue component is in the range 30 through 60.</li>
</ul>



```cpp

VOID Example_SetColorKey(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an Image object based on a BMP file.
   // The image has three horizontal stripes.
   // The color of the top stripe has RGB components (90, 90, 20).
   // The color of the middle stripe has RGB components (150, 150, 150).
   // The color of the bottom stripe has RGB components (130, 130, 40).
   Image image(L"ColorKeyTest.bmp");

   // Create an ImageAttributes object, and set its color key.
   ImageAttributes imAtt;
   imAtt.SetColorKey(
      Color(100, 95, 30),
      Color(250, 245, 60),
      ColorAdjustTypeBitmap);

   // Draw the image. Apply the color key.
   // The bottom stripe of the image will be transparent because
   // 100 <= 130 <= 250 and
   // 95  <= 130 <= 245 and
   // 30  <= 40  <= 60.
   graphics.DrawImage(
      &image, 
      Rect(20, 20, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &imAtt);
}
				
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearcolorkey">ImageAttributes::ClearColorKey</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearthreshold">ImageAttributes::ClearThreshold</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setthreshold">ImageAttributes::SetThreshold</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>