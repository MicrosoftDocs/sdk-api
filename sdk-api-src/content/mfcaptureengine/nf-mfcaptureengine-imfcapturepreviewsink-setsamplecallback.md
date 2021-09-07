---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.SetSampleCallback
title: IMFCapturePreviewSink::SetSampleCallback (mfcaptureengine.h)
description: Sets a callback to receive the preview data for one stream.
helpviewer_keywords: ["IMFCapturePreviewSink interface [Media Foundation]","SetSampleCallback method","IMFCapturePreviewSink.SetSampleCallback","IMFCapturePreviewSink::SetSampleCallback","SetSampleCallback","SetSampleCallback method [Media Foundation]","SetSampleCallback method [Media Foundation]","IMFCapturePreviewSink interface","mf.imfcapturepreviewsink_setsamplecallback","mfcaptureengine/IMFCapturePreviewSink::SetSampleCallback"]
old-location: mf\imfcapturepreviewsink_setsamplecallback.htm
tech.root: mf
ms.assetid: 0E14E3E4-25C7-4FCA-B220-20E346E66933
ms.date: 12/05/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],SetSampleCallback method, IMFCapturePreviewSink.SetSampleCallback, IMFCapturePreviewSink::SetSampleCallback, SetSampleCallback, SetSampleCallback method [Media Foundation], SetSampleCallback method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_setsamplecallback, mfcaptureengine/IMFCapturePreviewSink::SetSampleCallback
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFCapturePreviewSink::SetSampleCallback
 - mfcaptureengine/IMFCapturePreviewSink::SetSampleCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCapturePreviewSink.SetSampleCallback
---

# IMFCapturePreviewSink::SetSampleCallback


## -description

Sets a callback to receive the preview data for one stream.

## -parameters

### -param dwStreamSinkIndex [in]

The zero-based index of the stream. The index is returned in the <i>pdwSinkStreamIndex</i> parameter of the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">IMFCaptureSink::AddStream</a> method.

### -param pCallback [in]

A pointer to the <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback">IMFCaptureEngineOnSampleCallback</a> interface. The caller must implement this interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling this method overrides any previous call to <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-setrenderhandle">IMFCapturePreviewSink::SetRenderHandle</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink">IMFCapturePreviewSink</a>