---
UID: NF:gdiplusimageattributes.ImageAttributes.SetRemapTable
title: ImageAttributes::SetRemapTable (gdiplusimageattributes.h)
description: The ImageAttributes::SetRemapTable method sets the color-remap table for a specified category.
helpviewer_keywords: ["ImageAttributes class [GDI+]","SetRemapTable method","ImageAttributes.SetRemapTable","ImageAttributes::SetRemapTable","SetRemapTable","SetRemapTable method [GDI+]","SetRemapTable method [GDI+]","ImageAttributes class","_gdiplus_CLASS_ImageAttributes_SetRemapTable_mapSize_map_type_","gdiplus._gdiplus_CLASS_ImageAttributes_SetRemapTable_mapSize_map_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetRemapTable_mapSize_map_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setremaptable.htm
ms.date: 12/05/2018
ms.keywords: ImageAttributes class [GDI+],SetRemapTable method, ImageAttributes.SetRemapTable, ImageAttributes::SetRemapTable, SetRemapTable, SetRemapTable method [GDI+], SetRemapTable method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetRemapTable_mapSize_map_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetRemapTable_mapSize_map_type_
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
 - ImageAttributes::SetRemapTable
 - gdiplusimageattributes/ImageAttributes::SetRemapTable
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
 - ImageAttributes.SetRemapTable
---

# ImageAttributes::SetRemapTable


## -description

The <b>ImageAttributes::SetRemapTable</b> method sets the color-remap table for a specified category.

## -parameters

### -param mapSize [in]

Type: <b>UINT</b>

<b>INT</b> that specifies the number of elements in the <i>map</i> array.

### -param map [in]

Type: <b>const <a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a> structures that defines the color map.

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the color-remap table is set. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A color-remap table is an array of <a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a> structures. Each <b>ColorMap</b> structure has two <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> objects: one that specifies an old color and one that specifies a corresponding new color. During rendering, any color that matches one of the old colors in the remap table is changed to the corresponding new color.

An <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color remap for the default category, a color-remap table for the bitmap category, and still a different color-remap table for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the color-remap table for the pen category by passing <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetRemapTable</b> method, then none of the default adjustment settings will apply to pens.


#### Examples



The following example creates an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a .bmp file and then draws the image. The code creates an <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object and sets its default remap table so that red is converted to blue. Then the code draws the image again using the color adjustment specified by the remap table.


```cpp

VOID Example_SetRemapTable(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an Image object based on a .bmp file.
   // The image has one red stripe and one green stripe.
   Image image(L"RedGreenStripes.bmp");

   // Create an ImageAttributes object and set its remap table.
   ImageAttributes imageAtt;
   ColorMap cMap;
   cMap.oldColor = Color(255, 255, 0, 0);  // red 
   cMap.newColor = Color(255, 0, 0, 255);  // blue
   imageAtt.SetRemapTable(12, &cMap,
      ColorAdjustTypeDefault);

   // Draw the image with no color adjustment.
   graphics.DrawImage(&image, 10, 10, image.GetWidth(), image.GetHeight());
 
   // Draw the image with red converted to blue.
   graphics.DrawImage(&image,
      Rect(100, 10, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),           // source rect
      UnitPixel,
      &imageAtt);
}
				
```


The following illustration shows the output of the preceding code.

<img alt="Illustration showing a rectangle with red and green regions, then the same rectangle with the red region replaced with blue" src="./images/imageattributessetremaptable.png"/>

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearremaptable">ImageAttributes::ClearRemapTable</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>