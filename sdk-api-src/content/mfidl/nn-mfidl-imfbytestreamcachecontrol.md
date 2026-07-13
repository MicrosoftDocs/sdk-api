---
UID: NN:mfidl.IMFByteStreamCacheControl
title: IMFByteStreamCacheControl (mfidl.h)
description: Controls how a network byte stream transfers data to a local cache. (IMFByteStreamCacheControl)
helpviewer_keywords: ["IMFByteStreamCacheControl","IMFByteStreamCacheControl interface [Media Foundation]","IMFByteStreamCacheControl interface [Media Foundation]","described","mf.imfbytestreamcachecontrol","mfidl/IMFByteStreamCacheControl"]
old-location: mf\imfbytestreamcachecontrol.htm
tech.root: mf
ms.assetid: e12a532a-4624-4e06-8e19-6e9daec550ac
ms.date: 12/05/2018
ms.keywords: IMFByteStreamCacheControl, IMFByteStreamCacheControl interface [Media Foundation], IMFByteStreamCacheControl interface [Media Foundation],described, mf.imfbytestreamcachecontrol, mfidl/IMFByteStreamCacheControl
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFByteStreamCacheControl
 - mfidl/IMFByteStreamCacheControl
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
 - IMFByteStreamCacheControl
---

# IMFByteStreamCacheControl interface


## -description

Controls how a network byte stream transfers data to a local cache. Optionally, this interface is exposed by byte streams that read data from a network, for example, through HTTP.
      

To get a pointer to this interface, call <b>QueryInterface</b> on the byte stream object.

## -inheritance

The <b>IMFByteStreamCacheControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStreamCacheControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering">IMFByteStreamBuffering</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
