---
UID: NN:mfcaptureengine.IMFCapturePhotoSink
title: IMFCapturePhotoSink (mfcaptureengine.h)
description: Controls the photo sink.
helpviewer_keywords: ["IMFCapturePhotoSink","IMFCapturePhotoSink interface [Media Foundation]","IMFCapturePhotoSink interface [Media Foundation]","described","mf.imfcapturephotosink","mfcaptureengine/IMFCapturePhotoSink"]
old-location: mf\imfcapturephotosink.htm
tech.root: mf
ms.assetid: 14BB9A86-47F2-4CFE-A932-3F2C7B6AF2BA
ms.date: 12/05/2018
ms.keywords: IMFCapturePhotoSink, IMFCapturePhotoSink interface [Media Foundation], IMFCapturePhotoSink interface [Media Foundation],described, mf.imfcapturephotosink, mfcaptureengine/IMFCapturePhotoSink
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
 - IMFCapturePhotoSink
 - mfcaptureengine/IMFCapturePhotoSink
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
 - IMFCapturePhotoSink
---

# IMFCapturePhotoSink interface


## -description

Controls the photo sink. The photo sink captures still images from the video stream.

## -inheritance

The <b>IMFCapturePhotoSink</b> interface inherits from <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>. <b>IMFCapturePhotoSink</b> also has these types of members:

## -remarks

The photo sink can deliver samples to one of the following destinations:

<ul>
<li>Byte stream.</li>
<li>Output file.</li>
<li>Application-provided callback interface.</li>
</ul>
The application must specify a single destination. Multiple destinations are not supported.

To capture an image, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-takephoto">IMFCaptureEngine::TakePhoto</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
