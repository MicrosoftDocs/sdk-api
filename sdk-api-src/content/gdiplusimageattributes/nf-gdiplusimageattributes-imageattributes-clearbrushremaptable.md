---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearBrushRemapTable
title: ImageAttributes::ClearBrushRemapTable (gdiplusimageattributes.h)
description: The ImageAttributes::ClearBrushRemapTable method clears the brush color-remap table of this ImageAttributes object.
helpviewer_keywords: ["ClearBrushRemapTable","ClearBrushRemapTable method [GDI+]","ClearBrushRemapTable method [GDI+]","ImageAttributes class","ImageAttributes class [GDI+]","ClearBrushRemapTable method","ImageAttributes.ClearBrushRemapTable","ImageAttributes::ClearBrushRemapTable","_gdiplus_CLASS_ImageAttributes_ClearBrushRemapTable_","gdiplus._gdiplus_CLASS_ImageAttributes_ClearBrushRemapTable_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearBrushRemapTable_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearbrushremaptable.htm
ms.date: 12/05/2018
ms.keywords: ClearBrushRemapTable, ClearBrushRemapTable method [GDI+], ClearBrushRemapTable method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearBrushRemapTable method, ImageAttributes.ClearBrushRemapTable, ImageAttributes::ClearBrushRemapTable, _gdiplus_CLASS_ImageAttributes_ClearBrushRemapTable_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearBrushRemapTable_
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
 - ImageAttributes::ClearBrushRemapTable
 - gdiplusimageattributes/ImageAttributes::ClearBrushRemapTable
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
 - ImageAttributes.ClearBrushRemapTable
---

# ImageAttributes::ClearBrushRemapTable


## -description

The <b>ImageAttributes::ClearBrushRemapTable</b> method clears the brush color-remap table of this <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

An <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify one color-remap table for the default category, a different color-remap table for the bitmap category, and still a different color-remap table for the brush category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the brush category, then the default settings apply to the brush category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a default remap table that converts red to green and you specify a default gamma value of 1.8. If you call <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setbrushremaptable">ImageAttributes::SetBrushRemapTable</a>, then the default remap table (red to green) and the default gamma value (1.8) will not apply to brushes. If you later call <b>ImageAttributes::ClearBrushRemapTable</b>, the brush category will not revert to the default remap table; rather, the brush category will have no remap table. Similarly, the brush category will not revert to the default gamma value; rather, the brush category will have no gamma value.


#### Examples



The following example creates an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object from a .emf file. The code also creates an <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object. The call to <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable">ImageAttributes::SetRemapTable</a> sets the default color-remap table of the <b>ImageAttributes</b> object to a table that converts red to blue. The call to <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setbrushremaptable">ImageAttributes::SetBrushRemapTable</a> sets the brush remap table of the <b>ImageAttributes</b> object to a table that converts red to green.

The code calls <a href="/previous-versions/ms536045(v=vs.85)">DrawImage</a> once to draw the image with no color adjustment. Then the code calls <b>DrawImage</b> three more times, each time passing the address of the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object and the address of the <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object. The second time the image is drawn (after the call to <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable">ImageAttributes::SetRemapTable</a>), all of the red is converted to blue. The third time the image is drawn (after the call to <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setbrushremaptable">ImageAttributes::SetBrushRemapTable</a>), all of the red painted with a brush is converted to green, and the rest of the red is converted to blue. The fourth time the image is drawn (after the call to <b>ImageAttributes::ClearBrushRemapTable</b>), all the red painted with a brush remains unchanged, and the rest of the red is converted to blue.


```cpp

VOID Example_SetClearBrushRemap(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"TestMetafile4.emf");
   ImageAttributes imAtt;

   ColorMap defaultMap;
   defaultMap.oldColor = Color(255, 255, 0, 0);   // red converted to blue
   defaultMap.newColor = Color(255, 0, 0, 255);

   ColorMap brushMap;
   brushMap.oldColor = Color(255, 255, 0, 0);     // red converted to green
   brushMap.newColor = Color(255, 0, 255, 0);

   // Set the default color-remap table.
   imAtt.SetRemapTable(1, &defaultMap, ColorAdjustTypeDefault);

   // Draw the image (metafile) using no color adjustment.
   graphics.DrawImage(
      &image,
      Rect(10, 10, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel);

   // Draw the image (metafile) using default color adjustment.
   // All red is converted to blue.
   graphics.DrawImage(
      &image,
      Rect(10, 90, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &imAtt);

   // Set the brush remap table.
   imAtt.SetBrushRemapTable(1, &brushMap);

   // Draw the image (metafile) using default and brush adjustment.
   // Red painted with a brush is converted to green.
   // All other red is converted to blue (default).
   graphics.DrawImage(
      &image,
      Rect(10, 170, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),           // source rect
      UnitPixel,
      &imAtt);

   // Clear the brush remap table.
   imAtt.ClearBrushRemapTable();

   // Draw the image (metafile) using only default color adjustment.
   // Red painted with a brush gets no color adjustment.
   // All other red is converted to blue (default).
   graphics.DrawImage(
      &image,
      Rect(10, 250, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),           // source rect
      UnitPixel,
      &imAtt);  
}
				
```


The preceding code, along with a particular file, Testmetafile4.emf, produced the following output. The ellipses in the left column were drawn with a pen, and the ellipses in the right column were filled with a brush. Note that the default remap table applies to the ellipses drawn with a pen. The remap table that applies to the ellipses filled with a brush varies according to the <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setbrushremaptable">ImageAttributes::SetBrushRemapTable</a> and <b>ImageAttributes::ClearBrushRemapTable</b> calls.

<img alt="Illustration showing four empty ellipses; the first is red and the rest blue, then four filled ellipses: red, blue, green, and red" src="./images/imageattributesclearbrushremap.png"/>

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormap">ColorMap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearremaptable">ImageAttributes::ClearRemapTable</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setbrushremaptable">ImageAttributes::SetBrushRemapTable</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable">ImageAttributes::SetRemapTable</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>
