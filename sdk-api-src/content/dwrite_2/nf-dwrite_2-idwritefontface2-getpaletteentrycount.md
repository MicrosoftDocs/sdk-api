---
UID: NF:dwrite_2.IDWriteFontFace2.GetPaletteEntryCount
title: IDWriteFontFace2::GetPaletteEntryCount (dwrite_2.h)
description: Get the number of entries in each color palette.
helpviewer_keywords: ["GetPaletteEntryCount","GetPaletteEntryCount method [Direct Write]","GetPaletteEntryCount method [Direct Write]","IDWriteFontFace2 interface","IDWriteFontFace2 interface [Direct Write]","GetPaletteEntryCount method","IDWriteFontFace2.GetPaletteEntryCount","IDWriteFontFace2::GetPaletteEntryCount","directwrite.idwritefontface2_getpaletteentrycount","dwrite_2/IDWriteFontFace2::GetPaletteEntryCount"]
old-location: directwrite\idwritefontface2_getpaletteentrycount.htm
tech.root: DirectWrite
ms.assetid: 7DFB0D3F-18E8-44AA-A7DA-4B9D971D3C35
ms.date: 12/05/2018
ms.keywords: GetPaletteEntryCount, GetPaletteEntryCount method [Direct Write], GetPaletteEntryCount method [Direct Write],IDWriteFontFace2 interface, IDWriteFontFace2 interface [Direct Write],GetPaletteEntryCount method, IDWriteFontFace2.GetPaletteEntryCount, IDWriteFontFace2::GetPaletteEntryCount, directwrite.idwritefontface2_getpaletteentrycount, dwrite_2/IDWriteFontFace2::GetPaletteEntryCount
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
 - IDWriteFontFace2::GetPaletteEntryCount
 - dwrite_2/IDWriteFontFace2::GetPaletteEntryCount
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
 - IDWriteFontFace2.GetPaletteEntryCount
---

# IDWriteFontFace2::GetPaletteEntryCount


## -description

Get the number of entries in each color palette.



## -returns

The number of entries in each color palette. All color palettes
    in a font have the same number of palette entries. The return value is 
    zero if the font has no color information.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2">IDWriteFontFace2</a>

