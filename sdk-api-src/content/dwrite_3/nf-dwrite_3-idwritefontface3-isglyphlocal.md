---
UID: NF:dwrite_3.IDWriteFontFace3.IsGlyphLocal
title: IDWriteFontFace3::IsGlyphLocal (dwrite_3.h)
description: Determines whether the glyph is locally downloaded from the font.
helpviewer_keywords: ["IDWriteFontFace3 interface [Direct Write]","IsGlyphLocal method","IDWriteFontFace3.IsGlyphLocal","IDWriteFontFace3::IsGlyphLocal","IsGlyphLocal","IsGlyphLocal method [Direct Write]","IsGlyphLocal method [Direct Write]","IDWriteFontFace3 interface","directwrite.idwritefontface3_isglyphlocal","dwrite_3/IDWriteFontFace3::IsGlyphLocal"]
old-location: directwrite\idwritefontface3_isglyphlocal.htm
tech.root: DirectWrite
ms.assetid: def185b6-a717-5390-8521-46e38335800b
ms.date: 09/10/2025
ms.keywords: IDWriteFontFace3 interface [Direct Write],IsGlyphLocal method, IDWriteFontFace3.IsGlyphLocal, IDWriteFontFace3::IsGlyphLocal, IsGlyphLocal, IsGlyphLocal method [Direct Write], IsGlyphLocal method [Direct Write],IDWriteFontFace3 interface, directwrite.idwritefontface3_isglyphlocal, dwrite_3/IDWriteFontFace3::IsGlyphLocal
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontFace3::IsGlyphLocal
 - dwrite_3/IDWriteFontFace3::IsGlyphLocal
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
 - IDWriteFontFace3.IsGlyphLocal
---

# IDWriteFontFace3::IsGlyphLocal


## -description

Determines whether the glyph is locally downloaded from the font.

## -parameters

### -param glyphId [in]

Type: <b>UINT16</b>

Glyph identifier.

## -returns

Type: <b>BOOL</b>

Returns TRUE if the font has the specified glyph locally available.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>

