---
UID: NF:mfcaptureengine.IMFCaptureSource.GetCaptureDeviceActivate
title: IMFCaptureSource::GetCaptureDeviceActivate (mfcaptureengine.h)
description: Gets the current capture device's IMFActivate object pointer.
helpviewer_keywords: ["GetCaptureDeviceActivate","GetCaptureDeviceActivate method [Media Foundation]","GetCaptureDeviceActivate method [Media Foundation]","IMFCaptureSource interface","IMFCaptureSource interface [Media Foundation]","GetCaptureDeviceActivate method","IMFCaptureSource.GetCaptureDeviceActivate","IMFCaptureSource::GetCaptureDeviceActivate","mf.imfcapturesource_getcapturedeviceactivate","mfcaptureengine/IMFCaptureSource::GetCaptureDeviceActivate"]
old-location: mf\imfcapturesource_getcapturedeviceactivate.htm
tech.root: mf
ms.assetid: 5f69321f-67df-4d6c-a98a-51a9859f8a22
ms.date: 12/05/2018
ms.keywords: GetCaptureDeviceActivate, GetCaptureDeviceActivate method [Media Foundation], GetCaptureDeviceActivate method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetCaptureDeviceActivate method, IMFCaptureSource.GetCaptureDeviceActivate, IMFCaptureSource::GetCaptureDeviceActivate, mf.imfcapturesource_getcapturedeviceactivate, mfcaptureengine/IMFCaptureSource::GetCaptureDeviceActivate
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
 - IMFCaptureSource::GetCaptureDeviceActivate
 - mfcaptureengine/IMFCaptureSource::GetCaptureDeviceActivate
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
 - IMFCaptureSource.GetCaptureDeviceActivate
---

# IMFCaptureSource::GetCaptureDeviceActivate


## -description

 Gets the current capture device's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> object pointer.

## -parameters

### -param mfCaptureEngineDeviceType [in]

The capture engine device type.

### -param ppActivate [out]

Receives the pointer to a <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> that represents a device.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource">IMFCaptureSource</a>