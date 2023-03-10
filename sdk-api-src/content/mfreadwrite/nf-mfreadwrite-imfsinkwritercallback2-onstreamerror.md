---
UID: NF:mfreadwrite.IMFSinkWriterCallback2.OnStreamError
title: IMFSinkWriterCallback2::OnStreamError (mfreadwrite.h)
description: Called when an asynchronous error occurs with the IMFSinkWriter.
helpviewer_keywords: ["IMFSinkWriterCallback2 interface [Media Foundation]","OnStreamError method","IMFSinkWriterCallback2.OnStreamError","IMFSinkWriterCallback2::OnStreamError","OnStreamError","OnStreamError method [Media Foundation]","OnStreamError method [Media Foundation]","IMFSinkWriterCallback2 interface","mf.imfsinkwritercallback2_onstreamerror","mfreadwrite/IMFSinkWriterCallback2::OnStreamError"]
old-location: mf\imfsinkwritercallback2_onstreamerror.htm
tech.root: mf
ms.assetid: 31239998-9D12-46A4-B3F3-68167F6EFFDD
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterCallback2 interface [Media Foundation],OnStreamError method, IMFSinkWriterCallback2.OnStreamError, IMFSinkWriterCallback2::OnStreamError, OnStreamError, OnStreamError method [Media Foundation], OnStreamError method [Media Foundation],IMFSinkWriterCallback2 interface, mf.imfsinkwritercallback2_onstreamerror, mfreadwrite/IMFSinkWriterCallback2::OnStreamError
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
 - IMFSinkWriterCallback2::OnStreamError
 - mfreadwrite/IMFSinkWriterCallback2::OnStreamError
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
 - IMFSinkWriterCallback2.OnStreamError
---

# IMFSinkWriterCallback2::OnStreamError


## -description

Called when an asynchronous error occurs with the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>.

## -parameters

### -param dwStreamIndex

The index of the stream of the transform that raised the asynchronous error.

### -param hrStatus

The error that occurred.

## -returns

Returns an <b>HRESULT</b> value. Currently, the sink writer ignores the return value.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback2">IMFSinkWriterCallback2</a>