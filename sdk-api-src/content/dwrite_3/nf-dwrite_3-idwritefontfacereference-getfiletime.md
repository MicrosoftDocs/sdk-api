---
UID: NF:dwrite_3.IDWriteFontFaceReference.GetFileTime
title: IDWriteFontFaceReference::GetFileTime (dwrite_3.h)
description: Get the last modified date.
helpviewer_keywords: ["GetFileTime","GetFileTime method [Direct Write]","GetFileTime method [Direct Write]","IDWriteFontFaceReference interface","IDWriteFontFaceReference interface [Direct Write]","GetFileTime method","IDWriteFontFaceReference.GetFileTime","IDWriteFontFaceReference::GetFileTime","directwrite.idwritefontfacereference_getfiletime","dwrite_3/IDWriteFontFaceReference::GetFileTime"]
old-location: directwrite\idwritefontfacereference_getfiletime.htm
tech.root: DirectWrite
ms.assetid: 98de8a3d-073e-78df-2e2c-8ab64632091c
ms.date: 09/10/2025
ms.keywords: GetFileTime, GetFileTime method [Direct Write], GetFileTime method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],GetFileTime method, IDWriteFontFaceReference.GetFileTime, IDWriteFontFaceReference::GetFileTime, directwrite.idwritefontfacereference_getfiletime, dwrite_3/IDWriteFontFaceReference::GetFileTime
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
 - IDWriteFontFaceReference::GetFileTime
 - dwrite_3/IDWriteFontFaceReference::GetFileTime
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
 - IDWriteFontFaceReference.GetFileTime
---

# IDWriteFontFaceReference::GetFileTime


## -description

Get the last modified date.

## -parameters

### -param lastWriteTime [out]

Type: <b>FILETIME*</b>

Returns the last modified date. The time may be zero if the font file loader does not expose file time.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>

