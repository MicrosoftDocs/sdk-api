---
UID: NF:mfcaptureengine.IMFCapturePhotoSink.SetSampleCallback
title: IMFCapturePhotoSink::SetSampleCallback (mfcaptureengine.h)
description: Sets a callback to receive the still-image data.
helpviewer_keywords: ["IMFCapturePhotoSink interface [Media Foundation]","SetSampleCallback method","IMFCapturePhotoSink.SetSampleCallback","IMFCapturePhotoSink::SetSampleCallback","SetSampleCallback","SetSampleCallback method [Media Foundation]","SetSampleCallback method [Media Foundation]","IMFCapturePhotoSink interface","mf.imfcapturephotosink_setsamplecallback","mfcaptureengine/IMFCapturePhotoSink::SetSampleCallback"]
old-location: mf\imfcapturephotosink_setsamplecallback.htm
tech.root: mf
ms.assetid: 595716F6-8059-4B56-9FB3-906846BA3CBB
ms.date: 12/05/2018
ms.keywords: IMFCapturePhotoSink interface [Media Foundation],SetSampleCallback method, IMFCapturePhotoSink.SetSampleCallback, IMFCapturePhotoSink::SetSampleCallback, SetSampleCallback, SetSampleCallback method [Media Foundation], SetSampleCallback method [Media Foundation],IMFCapturePhotoSink interface, mf.imfcapturephotosink_setsamplecallback, mfcaptureengine/IMFCapturePhotoSink::SetSampleCallback
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
 - IMFCapturePhotoSink::SetSampleCallback
 - mfcaptureengine/IMFCapturePhotoSink::SetSampleCallback
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
 - IMFCapturePhotoSink.SetSampleCallback
---

# IMFCapturePhotoSink::SetSampleCallback


## -description

Sets a callback to receive the still-image data.

## -parameters

### -param pCallback [in]

A pointer to the <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback">IMFCaptureEngineOnSampleCallback</a> interface. The caller must implement this interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling this method overrides any previous call to <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturephotosink-setoutputbytestream">IMFCapturePhotoSink::SetOutputByteStream</a> or  <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturephotosink-setoutputfilename">IMFCapturePhotoSink::SetOutputFileName</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink">IMFCapturePhotoSink</a>