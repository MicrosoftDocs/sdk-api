---
UID: NF:dwrite_3.IDWriteFontFaceReference.EnqueueGlyphDownloadRequest
title: IDWriteFontFaceReference::EnqueueGlyphDownloadRequest (dwrite_3.h)
description: Adds a request to the font download queue (IDWriteFontDownloadQueue). (IDWriteFontFaceReference.EnqueueGlyphDownloadRequest)
helpviewer_keywords: ["EnqueueGlyphDownloadRequest","EnqueueGlyphDownloadRequest method [Direct Write]","EnqueueGlyphDownloadRequest method [Direct Write]","IDWriteFontFaceReference interface","IDWriteFontFaceReference interface [Direct Write]","EnqueueGlyphDownloadRequest method","IDWriteFontFaceReference.EnqueueGlyphDownloadRequest","IDWriteFontFaceReference::EnqueueGlyphDownloadRequest","directwrite.idwritefontfacereference_enqueueglyphdownloadrequest","dwrite_3/IDWriteFontFaceReference::EnqueueGlyphDownloadRequest"]
old-location: directwrite\idwritefontfacereference_enqueueglyphdownloadrequest.htm
tech.root: DirectWrite
ms.assetid: 4e35c011-8d5b-0bb5-fea2-4034b8e379aa
ms.date: 09/10/2025
ms.keywords: EnqueueGlyphDownloadRequest, EnqueueGlyphDownloadRequest method [Direct Write], EnqueueGlyphDownloadRequest method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],EnqueueGlyphDownloadRequest method, IDWriteFontFaceReference.EnqueueGlyphDownloadRequest, IDWriteFontFaceReference::EnqueueGlyphDownloadRequest, directwrite.idwritefontfacereference_enqueueglyphdownloadrequest, dwrite_3/IDWriteFontFaceReference::EnqueueGlyphDownloadRequest
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
 - IDWriteFontFaceReference::EnqueueGlyphDownloadRequest
 - dwrite_3/IDWriteFontFaceReference::EnqueueGlyphDownloadRequest
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
 - IDWriteFontFaceReference.EnqueueGlyphDownloadRequest
---

# IDWriteFontFaceReference::EnqueueGlyphDownloadRequest


## -description

Adds a request to the font download queue (<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>).

## -parameters

### -param glyphIndices [in]

Type: <b>const UINT16*</b>

Array of glyph indices to download.

### -param glyphCount

Type: <b>UINT32</b>

The number of elements in the glyph index array.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Downloading a glyph involves downloading any other glyphs it depends on from the font tables (GSUB, COLR, glyf).

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>

