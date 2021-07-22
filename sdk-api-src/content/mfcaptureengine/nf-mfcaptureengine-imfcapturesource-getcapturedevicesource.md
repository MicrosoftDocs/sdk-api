---
UID: NF:mfcaptureengine.IMFCaptureSource.GetCaptureDeviceSource
title: IMFCaptureSource::GetCaptureDeviceSource (mfcaptureengine.h)
description: Gets the current capture device's IMFMediaSource object pointer.
helpviewer_keywords: ["GetCaptureDeviceSource","GetCaptureDeviceSource method [Media Foundation]","GetCaptureDeviceSource method [Media Foundation]","IMFCaptureSource interface","IMFCaptureSource interface [Media Foundation]","GetCaptureDeviceSource method","IMFCaptureSource.GetCaptureDeviceSource","IMFCaptureSource::GetCaptureDeviceSource","mf.imfcapturesource_getcapturedevicesource","mfcaptureengine/IMFCaptureSource::GetCaptureDeviceSource"]
old-location: mf\imfcapturesource_getcapturedevicesource.htm
tech.root: mf
ms.assetid: 98bce6e3-02f2-449e-aba4-4bfc9de6d1db
ms.date: 12/05/2018
ms.keywords: GetCaptureDeviceSource, GetCaptureDeviceSource method [Media Foundation], GetCaptureDeviceSource method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetCaptureDeviceSource method, IMFCaptureSource.GetCaptureDeviceSource, IMFCaptureSource::GetCaptureDeviceSource, mf.imfcapturesource_getcapturedevicesource, mfcaptureengine/IMFCaptureSource::GetCaptureDeviceSource
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
 - IMFCaptureSource::GetCaptureDeviceSource
 - mfcaptureengine/IMFCaptureSource::GetCaptureDeviceSource
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
 - IMFCaptureSource.GetCaptureDeviceSource
---

# IMFCaptureSource::GetCaptureDeviceSource


## -description

Gets the current capture device's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> object pointer.

## -parameters

### -param mfCaptureEngineDeviceType [in]

The capture engine device type.

### -param ppMediaSource [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> that represent the device.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource">IMFCaptureSource</a>