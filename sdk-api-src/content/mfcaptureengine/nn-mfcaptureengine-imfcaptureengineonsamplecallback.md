---
UID: NN:mfcaptureengine.IMFCaptureEngineOnSampleCallback
title: IMFCaptureEngineOnSampleCallback (mfcaptureengine.h)
description: Callback interface to receive data from the capture engine.
helpviewer_keywords: ["IMFCaptureEngineOnSampleCallback","IMFCaptureEngineOnSampleCallback interface [Media Foundation]","IMFCaptureEngineOnSampleCallback interface [Media Foundation]","described","mf.imfcaptureengineonsamplecallback","mfcaptureengine/IMFCaptureEngineOnSampleCallback"]
old-location: mf\imfcaptureengineonsamplecallback.htm
tech.root: mf
ms.assetid: 7C621525-CCD2-45EC-9E7A-3A774B96EA6F
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngineOnSampleCallback, IMFCaptureEngineOnSampleCallback interface [Media Foundation], IMFCaptureEngineOnSampleCallback interface [Media Foundation],described, mf.imfcaptureengineonsamplecallback, mfcaptureengine/IMFCaptureEngineOnSampleCallback
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
 - IMFCaptureEngineOnSampleCallback
 - mfcaptureengine/IMFCaptureEngineOnSampleCallback
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
 - IMFCaptureEngineOnSampleCallback
---

# IMFCaptureEngineOnSampleCallback interface


## -description

Callback interface to receive data from the capture engine.

## -inheritance

The <b>IMFCaptureEngineOnSampleCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureEngineOnSampleCallback</b> also has these types of members:

## -remarks

To set the callback interface, call one of the following methods.

<ul>
<li>
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturephotosink-setsamplecallback">IMFCapturePhotoSink::SetSampleCallback</a>
</li>
<li>
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturepreviewsink-setsamplecallback">IMFCapturePreviewSink::SetSampleCallback</a>
</li>
<li>
<a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setsamplecallback">IMFCaptureRecordSink::SetSampleCallback</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
