---
UID: NF:mfcaptureengine.IMFCaptureEngineOnSampleCallback.OnSample
title: IMFCaptureEngineOnSampleCallback::OnSample (mfcaptureengine.h)
description: Called when the capture sink receives a sample.
helpviewer_keywords: ["IMFCaptureEngineOnSampleCallback interface [Media Foundation]","OnSample method","IMFCaptureEngineOnSampleCallback.OnSample","IMFCaptureEngineOnSampleCallback::OnSample","OnSample","OnSample method [Media Foundation]","OnSample method [Media Foundation]","IMFCaptureEngineOnSampleCallback interface","mf.imfcaptureengineonsamplecallback_onsample","mfcaptureengine/IMFCaptureEngineOnSampleCallback::OnSample"]
old-location: mf\imfcaptureengineonsamplecallback_onsample.htm
tech.root: mf
ms.assetid: 83FEFE33-DEAD-4CE0-9EEE-B8F3801ADC1C
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngineOnSampleCallback interface [Media Foundation],OnSample method, IMFCaptureEngineOnSampleCallback.OnSample, IMFCaptureEngineOnSampleCallback::OnSample, OnSample, OnSample method [Media Foundation], OnSample method [Media Foundation],IMFCaptureEngineOnSampleCallback interface, mf.imfcaptureengineonsamplecallback_onsample, mfcaptureengine/IMFCaptureEngineOnSampleCallback::OnSample
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
 - IMFCaptureEngineOnSampleCallback::OnSample
 - mfcaptureengine/IMFCaptureEngineOnSampleCallback::OnSample
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
 - IMFCaptureEngineOnSampleCallback.OnSample
---

# IMFCaptureEngineOnSampleCallback::OnSample


## -description

Called when the capture sink receives a sample.

## -parameters

### -param pSample [in, optional]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface. Use this interface to get the time stamp, duration, and stream data. For more information, see <a href="/windows/desktop/medfound/media-samples">Media Samples</a>. This parameter can be <b>NULL</b>, so make sure to check for a <b>NULL</b> value before you dereference the pointer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback">IMFCaptureEngineOnSampleCallback</a>