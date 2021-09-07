---
UID: NF:mfcaptureengine.IMFCapturePhotoSink.SetOutputByteStream
title: IMFCapturePhotoSink::SetOutputByteStream (mfcaptureengine.h)
description: Specifies a byte stream that will receive the still image data.
helpviewer_keywords: ["IMFCapturePhotoSink interface [Media Foundation]","SetOutputByteStream method","IMFCapturePhotoSink.SetOutputByteStream","IMFCapturePhotoSink::SetOutputByteStream","SetOutputByteStream","SetOutputByteStream method [Media Foundation]","SetOutputByteStream method [Media Foundation]","IMFCapturePhotoSink interface","mf.imfcapturephotosink_setoutputbytestream","mfcaptureengine/IMFCapturePhotoSink::SetOutputByteStream"]
old-location: mf\imfcapturephotosink_setoutputbytestream.htm
tech.root: mf
ms.assetid: D67C2D66-FC40-4AF3-9E83-29D0DBF99AD3
ms.date: 12/05/2018
ms.keywords: IMFCapturePhotoSink interface [Media Foundation],SetOutputByteStream method, IMFCapturePhotoSink.SetOutputByteStream, IMFCapturePhotoSink::SetOutputByteStream, SetOutputByteStream, SetOutputByteStream method [Media Foundation], SetOutputByteStream method [Media Foundation],IMFCapturePhotoSink interface, mf.imfcapturephotosink_setoutputbytestream, mfcaptureengine/IMFCapturePhotoSink::SetOutputByteStream
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
 - IMFCapturePhotoSink::SetOutputByteStream
 - mfcaptureengine/IMFCapturePhotoSink::SetOutputByteStream
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
 - IMFCapturePhotoSink.SetOutputByteStream
---

# IMFCapturePhotoSink::SetOutputByteStream


## -description

Specifies a byte stream that will receive the still image data.

## -parameters

### -param pByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream. The byte stream must be writable.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling this method overrides any previous call to <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturephotosink-setoutputfilename">IMFCapturePhotoSink::SetOutputFileName</a> or <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturephotosink-setsamplecallback">IMFCapturePhotoSink::SetSampleCallback</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink">IMFCapturePhotoSink</a>