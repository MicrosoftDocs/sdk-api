---
UID: NF:dwrite_2.IDWriteFontFallback.MapCharacters
title: IDWriteFontFallback::MapCharacters (dwrite_2.h)
description: Determines an appropriate font to use to render the beginning range of text.
helpviewer_keywords: ["IDWriteFontFallback interface [Direct Write]","MapCharacters method","IDWriteFontFallback.MapCharacters","IDWriteFontFallback::MapCharacters","MapCharacters","MapCharacters method [Direct Write]","MapCharacters method [Direct Write]","IDWriteFontFallback interface","directwrite.idwritefontfallback_mapcharacters","dwrite_2/IDWriteFontFallback::MapCharacters"]
old-location: directwrite\idwritefontfallback_mapcharacters.htm
tech.root: DirectWrite
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
ms.date: 12/05/2018
ms.keywords: IDWriteFontFallback interface [Direct Write],MapCharacters method, IDWriteFontFallback.MapCharacters, IDWriteFontFallback::MapCharacters, MapCharacters, MapCharacters method [Direct Write], MapCharacters method [Direct Write],IDWriteFontFallback interface, directwrite.idwritefontfallback_mapcharacters, dwrite_2/IDWriteFontFallback::MapCharacters
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
 - IDWriteFontFallback::MapCharacters
 - dwrite_2/IDWriteFontFallback::MapCharacters
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
 - IDWriteFontFallback.MapCharacters
---

# IDWriteFontFallback::MapCharacters


## -description

Determines an appropriate font to use to render the beginning range of text.

## -parameters

### -param analysisSource

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>*</b>

The text source implementation holds the text and locale.

### -param textPosition

Type: <b>UINT32</b>

Starting position to analyze.

### -param textLength

Type: <b>UINT32</b>

Length of the text to analyze.

### -param baseFontCollection [in, optional]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>*</b>

Default font collection to use.

### -param baseFamilyName [in, optional]

Type: <b>const wchar_t*</b>

Family name of the base font. If you pass null, no matching     will be done against the family.

### -param baseWeight

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight">DWRITE_FONT_WEIGHT</a></b>

The desired weight.

### -param baseStyle

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style">DWRITE_FONT_STYLE</a></b>

The desired style.

### -param baseStretch

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch">DWRITE_FONT_STRETCH</a></b>

The desired stretch.

### -param mappedLength [out]

Type: <b>UINT32*</b>

Length of text mapped to the mapped font. This will always be less than     or equal to the text length and greater than zero (if the text length is non-zero) so     the caller advances at least one character.

### -param mappedFont [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>**</b>

The font that should be used to render the first <i>mappedLength</i>     characters of the text. If it returns NULL, that means that no font can render the     text, and <i>mappedLength</i> is the number of characters to skip (rendered with a missing
         glyph).

### -param scale [out]

Type: <b>FLOAT*</b>

Scale factor to multiply the em size of the returned font by.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback">IDWriteFontFallback</a>

