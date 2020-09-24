---
UID: NF:gdiplusheaders.Image.GetPalette
title: Image::GetPalette (gdiplusheaders.h)
description: The Image::GetPalette method gets the ColorPalette of this Image object.
helpviewer_keywords: ["GetPalette","GetPalette method [GDI+]","GetPalette method [GDI+]","Image class","Image class [GDI+]","GetPalette method","Image.GetPalette","Image::GetPalette","_gdiplus_CLASS_Image_GetPalette_palette_size_","gdiplus._gdiplus_CLASS_Image_GetPalette_palette_size_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetPalette_palette_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getpalette.htm
ms.date: 12/05/2018
ms.keywords: GetPalette, GetPalette method [GDI+], GetPalette method [GDI+],Image class, Image class [GDI+],GetPalette method, Image.GetPalette, Image::GetPalette, _gdiplus_CLASS_Image_GetPalette_palette_size_, gdiplus._gdiplus_CLASS_Image_GetPalette_palette_size_
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
 - Image::GetPalette
 - gdiplusheaders/Image::GetPalette
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
 - Image.GetPalette
---

# Image::GetPalette


## -description

The <b>Image::GetPalette</b> method gets the <a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a> of this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.

## -parameters

### -param palette [out]

Type: <b><a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspixelformats/ns-gdipluspixelformats-colorpalette">ColorPalette</a> structure that receives the palette.

### -param size [in]

Type: <b>INT</b>

Integer that specifies the size, in bytes, of the palette. Call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpalettesize">Image::GetPaletteSize</a> method to determine the size.

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



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpalettesize">Image::GetPaletteSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-setpalette">Image::SetPalette</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>