---
UID: NF:dwrite.IDWriteFontFace.GetDesignGlyphMetrics
title: IDWriteFontFace::GetDesignGlyphMetrics (dwrite.h)
description: Obtains ideal (resolution-independent) glyph metrics in font design units.
helpviewer_keywords: ["GetDesignGlyphMetrics","GetDesignGlyphMetrics method [Direct Write]","GetDesignGlyphMetrics method [Direct Write]","IDWriteFontFace interface","IDWriteFontFace interface [Direct Write]","GetDesignGlyphMetrics method","IDWriteFontFace.GetDesignGlyphMetrics","IDWriteFontFace::GetDesignGlyphMetrics","directwrite.IDWriteFontFace_GetDesignGlyphMetrics","dwrite/IDWriteFontFace::GetDesignGlyphMetrics"]
old-location: directwrite\IDWriteFontFace_GetDesignGlyphMetrics.htm
tech.root: DirectWrite
ms.assetid: 4da03cbe-5287-4d9c-aaa2-cff3dbf259fc
ms.date: 12/05/2018
ms.keywords: GetDesignGlyphMetrics, GetDesignGlyphMetrics method [Direct Write], GetDesignGlyphMetrics method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetDesignGlyphMetrics method, IDWriteFontFace.GetDesignGlyphMetrics, IDWriteFontFace::GetDesignGlyphMetrics, directwrite.IDWriteFontFace_GetDesignGlyphMetrics, dwrite/IDWriteFontFace::GetDesignGlyphMetrics
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteFontFace::GetDesignGlyphMetrics
 - dwrite/IDWriteFontFace::GetDesignGlyphMetrics
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
 - IDWriteFontFace.GetDesignGlyphMetrics
---

# IDWriteFontFace::GetDesignGlyphMetrics


## -description

 Obtains ideal (resolution-independent) glyph metrics in font design units.

## -parameters

### -param glyphIndices [in]

Type: <b>const UINT16*</b>

 An array of glyph indices for which to compute  metrics. The array must contain at least as many elements as specified by <i>glyphCount</i>.

### -param glyphCount

Type: <b>UINT32</b>

The number of elements in the <i>glyphIndices</i> array.

### -param glyphMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics">DWRITE_GLYPH_METRICS</a>*</b>

When this method returns, contains an array of DWRITE_GLYPH_METRICS structures.  <i>glyphMetrics</i> must be initialized with an empty buffer that contains at least as many elements as <i>glyphCount</i>.
     The metrics returned by this function are in font design units.

### -param isSideways

Type: <b>BOOL</b>

Indicates whether the font is being used in a sideways run. This can affect the glyph metrics if the font has oblique simulation
    because sideways oblique simulation differs from non-sideways oblique simulation

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Design glyph metrics are used for glyph positioning.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>

