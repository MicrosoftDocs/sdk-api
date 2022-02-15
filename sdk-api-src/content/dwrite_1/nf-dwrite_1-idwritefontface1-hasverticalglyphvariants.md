---
UID: NF:dwrite_1.IDWriteFontFace1.HasVerticalGlyphVariants
title: IDWriteFontFace1::HasVerticalGlyphVariants (dwrite_1.h)
description: Determines whether the font has any vertical glyph variants.
helpviewer_keywords: ["HasVerticalGlyphVariants","HasVerticalGlyphVariants method [Direct Write]","HasVerticalGlyphVariants method [Direct Write]","IDWriteFontFace1 interface","IDWriteFontFace1 interface [Direct Write]","HasVerticalGlyphVariants method","IDWriteFontFace1.HasVerticalGlyphVariants","IDWriteFontFace1::HasVerticalGlyphVariants","directwrite.idwritefontface1_hasverticalglyphvariants","dwrite_1/IDWriteFontFace1::HasVerticalGlyphVariants"]
old-location: directwrite\idwritefontface1_hasverticalglyphvariants.htm
tech.root: DirectWrite
ms.assetid: 694F003E-4189-4DC6-ADC8-B94EE8C624BE
ms.date: 12/05/2018
ms.keywords: HasVerticalGlyphVariants, HasVerticalGlyphVariants method [Direct Write], HasVerticalGlyphVariants method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],HasVerticalGlyphVariants method, IDWriteFontFace1.HasVerticalGlyphVariants, IDWriteFontFace1::HasVerticalGlyphVariants, directwrite.idwritefontface1_hasverticalglyphvariants, dwrite_1/IDWriteFontFace1::HasVerticalGlyphVariants
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
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFace1::HasVerticalGlyphVariants
 - dwrite_1/IDWriteFontFace1::HasVerticalGlyphVariants
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteFontFace1.HasVerticalGlyphVariants
---

# IDWriteFontFace1::HasVerticalGlyphVariants


## -description

Determines whether the font has any vertical glyph variants.



## -returns

Returns TRUE if the font contains vertical glyph variants, otherwise FALSE.

## -remarks

For OpenType fonts, <b>HasVerticalGlyphVariants</b> returns TRUE if the font contains a "vert"feature. 


<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants">IDWriteFontFace1::GetVerticalGlyphVariants</a> retrieves the vertical forms of the nominal glyphs that are retrieved from <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices">IDWriteFontFace::GetGlyphIndices</a>.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants">IDWriteFontFace1::GetVerticalGlyphVariants</a>



<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices">IDWriteFontFace::GetGlyphIndices</a>

