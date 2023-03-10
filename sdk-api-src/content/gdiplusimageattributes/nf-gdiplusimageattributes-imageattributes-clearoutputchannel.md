---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearOutputChannel
title: ImageAttributes::ClearOutputChannel (gdiplusimageattributes.h)
description: The ImageAttributes::ClearOutputChannel method clears the cyan-magenta-yellow-black (CMYK) output channel setting for a specified category.
helpviewer_keywords: ["ClearOutputChannel","ClearOutputChannel method [GDI+]","ClearOutputChannel method [GDI+]","ImageAttributes class","ImageAttributes class [GDI+]","ClearOutputChannel method","ImageAttributes.ClearOutputChannel","ImageAttributes::ClearOutputChannel","_gdiplus_CLASS_ImageAttributes_ClearOutputChannel_type_","gdiplus._gdiplus_CLASS_ImageAttributes_ClearOutputChannel_type_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearOutputChannel_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearoutputchannel.htm
ms.date: 12/05/2018
ms.keywords: ClearOutputChannel, ClearOutputChannel method [GDI+], ClearOutputChannel method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearOutputChannel method, ImageAttributes.ClearOutputChannel, ImageAttributes::ClearOutputChannel, _gdiplus_CLASS_ImageAttributes_ClearOutputChannel_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearOutputChannel_type_
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
 - ImageAttributes::ClearOutputChannel
 - gdiplusimageattributes/ImageAttributes::ClearOutputChannel
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
 - ImageAttributes.ClearOutputChannel
---

# ImageAttributes::ClearOutputChannel


## -description

The <b>ImageAttributes::ClearOutputChannel</b> method clears the cyan-magenta-yellow-black (CMYK) output channel setting for a specified category.

## -parameters

### -param type [in, optional]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a> enumeration that specifies the category for which the output channel setting is cleared. The default value is <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustTypeDefault</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

An <a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify an output channel for the default category and a different output channel for the bitmap category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the bitmap category, then the default settings apply to the bitmap category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify an output channel and an adjustment matrix for the default category. If you set the output channel for the bitmap category by calling <a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setoutputchannel">ImageAttributes::SetOutputChannel</a>, then the default output channel will not apply to bitmaps. If you later clear the bitmap output channel by calling <b>ImageAttributes::ClearOutputChannel</b>, the bitmap category will not revert to the default output channel; rather, the bitmap category will have no output channel setting. Similarly, the bitmap category will not revert to the default color-adjustment matrix; rather, the bitmap category will have no color-adjustment matrix.

## -see-also

<a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-coloradjusttype">ColorAdjustType</a>



<a href="/windows/desktop/api/gdipluscolor/ne-gdipluscolor-colorchannelflags">ColorChannelFlags</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-clearoutputchannelcolorprofile">ImageAttributes::ClearOutputChannelColorProfile</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setoutputchannel">ImageAttributes::SetOutputChannel</a>



<a href="/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setoutputchannelcolorprofile">ImageAttributes::SetOutputChannelColorProfile</a>