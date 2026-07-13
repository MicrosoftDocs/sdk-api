---
UID: NF:dwrite_1.IDWriteFontFace1.GetKerningPairAdjustments
title: IDWriteFontFace1::GetKerningPairAdjustments (dwrite_1.h)
description: Retrieves the kerning pair adjustments from the font's kern table.
helpviewer_keywords: ["GetKerningPairAdjustments","GetKerningPairAdjustments method [Direct Write]","GetKerningPairAdjustments method [Direct Write]","IDWriteFontFace1 interface","IDWriteFontFace1 interface [Direct Write]","GetKerningPairAdjustments method","IDWriteFontFace1.GetKerningPairAdjustments","IDWriteFontFace1::GetKerningPairAdjustments","directwrite.idwritefontface1_getkerningpairadjustments","dwrite_1/IDWriteFontFace1::GetKerningPairAdjustments"]
old-location: directwrite\idwritefontface1_getkerningpairadjustments.htm
tech.root: DirectWrite
ms.assetid: DA837B04-85BC-4A3B-A6FE-24D5AFD21B14
ms.date: 12/05/2018
ms.keywords: GetKerningPairAdjustments, GetKerningPairAdjustments method [Direct Write], GetKerningPairAdjustments method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetKerningPairAdjustments method, IDWriteFontFace1.GetKerningPairAdjustments, IDWriteFontFace1::GetKerningPairAdjustments, directwrite.idwritefontface1_getkerningpairadjustments, dwrite_1/IDWriteFontFace1::GetKerningPairAdjustments
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
 - IDWriteFontFace1::GetKerningPairAdjustments
 - dwrite_1/IDWriteFontFace1::GetKerningPairAdjustments
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
 - IDWriteFontFace1.GetKerningPairAdjustments
---

# IDWriteFontFace1::GetKerningPairAdjustments


## -description

Retrieves the kerning pair adjustments from the font's kern table.

## -parameters

### -param glyphCount

Type: <b>UINT32</b>

Number of glyphs to retrieve adjustments for.

### -param glyphIndices [in]

Type: <b>const UINT16*</b>

An array of glyph id's to retrieve adjustments
    for.

### -param glyphAdvanceAdjustments [out]

Type: <b>INT32*</b>

The advances, returned in font design units, for
    each glyph. The last glyph adjustment is zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>GetKerningPairAdjustments</b> isn't a direct replacement for GDI's character based
    <a href="/windows/win32/api/wingdi/nf-wingdi-getkerningpairsa">GetKerningPairs</a>, but it serves the same role, without the client
    needing to cache them locally. <b>GetKerningPairAdjustments</b> also uses glyph id's directly
    rather than UCS-2 characters (how the kern table actually stores
    them), which avoids glyph collapse and ambiguity, such as the dash
    and hyphen, or space and non-breaking space.

Newer fonts may have only GPOS kerning instead of the legacy pair-table kerning. Such fonts, like Gabriola, will only return 0's for
    adjustments. <b>GetKerningPairAdjustments</b> doesn't virtualize and flatten these
    GPOS entries into kerning pairs.

You can realize a performance benefit by calling <a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs">IDWriteFontFace1::HasKerningPairs</a> to determine whether you need to call  <b>GetKerningPairAdjustments</b>. If you previously called <b>IDWriteFontFace1::HasKerningPairs</b> and it returned FALSE, you can avoid calling <b>GetKerningPairAdjustments</b> because the font has no kerning pair-table entries. That is, in this situation, a call to <b>GetKerningPairAdjustments</b> would be a no-op.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs">IDWriteFontFace1::HasKerningPairs</a>

