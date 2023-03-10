---
UID: NF:gdiplusimageattributes.ImageAttributes.SetThreshold
title: ImageAttributes::SetThreshold (gdiplusimageattributes.h)
description: The ImageAttributes::SetThreshold method sets the threshold (transparency range) for a specified category.
helpviewer_keywords: ["ImageAttributes class [GDI+]","SetThreshold method","ImageAttributes.SetThreshold","ImageAttributes::SetThreshold","SetThreshold","SetThreshold method [GDI+]","SetThreshold method [GDI+]","ImageAttributes class","_gdiplus_CLASS_ImageAttributes_SetThreshold_threshold_type_","gdiplus._gdiplus_CLASS_ImageAttributes_SetThreshold_threshold_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetThreshold_threshold_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setthreshold.htm
ms.date: 12/05/2018
ms.keywords: ImageAttributes class [GDI+],SetThreshold method, ImageAttributes.SetThreshold, ImageAttributes::SetThreshold, SetThreshold, SetThreshold method [GDI+], SetThreshold method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetThreshold_threshold_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetThreshold_threshold_type_
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
 - ImageAttributes::SetThreshold
 - gdiplusimageattributes/ImageAttributes::SetThreshold
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
 - ImageAttributes.SetThreshold
---

# ImageAttributes::SetThreshold


## -description

The <b>ImageAttributes::SetThreshold</b> method sets the threshold (transparency range) for a specified category.

## -parameters

### -param threshold [in]

Type: <b>REAL</b>

<b>REAL</b> number that specifies the threshold value.

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the color threshold is set. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The threshold is a value from 0 through 1 that specifies a cutoff point for each color component. For example, suppose the threshold is set to 0.7, and suppose you are rendering a color whose red, green, and blue components are 230, 50, and 220. The red component, 230, is greater than 0.7×255, so the red component will be changed to 255 (full intensity). The green component, 50, is less than 0.7×255, so the green component will be changed to 0. The blue component, 220, is greater than 0.7×255, so the blue component will be changed to 255.

An <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a threshold for the default category, a threshold for the bitmap category, and still a different threshold for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the threshold for the pen category by passing <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetThreshold</b> method, then none of the default adjustment settings will apply to pens.


#### Examples



The following example creates an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a .bmp file. The code also creates an <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object and sets its bitmap threshold value to 0.6. Then the code draws the image twice: once with no color adjustment and once with the adjustment specified by the threshold.


```cpp

VOID Example_SetThreshold(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an Image object based on a .bmp file.
   // The image has one stripe with RGB components (160, 0, 0)
   // and one stripe with RGB components (0, 140, 0).
   Image image(L"RedGreenThreshold.bmp");

   // Create an ImageAttributes object, and set its bitmap threshold to 0.6.
   ImageAttributes imAtt;
   imAtt.SetThreshold(0.6f, ColorAdjustTypeBitmap);

   // Draw the image with no color adjustment.
   graphics.DrawImage(&image, 10, 10, image.GetWidth(), image.GetHeight());
 
   // Draw the image with the threshold applied.
   // 160 > 0.6*255, so the red stripe will be changed to full intensity.
   // 140 < 0.6*255, so the green stripe will be changed to zero intensity.   
   graphics.DrawImage(&image,
      Rect(100, 10, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),           // source rect
      UnitPixel,
      &imAtt);
}
				
```


The following illustration shows the output of the preceding code. Note that the red was converted to maximum intensity, and the green was converted to zero intensity.

<img alt="Illustration showing a rectangle with maroon and green regions, then the same rectangle but rendered in red and black" src="./images/imageattributessetthreshold.png"/>

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearcolorkey">ImageAttributes::ClearColorKey</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearthreshold">ImageAttributes::ClearThreshold</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolorkey">ImageAttributes::SetColorKey</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>