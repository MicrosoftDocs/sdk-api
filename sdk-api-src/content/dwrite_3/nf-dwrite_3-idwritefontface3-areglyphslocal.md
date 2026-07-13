---
UID: NF:dwrite_3.IDWriteFontFace3.AreGlyphsLocal
title: IDWriteFontFace3::AreGlyphsLocal (dwrite_3.h)
description: Determines whether the specified glyphs are local.
helpviewer_keywords: ["AreGlyphsLocal","AreGlyphsLocal method [Direct Write]","AreGlyphsLocal method [Direct Write]","IDWriteFontFace3 interface","IDWriteFontFace3 interface [Direct Write]","AreGlyphsLocal method","IDWriteFontFace3.AreGlyphsLocal","IDWriteFontFace3::AreGlyphsLocal","directwrite.idwritefontface3_areglyphslocal","dwrite_3/IDWriteFontFace3::AreGlyphsLocal"]
old-location: directwrite\idwritefontface3_areglyphslocal.htm
tech.root: DirectWrite
ms.assetid: e8d5b51d-c5b5-6ea5-eda0-36cc9ec425d3
ms.date: 09/10/2025
ms.keywords: AreGlyphsLocal, AreGlyphsLocal method [Direct Write], AreGlyphsLocal method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],AreGlyphsLocal method, IDWriteFontFace3.AreGlyphsLocal, IDWriteFontFace3::AreGlyphsLocal, directwrite.idwritefontface3_areglyphslocal, dwrite_3/IDWriteFontFace3::AreGlyphsLocal
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
 - IDWriteFontFace3::AreGlyphsLocal
 - dwrite_3/IDWriteFontFace3::AreGlyphsLocal
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
 - IDWriteFontFace3.AreGlyphsLocal
---

# IDWriteFontFace3::AreGlyphsLocal


## -description

Determines whether the specified glyphs are local.

## -parameters

### -param glyphIndices [in]

Type: <b>UINT16</b>

Array of glyph indices.

### -param glyphCount

Type: <b>UINT32</b>

The number of elements in the glyph index array.

### -param enqueueIfNotLocal

Type: <b>BOOL</b>

Specifies whether to enqueue a download request    
       if any of the specified glyphs are not local.

### -param isLocal [out]

Type: <b>BOOL*</b>

Receives TRUE if all of the specified glyphs are local,    
       FALSE if any of the specified glyphs are remote.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>

