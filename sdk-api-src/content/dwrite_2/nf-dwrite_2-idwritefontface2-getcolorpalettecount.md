---
UID: NF:dwrite_2.IDWriteFontFace2.GetColorPaletteCount
title: IDWriteFontFace2::GetColorPaletteCount (dwrite_2.h)
description: Gets the number of color palettes defined by the font.
helpviewer_keywords: ["GetColorPaletteCount","GetColorPaletteCount method [Direct Write]","GetColorPaletteCount method [Direct Write]","IDWriteFontFace2 interface","IDWriteFontFace2 interface [Direct Write]","GetColorPaletteCount method","IDWriteFontFace2.GetColorPaletteCount","IDWriteFontFace2::GetColorPaletteCount","directwrite.idwritefontface2_getcolorpalettecount","dwrite_2/IDWriteFontFace2::GetColorPaletteCount"]
old-location: directwrite\idwritefontface2_getcolorpalettecount.htm
tech.root: DirectWrite
ms.assetid: 99BB9C72-99B1-427C-B740-55A138189459
ms.date: 12/05/2018
ms.keywords: GetColorPaletteCount, GetColorPaletteCount method [Direct Write], GetColorPaletteCount method [Direct Write],IDWriteFontFace2 interface, IDWriteFontFace2 interface [Direct Write],GetColorPaletteCount method, IDWriteFontFace2.GetColorPaletteCount, IDWriteFontFace2::GetColorPaletteCount, directwrite.idwritefontface2_getcolorpalettecount, dwrite_2/IDWriteFontFace2::GetColorPaletteCount
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFace2::GetColorPaletteCount
 - dwrite_2/IDWriteFontFace2::GetColorPaletteCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace2.GetColorPaletteCount
---

# IDWriteFontFace2::GetColorPaletteCount


## -description

Gets the number of color palettes defined by the font.



## -returns

The return value is zero if the font has no color information. Color fonts are required to define at least one palette, with palette index zero reserved as the default palette.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2">IDWriteFontFace2</a>

