---
UID: NF:dwrite_1.IDWriteFontFace1.GetVerticalGlyphVariants
title: IDWriteFontFace1::GetVerticalGlyphVariants (dwrite_1.h)
author: windows-sdk-content
description: Retrieves the vertical forms of the nominal glyphs retrieved from GetGlyphIndices.
old-location: directwrite\idwritefontface1_getverticalglyphvariants.htm
tech.root: DirectWrite
ms.assetid: 91CD924E-A664-45C6-B787-61129C31501B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetVerticalGlyphVariants, GetVerticalGlyphVariants method [Direct Write], GetVerticalGlyphVariants method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetVerticalGlyphVariants method, IDWriteFontFace1.GetVerticalGlyphVariants, IDWriteFontFace1::GetVerticalGlyphVariants, directwrite.idwritefontface1_getverticalglyphvariants, dwrite_1/IDWriteFontFace1::GetVerticalGlyphVariants
ms.topic: method
f1_keywords: ["dwrite_1/IDWriteFontFace1.GetVerticalGlyphVariants"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteFontFace1.GetVerticalGlyphVariants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFace1::GetVerticalGlyphVariants


## -description


Retrieves the vertical forms of the nominal glyphs retrieved from
    GetGlyphIndices.


## -parameters




### -param glyphCount

Type: <b>UINT32</b>

The number of glyphs to retrieve.


### -param nominalGlyphIndices [in]

Type: <b>const UINT16*</b>

Original glyph indices from cmap.


### -param verticalGlyphIndices [out]

Type: <b>UINT16*</b>

The vertical form of glyph indices.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The retrieval uses the font's 'vert' table. This is used in
    CJK vertical layout so the correct characters are shown.

Call <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefontface-getglyphindices">GetGlyphIndices</a> to get the nominal glyph indices, followed by
    calling this to remap the to the substituted forms, when the run
    is sideways, and the font has vertical glyph variants. See <a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-hasverticalglyphvariants">HasVerticalGlyphVariants</a> for more info.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>
 

 

