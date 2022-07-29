---
UID: NN:mfidl.IMFByteStreamCacheControl2
title: IMFByteStreamCacheControl2 (mfidl.h)
description: Controls how a network byte stream transfers data to a local cache. (IMFByteStreamCacheControl2)
helpviewer_keywords: ["IMFByteStreamCacheControl2","IMFByteStreamCacheControl2 interface [Media Foundation]","IMFByteStreamCacheControl2 interface [Media Foundation]","described","mf.imfbytestreamcachecontrol2","mfidl/IMFByteStreamCacheControl2"]
old-location: mf\imfbytestreamcachecontrol2.htm
tech.root: mf
ms.assetid: A901F679-B6F2-4DB7-8EFC-EA61249B64FB
ms.date: 12/05/2018
ms.keywords: IMFByteStreamCacheControl2, IMFByteStreamCacheControl2 interface [Media Foundation], IMFByteStreamCacheControl2 interface [Media Foundation],described, mf.imfbytestreamcachecontrol2, mfidl/IMFByteStreamCacheControl2
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
 - IMFByteStreamCacheControl2
 - mfidl/IMFByteStreamCacheControl2
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
 - IMFByteStreamCacheControl2
---

# IMFByteStreamCacheControl2 interface


## -description

Controls how a network byte stream transfers data to a local cache. This interface extends the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a> interface.

## -inheritance

The <b>IMFByteStreamCacheControl2</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a>. <b>IMFByteStreamCacheControl2</b> also has these types of members:

## -remarks

Byte streams object in Microsoft Media Foundation can optionally implement this interface. To get a pointer to this interface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the byte stream object.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
