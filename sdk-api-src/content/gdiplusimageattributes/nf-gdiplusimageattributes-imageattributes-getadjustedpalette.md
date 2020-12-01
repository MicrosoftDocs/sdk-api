---
UID: NF:gdiplusimageattributes.ImageAttributes.GetAdjustedPalette
title: ImageAttributes::GetAdjustedPalette (gdiplusimageattributes.h)
description: The ImageAttributes::GetAdjustedPalette method adjusts the colors in a palette according to the adjustment settings of a specified category.
helpviewer_keywords: ["GetAdjustedPalette","GetAdjustedPalette method [GDI+]","GetAdjustedPalette method [GDI+]","ImageAttributes class","ImageAttributes class [GDI+]","GetAdjustedPalette method","ImageAttributes.GetAdjustedPalette","ImageAttributes::GetAdjustedPalette","_gdiplus_CLASS_ImageAttributes_GetAdjustedPalette_colorPalette_colorAdjustType_","gdiplus._gdiplus_CLASS_ImageAttributes_GetAdjustedPalette_colorPalette_colorAdjustType_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_GetAdjustedPalette_colorPalette_colorAdjustType_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\getadjustedpalette.htm
ms.date: 12/05/2018
ms.keywords: GetAdjustedPalette, GetAdjustedPalette method [GDI+], GetAdjustedPalette method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],GetAdjustedPalette method, ImageAttributes.GetAdjustedPalette, ImageAttributes::GetAdjustedPalette, _gdiplus_CLASS_ImageAttributes_GetAdjustedPalette_colorPalette_colorAdjustType_, gdiplus._gdiplus_CLASS_ImageAttributes_GetAdjustedPalette_colorPalette_colorAdjustType_
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
 - ImageAttributes::GetAdjustedPalette
 - gdiplusimageattributes/ImageAttributes::GetAdjustedPalette
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
 - ImageAttributes.GetAdjustedPalette
---

# ImageAttributes::GetAdjustedPalette


## -description

The <b>ImageAttributes::GetAdjustedPalette</b> method adjusts the colors in a palette according to the adjustment settings of a specified category.

## -parameters

### -param colorPalette [in, out]

Type: <b><a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a> structure that on input, contains the palette to be adjusted and, on output, receives the adjusted palette.

### -param colorAdjustType [in]

Type: <b><a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category whose adjustment settings will be applied to the palette.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

An <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color-remap table for the default category, a different color-remap table for the bitmap category, and still a different color-remap table for the pen category.

When you call <b>ImageAttributes::GetAdjustedPalette</b>, you can specify the adjustment category that is used to adjust the palette colors. For example, if you pass <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeBitmap</a> to the <b>ImageAttributes::GetAdjustedPalette</b> method, then the adjustment settings of the bitmap category are used to adjust the palette colors.


#### Examples



The following example initializes a <a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a> structure with four colors: aqua, black, red, and green. The code also creates an <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object and sets its bitmap remap table so that green will be converted to blue. Then the code adjusts the palette colors by passing the address of the palette to the <b>ImageAttributes::GetAdjustedPalette</b> method of the <b>ImageAttributes</b> object. The code displays the four palette colors twice: once before the adjustment and once after the adjustment.


```cpp

VOID Example_GetAdjustedPalette(HDC hdc)
{
   Graphics graphics(hdc);
   INT j;

   // Create a palette that has four entries.
   ColorPalette* palette = 
      (ColorPalette*)malloc(sizeof(ColorPalette) + 3 * sizeof(ARGB));
   palette->Flags = 0;
   palette->Count = 4;

   palette->Entries[0] = 0xFF00FFFF;   // aqua
   palette->Entries[1] = 0xFF000000;   // black
   palette->Entries[2] = 0xFFFF0000;   // red
   palette->Entries[3] = 0xFF00FF00;   // green
  
   // Display the four palette colors with no adjustment.
   SolidBrush brush(Color());
   for(j = 0; j < 4; ++j)
   {
      brush.SetColor(palette->Entries[j]);
      graphics.FillRectangle(&brush, 30*j, 0, 20, 20);
   }

   // Create a remap table that converts green to blue.
   ColorMap map;
      map.oldColor = Color(255, 0, 255, 0);  // green
      map.newColor = Color(255, 0, 0, 255);  // blue

   // Create an ImageAttributes object, and set its bitmap remap table.
   ImageAttributes imAtt;
   imAtt.SetRemapTable(1, &map, ColorAdjustTypeBitmap);

   // Adjust the palette.
   imAtt.GetAdjustedPalette(palette, ColorAdjustTypeBitmap);

   // Display the four palette colors after the adjustment.
   for(j = 0; j < 4; ++j)
   {
      brush.SetColor(palette->Entries[j]);
      graphics.FillRectangle(&brush, 30*j, 30, 20, 20);
   }
}
				
```


The following illustration shows the output of the preceding code. Note that the green in the original palette was changed to blue.

<img alt="Illustration with two rows of colored rectangles; the last of which is green in Row 1, blue in Row 2" src="./images/imageattributesgetadjustedpalette.png"/>

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a>



<a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/api/gdipluspixelformats/ne-gdipluspixelformats-paletteflags">PaletteFlags</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>