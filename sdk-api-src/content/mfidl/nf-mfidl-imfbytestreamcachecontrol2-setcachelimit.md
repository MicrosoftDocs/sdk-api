---
UID: NF:mfidl.IMFByteStreamCacheControl2.SetCacheLimit
title: IMFByteStreamCacheControl2::SetCacheLimit (mfidl.h)
description: Limits the cache size.
helpviewer_keywords: ["IMFByteStreamCacheControl2 interface [Media Foundation]","SetCacheLimit method","IMFByteStreamCacheControl2.SetCacheLimit","IMFByteStreamCacheControl2::SetCacheLimit","SetCacheLimit","SetCacheLimit method [Media Foundation]","SetCacheLimit method [Media Foundation]","IMFByteStreamCacheControl2 interface","mf.imfbytestreamcachecontrol2_setcachelimit","mfidl/IMFByteStreamCacheControl2::SetCacheLimit"]
old-location: mf\imfbytestreamcachecontrol2_setcachelimit.htm
tech.root: mf
ms.assetid: 1DDC3D76-E28B-4B8C-B2CD-FE77E840D949
ms.date: 12/05/2018
ms.keywords: IMFByteStreamCacheControl2 interface [Media Foundation],SetCacheLimit method, IMFByteStreamCacheControl2.SetCacheLimit, IMFByteStreamCacheControl2::SetCacheLimit, SetCacheLimit, SetCacheLimit method [Media Foundation], SetCacheLimit method [Media Foundation],IMFByteStreamCacheControl2 interface, mf.imfbytestreamcachecontrol2_setcachelimit, mfidl/IMFByteStreamCacheControl2::SetCacheLimit
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
 - IMFByteStreamCacheControl2::SetCacheLimit
 - mfidl/IMFByteStreamCacheControl2::SetCacheLimit
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
 - IMFByteStreamCacheControl2.SetCacheLimit
---

# IMFByteStreamCacheControl2::SetCacheLimit


## -description

Limits the cache size.

## -parameters

### -param qwBytes [in]

The maximum number of bytes to store in the cache, or <b>ULONGLONG_MAX </b> for no limit.  The default value is no limit.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol2">IMFByteStreamCacheControl2</a>