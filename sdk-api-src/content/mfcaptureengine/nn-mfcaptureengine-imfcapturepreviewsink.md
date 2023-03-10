---
UID: NN:mfcaptureengine.IMFCapturePreviewSink
title: IMFCapturePreviewSink (mfcaptureengine.h)
description: Controls the preview sink.
helpviewer_keywords: ["IMFCapturePreviewSink","IMFCapturePreviewSink interface [Media Foundation]","IMFCapturePreviewSink interface [Media Foundation]","described","mf.imfcapturepreviewsink","mfcaptureengine/IMFCapturePreviewSink"]
old-location: mf\imfcapturepreviewsink.htm
tech.root: mf
ms.assetid: 5E64C24D-D6EC-419B-9DC8-309EBCE0077E
ms.date: 12/05/2018
ms.keywords: IMFCapturePreviewSink, IMFCapturePreviewSink interface [Media Foundation], IMFCapturePreviewSink interface [Media Foundation],described, mf.imfcapturepreviewsink, mfcaptureengine/IMFCapturePreviewSink
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
 - IMFCapturePreviewSink
 - mfcaptureengine/IMFCapturePreviewSink
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
 - IMFCapturePreviewSink
---

# IMFCapturePreviewSink interface


## -description

Controls the preview sink. The preview sink enables the application to preview audio and video from the camera.

## -inheritance

The <b>IMFCapturePreviewSink</b> interface inherits from <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>. <b>IMFCapturePreviewSink</b> also has these types of members:

## -remarks

To start preview, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-startpreview">IMFCaptureEngine::StartPreview</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
