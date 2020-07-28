---
UID: NF:gdiplusimageattributes.ImageAttributes.Reset
title: ImageAttributes::Reset (gdiplusimageattributes.h)
description: The ImageAttributes::Reset method clears all color- and grayscale-adjustment settings for a specified category.
helpviewer_keywords: ["ImageAttributes class [GDI+]","Reset method","ImageAttributes.Reset","ImageAttributes::Reset","Reset","Reset method [GDI+]","Reset method [GDI+]","ImageAttributes class","_gdiplus_CLASS_ImageAttributes_Reset_type_","gdiplus._gdiplus_CLASS_ImageAttributes_Reset_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_Reset_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\reset_82type.htm
ms.date: 12/05/2018
ms.keywords: ImageAttributes class [GDI+],Reset method, ImageAttributes.Reset, ImageAttributes::Reset, Reset, Reset method [GDI+], Reset method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_Reset_type_, gdiplus._gdiplus_CLASS_ImageAttributes_Reset_type_
f1_keywords:
- gdiplusimageattributes/ImageAttributes.Reset
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- ImageAttributes.Reset
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# ImageAttributes::Reset


## -description


The <b>ImageAttributes::Reset</b> method clears all color- and grayscale-adjustment settings for a specified category.


## -parameters




### -param type [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which color adjustment is reset. The default value is <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



An 
				<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a gamma value for the default category, a different gamma value for the bitmap category, and still a different gamma value for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. You can reinstate the default settings for that category by calling <b>ImageAttributes::Reset</b>. For example, suppose you specify a gamma value for the default category. If you set the gamma value for the pen category by calling <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setgamma">ImageAttributes::SetGamma</a>, then the default gamma value will not apply to pens. If you later pass <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypePen</a> to the <b>ImageAttributes::Reset</b> method, the pen category will revert to the default gamma value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearnoop">ImageAttributes::ClearNoOp</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setnoop">ImageAttributes::SetNoOp</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>
 

 

