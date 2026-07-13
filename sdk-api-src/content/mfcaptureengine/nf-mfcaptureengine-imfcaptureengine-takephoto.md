---
UID: NF:mfcaptureengine.IMFCaptureEngine.TakePhoto
title: IMFCaptureEngine::TakePhoto (mfcaptureengine.h)
description: Captures a still image from the video stream.
helpviewer_keywords: ["IMFCaptureEngine interface [Media Foundation]","TakePhoto method","IMFCaptureEngine.TakePhoto","IMFCaptureEngine::TakePhoto","TakePhoto","TakePhoto method [Media Foundation]","TakePhoto method [Media Foundation]","IMFCaptureEngine interface","mf.imfcaptureengine_takephoto","mfcaptureengine/IMFCaptureEngine::TakePhoto"]
old-location: mf\imfcaptureengine_takephoto.htm
tech.root: mf
ms.assetid: 6E633E90-9C8B-44B6-9149-704872143147
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],TakePhoto method, IMFCaptureEngine.TakePhoto, IMFCaptureEngine::TakePhoto, TakePhoto, TakePhoto method [Media Foundation], TakePhoto method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_takephoto, mfcaptureengine/IMFCaptureEngine::TakePhoto
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
 - IMFCaptureEngine::TakePhoto
 - mfcaptureengine/IMFCaptureEngine::TakePhoto
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
 - IMFCaptureEngine.TakePhoto
---

# IMFCaptureEngine::TakePhoto


## -description

Captures a still image from the video stream.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before calling this method, configure the photo sink by calling <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">IMFCaptureSink::AddStream</a>. To get a pointer to the photo sink, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-getsink">IMFCaptureEngine::GetSink</a>. 

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_PHOTO_TAKEN</b> event through the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine">IMFCaptureEngine</a>
