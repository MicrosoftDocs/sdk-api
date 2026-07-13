---
UID: NF:dwrite_3.IDWriteFontFaceReference.EnqueueCharacterDownloadRequest
title: IDWriteFontFaceReference::EnqueueCharacterDownloadRequest (dwrite_3.h)
description: Adds a request to the font download queue (IDWriteFontDownloadQueue). (IDWriteFontFaceReference.EnqueueCharacterDownloadRequest)
helpviewer_keywords: ["EnqueueCharacterDownloadRequest","EnqueueCharacterDownloadRequest method [Direct Write]","EnqueueCharacterDownloadRequest method [Direct Write]","IDWriteFontFaceReference interface","IDWriteFontFaceReference interface [Direct Write]","EnqueueCharacterDownloadRequest method","IDWriteFontFaceReference.EnqueueCharacterDownloadRequest","IDWriteFontFaceReference::EnqueueCharacterDownloadRequest","directwrite.idwritefontfacereference_enqueuecharacterdownloadrequest","dwrite_3/IDWriteFontFaceReference::EnqueueCharacterDownloadRequest"]
old-location: directwrite\idwritefontfacereference_enqueuecharacterdownloadrequest.htm
tech.root: DirectWrite
ms.assetid: 7ca1b6c7-46c2-2440-35e4-0bcdc375d74e
ms.date: 09/10/2025
ms.keywords: EnqueueCharacterDownloadRequest, EnqueueCharacterDownloadRequest method [Direct Write], EnqueueCharacterDownloadRequest method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],EnqueueCharacterDownloadRequest method, IDWriteFontFaceReference.EnqueueCharacterDownloadRequest, IDWriteFontFaceReference::EnqueueCharacterDownloadRequest, directwrite.idwritefontfacereference_enqueuecharacterdownloadrequest, dwrite_3/IDWriteFontFaceReference::EnqueueCharacterDownloadRequest
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
 - IDWriteFontFaceReference::EnqueueCharacterDownloadRequest
 - dwrite_3/IDWriteFontFaceReference::EnqueueCharacterDownloadRequest
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
 - IDWriteFontFaceReference.EnqueueCharacterDownloadRequest
---

# IDWriteFontFaceReference::EnqueueCharacterDownloadRequest


## -description

Adds a request to the font download queue (<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>).

## -parameters

### -param characters [in]

Type: <b>const WCHAR*</b>

Array of characters to download.

### -param characterCount

Type: <b>UINT32</b>

The number of elements in the character array.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 Downloading a character involves downloading every glyph it depends on directly or indirectly, via font tables (cmap, GSUB, COLR, glyf).

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>

