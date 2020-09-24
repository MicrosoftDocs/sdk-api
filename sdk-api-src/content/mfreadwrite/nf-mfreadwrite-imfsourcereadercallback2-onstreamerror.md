---
UID: NF:mfreadwrite.IMFSourceReaderCallback2.OnStreamError
title: IMFSourceReaderCallback2::OnStreamError (mfreadwrite.h)
description: Called when an asynchronous error occurs with the IMFSourceReader.
helpviewer_keywords: ["IMFSourceReaderCallback2 interface [Media Foundation]","OnStreamError method","IMFSourceReaderCallback2.OnStreamError","IMFSourceReaderCallback2::OnStreamError","OnStreamError","OnStreamError method [Media Foundation]","OnStreamError method [Media Foundation]","IMFSourceReaderCallback2 interface","mf.imfsourcereadercallback2_onstreamerror","mfreadwrite/IMFSourceReaderCallback2::OnStreamError"]
old-location: mf\imfsourcereadercallback2_onstreamerror.htm
tech.root: mf
ms.assetid: 9239DE9E-8CC3-493A-B7FE-AB0294907069
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderCallback2 interface [Media Foundation],OnStreamError method, IMFSourceReaderCallback2.OnStreamError, IMFSourceReaderCallback2::OnStreamError, OnStreamError, OnStreamError method [Media Foundation], OnStreamError method [Media Foundation],IMFSourceReaderCallback2 interface, mf.imfsourcereadercallback2_onstreamerror, mfreadwrite/IMFSourceReaderCallback2::OnStreamError
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMFSourceReaderCallback2::OnStreamError
 - mfreadwrite/IMFSourceReaderCallback2::OnStreamError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSourceReaderCallback2.OnStreamError
---

# IMFSourceReaderCallback2::OnStreamError


## -description

Called when an asynchronous error occurs with the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>.

## -parameters

### -param dwStreamIndex

The index of the stream of the transform that raised the asynchronous error.

### -param hrStatus

The error that occurred.

## -returns

Returns an <b>HRESULT</b> value. Currently, the source reader ignores the return value.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback2">IMFSourceReaderCallback2</a>