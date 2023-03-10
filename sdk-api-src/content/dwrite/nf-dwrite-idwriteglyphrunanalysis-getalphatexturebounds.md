---
UID: NF:dwrite.IDWriteGlyphRunAnalysis.GetAlphaTextureBounds
title: IDWriteGlyphRunAnalysis::GetAlphaTextureBounds (dwrite.h)
description: Gets the bounding rectangle of the physical pixels affected by the glyph run.
helpviewer_keywords: ["GetAlphaTextureBounds","GetAlphaTextureBounds method [Direct Write]","GetAlphaTextureBounds method [Direct Write]","IDWriteGlyphRunAnalysis interface","IDWriteGlyphRunAnalysis interface [Direct Write]","GetAlphaTextureBounds method","IDWriteGlyphRunAnalysis.GetAlphaTextureBounds","IDWriteGlyphRunAnalysis::GetAlphaTextureBounds","directwrite.IDWriteGlyphRunAnalysis_GetAlphaTextureBounds","dwrite/IDWriteGlyphRunAnalysis::GetAlphaTextureBounds"]
old-location: directwrite\IDWriteGlyphRunAnalysis_GetAlphaTextureBounds.htm
tech.root: DirectWrite
ms.assetid: 9058edb7-23b2-418a-abcc-3ee827a79144
ms.date: 12/05/2018
ms.keywords: GetAlphaTextureBounds, GetAlphaTextureBounds method [Direct Write], GetAlphaTextureBounds method [Direct Write],IDWriteGlyphRunAnalysis interface, IDWriteGlyphRunAnalysis interface [Direct Write],GetAlphaTextureBounds method, IDWriteGlyphRunAnalysis.GetAlphaTextureBounds, IDWriteGlyphRunAnalysis::GetAlphaTextureBounds, directwrite.IDWriteGlyphRunAnalysis_GetAlphaTextureBounds, dwrite/IDWriteGlyphRunAnalysis::GetAlphaTextureBounds
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
 - IDWriteGlyphRunAnalysis::GetAlphaTextureBounds
 - dwrite/IDWriteGlyphRunAnalysis::GetAlphaTextureBounds
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
 - IDWriteGlyphRunAnalysis.GetAlphaTextureBounds
---

# IDWriteGlyphRunAnalysis::GetAlphaTextureBounds


## -description

 Gets the bounding rectangle of the physical pixels affected by the glyph run.

## -parameters

### -param textureType

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_texture_type">DWRITE_TEXTURE_TYPE</a></b>

Specifies the type of texture requested. If a bi-level texture is requested, the
     bounding rectangle includes only bi-level glyphs. Otherwise, the bounding rectangle includes only antialiased
     glyphs.

### -param textureBounds [out]

Type: <b>RECT*</b>

When this method returns, contains the bounding rectangle of the physical pixels affected by the glyph run, or an empty rectangle if there are no glyphs
     of the specified texture type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis">IDWriteGlyphRunAnalysis</a>

