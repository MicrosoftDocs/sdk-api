---
UID: NF:gdiplusheaders.Image.SetPalette
title: Image::SetPalette (gdiplusheaders.h)
description: The Image::SetPalette method sets the color palette of this Image object.
helpviewer_keywords: ["Image class [GDI+]","SetPalette method","Image.SetPalette","Image::SetPalette","SetPalette","SetPalette method [GDI+]","SetPalette method [GDI+]","Image class","_gdiplus_CLASS_Image_SetPalette_palette_","gdiplus._gdiplus_CLASS_Image_SetPalette_palette_"]
old-location: gdiplus\_gdiplus_CLASS_Image_SetPalette_palette_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\setpalette.htm
ms.date: 12/05/2018
ms.keywords: Image class [GDI+],SetPalette method, Image.SetPalette, Image::SetPalette, SetPalette, SetPalette method [GDI+], SetPalette method [GDI+],Image class, _gdiplus_CLASS_Image_SetPalette_palette_, gdiplus._gdiplus_CLASS_Image_SetPalette_palette_
req.header: gdiplusheaders.h
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
 - Image::SetPalette
 - gdiplusheaders/Image::SetPalette
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
 - Image.SetPalette
---

# Image::SetPalette


## -description

The <b>Image::SetPalette</b> method sets the color palette of this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.

## -parameters

### -param palette [in]

Type: <b>const ColorPalette*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a> structure that specifies the palette.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpalette">Image::GetPalette</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpalettesize">Image::GetPaletteSize</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>