---
UID: NF:dwrite_3.IDWriteFontFaceReference.EnqueueFileFragmentDownloadRequest
title: IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest (dwrite_3.h)
description: Adds a request to the font download queue (IDWriteFontDownloadQueue). (IDWriteFontFaceReference.EnqueueFileFragmentDownloadRequest)
helpviewer_keywords: ["EnqueueFileFragmentDownloadRequest","EnqueueFileFragmentDownloadRequest method [Direct Write]","EnqueueFileFragmentDownloadRequest method [Direct Write]","IDWriteFontFaceReference interface","IDWriteFontFaceReference interface [Direct Write]","EnqueueFileFragmentDownloadRequest method","IDWriteFontFaceReference.EnqueueFileFragmentDownloadRequest","IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest","directwrite.idwritefontfacereference_enqueuefilefragmentdownloadrequest","dwrite_3/IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest"]
old-location: directwrite\idwritefontfacereference_enqueuefilefragmentdownloadrequest.htm
tech.root: DirectWrite
ms.assetid: 6dfc2793-7960-5c13-950d-9ba14900c3e0
ms.date: 09/10/2025
ms.keywords: EnqueueFileFragmentDownloadRequest, EnqueueFileFragmentDownloadRequest method [Direct Write], EnqueueFileFragmentDownloadRequest method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],EnqueueFileFragmentDownloadRequest method, IDWriteFontFaceReference.EnqueueFileFragmentDownloadRequest, IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest, directwrite.idwritefontfacereference_enqueuefilefragmentdownloadrequest, dwrite_3/IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest
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
 - IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest
 - dwrite_3/IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest
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
 - IDWriteFontFaceReference.EnqueueFileFragmentDownloadRequest
---

# IDWriteFontFaceReference::EnqueueFileFragmentDownloadRequest


## -description

Adds a request to the font download queue (<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>).

## -parameters

### -param fileOffset

Type: <b>UINT64</b>

Offset of the fragment from the beginning of the font file.

### -param fragmentSize

Type: <b>UINT64</b>

Size of the fragment in bytes.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>

