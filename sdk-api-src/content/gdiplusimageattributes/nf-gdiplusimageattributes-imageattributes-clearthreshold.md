---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearThreshold
title: ImageAttributes::ClearThreshold (gdiplusimageattributes.h)
description: The ImageAttributes::ClearThreshold method clears the threshold value for a specified category.
helpviewer_keywords: ["ClearThreshold","ClearThreshold method [GDI+]","ClearThreshold method [GDI+]","ImageAttributes class","ImageAttributes class [GDI+]","ClearThreshold method","ImageAttributes.ClearThreshold","ImageAttributes::ClearThreshold","_gdiplus_CLASS_ImageAttributes_ClearThreshold_type_","gdiplus._gdiplus_CLASS_ImageAttributes_ClearThreshold_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearThreshold_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearthreshold.htm
ms.date: 12/05/2018
ms.keywords: ClearThreshold, ClearThreshold method [GDI+], ClearThreshold method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearThreshold method, ImageAttributes.ClearThreshold, ImageAttributes::ClearThreshold, _gdiplus_CLASS_ImageAttributes_ClearThreshold_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearThreshold_type_
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
 - ImageAttributes::ClearThreshold
 - gdiplusimageattributes/ImageAttributes::ClearThreshold
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
 - ImageAttributes.ClearThreshold
---

# ImageAttributes::ClearThreshold


## -description

The <b>ImageAttributes::ClearThreshold</b> method clears the threshold value for a specified category.

## -parameters

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the threshold is cleared. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The threshold is a value from 0 through 1 that specifies a cutoff point for each color component. For example, suppose the threshold is set to 0.7, and suppose you are rendering a color whose red, green, and blue components are 230, 50, and 220. The red component, 230, is greater than 0.7×255, so the red component will be changed to 255 (full intensity). The green component, 50, is less than 0.7×255, so the green component will be changed to 0. The blue component, 220, is greater than 0.7×255, so the blue component will be changed to 255.

An <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a threshold for the default category, a different threshold for the bitmap category, and still a different threshold for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a threshold and a gamma value for the default category. If you set the threshold for the pen category by calling <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setthreshold">ImageAttributes::SetThreshold</a>, then the default threshold will not apply to pens. If you later clear the pen threshold by calling <b>ImageAttributes::ClearThreshold</b>, the pen category will not revert to the default threshold; rather, the pen category will have no threshold. Similarly, the pen category will not revert to the default gamma value; rather, the pen category will have no gamma value.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearcolorkey">ImageAttributes::ClearColorKey</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolorkey">ImageAttributes::SetColorKey</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setthreshold">ImageAttributes::SetThreshold</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>