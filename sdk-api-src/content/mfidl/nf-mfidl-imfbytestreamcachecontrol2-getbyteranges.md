---
UID: NF:mfidl.IMFByteStreamCacheControl2.GetByteRanges
title: IMFByteStreamCacheControl2::GetByteRanges (mfidl.h)
description: Gets the ranges of bytes that are currently stored in the cache.
helpviewer_keywords: ["GetByteRanges","GetByteRanges method [Media Foundation]","GetByteRanges method [Media Foundation]","IMFByteStreamCacheControl2 interface","IMFByteStreamCacheControl2 interface [Media Foundation]","GetByteRanges method","IMFByteStreamCacheControl2.GetByteRanges","IMFByteStreamCacheControl2::GetByteRanges","mf.imfbytestreamcachecontrol2_getbyteranges","mfidl/IMFByteStreamCacheControl2::GetByteRanges"]
old-location: mf\imfbytestreamcachecontrol2_getbyteranges.htm
tech.root: mf
ms.assetid: FC91FCB5-CD22-494F-85B7-38571C38A44E
ms.date: 12/05/2018
ms.keywords: GetByteRanges, GetByteRanges method [Media Foundation], GetByteRanges method [Media Foundation],IMFByteStreamCacheControl2 interface, IMFByteStreamCacheControl2 interface [Media Foundation],GetByteRanges method, IMFByteStreamCacheControl2.GetByteRanges, IMFByteStreamCacheControl2::GetByteRanges, mf.imfbytestreamcachecontrol2_getbyteranges, mfidl/IMFByteStreamCacheControl2::GetByteRanges
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStreamCacheControl2::GetByteRanges
 - mfidl/IMFByteStreamCacheControl2::GetByteRanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFByteStreamCacheControl2.GetByteRanges
---

# IMFByteStreamCacheControl2::GetByteRanges


## -description

Gets the ranges of bytes that are currently stored in the cache.

## -parameters

### -param pcRanges [out]

Receives the number of ranges returned in the <i>ppRanges</i> array.

### -param ppRanges [out]

Receives an array of <a href="/windows/win32/api/mfidl/ns-mfidl-mf_byte_stream_cache_range">MF_BYTE_STREAM_CACHE_RANGE</a> structures. Each structure specifies a range of bytes stored in the cache. The caller must free the array by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol2">IMFByteStreamCacheControl2</a>