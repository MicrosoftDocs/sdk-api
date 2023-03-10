---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.ApplyCharacterSpacing
title: IDWriteTextAnalyzer1::ApplyCharacterSpacing (dwrite_1.h)
description: Applies spacing between characters, properly adjusting glyph clusters and diacritics.
helpviewer_keywords: ["ApplyCharacterSpacing","ApplyCharacterSpacing method [Direct Write]","ApplyCharacterSpacing method [Direct Write]","IDWriteTextAnalyzer1 interface","IDWriteTextAnalyzer1 interface [Direct Write]","ApplyCharacterSpacing method","IDWriteTextAnalyzer1.ApplyCharacterSpacing","IDWriteTextAnalyzer1::ApplyCharacterSpacing","directwrite.idwritetextanalyzer1_applycharacterspacing","dwrite_1/IDWriteTextAnalyzer1::ApplyCharacterSpacing"]
old-location: directwrite\idwritetextanalyzer1_applycharacterspacing.htm
tech.root: DirectWrite
ms.assetid: E4BACB7E-0032-450C-AEA8-87434329F33C
ms.date: 12/05/2018
ms.keywords: ApplyCharacterSpacing, ApplyCharacterSpacing method [Direct Write], ApplyCharacterSpacing method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],ApplyCharacterSpacing method, IDWriteTextAnalyzer1.ApplyCharacterSpacing, IDWriteTextAnalyzer1::ApplyCharacterSpacing, directwrite.idwritetextanalyzer1_applycharacterspacing, dwrite_1/IDWriteTextAnalyzer1::ApplyCharacterSpacing
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextAnalyzer1::ApplyCharacterSpacing
 - dwrite_1/IDWriteTextAnalyzer1::ApplyCharacterSpacing
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
 - IDWriteTextAnalyzer1.ApplyCharacterSpacing
---

# IDWriteTextAnalyzer1::ApplyCharacterSpacing


## -description

Applies spacing between characters, properly adjusting glyph clusters
    and diacritics.

## -parameters

### -param leadingSpacing

The spacing before each character, in reading order.

### -param trailingSpacing

The spacing after each character, in reading order.

### -param minimumAdvanceWidth

The minimum advance of each character,
    to prevent characters from becoming too thin or zero-width. This
    must be zero or greater.

### -param textLength

The length of the clustermap and original text.

### -param glyphCount

The number of glyphs.

### -param clusterMap [in]

Mapping from character ranges to glyph ranges.

### -param glyphAdvances [in]

The advance width of each glyph.

### -param glyphOffsets [in]

The offset of the origin of each glyph.

### -param glyphProperties [in]

Properties of each glyph, from GetGlyphs.

### -param modifiedGlyphAdvances [out]

The new advance width of each glyph.

### -param modifiedGlyphOffsets [out]

The new offset of the origin of each glyph.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The input and output advances/offsets are allowed to alias the same array.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1">IDWriteTextAnalyzer1</a>

