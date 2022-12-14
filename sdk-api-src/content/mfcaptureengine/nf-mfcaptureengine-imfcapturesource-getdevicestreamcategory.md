---
UID: NF:mfcaptureengine.IMFCaptureSource.GetDeviceStreamCategory
title: IMFCaptureSource::GetDeviceStreamCategory (mfcaptureengine.h)
description: Gets the stream category for the specified source stream index.
helpviewer_keywords: ["GetDeviceStreamCategory","GetDeviceStreamCategory method [Media Foundation]","GetDeviceStreamCategory method [Media Foundation]","IMFCaptureSource interface","IMFCaptureSource interface [Media Foundation]","GetDeviceStreamCategory method","IMFCaptureSource.GetDeviceStreamCategory","IMFCaptureSource::GetDeviceStreamCategory","mf.imfcapturesource_getdevicestreamcategory","mfcaptureengine/IMFCaptureSource::GetDeviceStreamCategory"]
old-location: mf\imfcapturesource_getdevicestreamcategory.htm
tech.root: mf
ms.assetid: f3caa002-8676-44d3-9696-da5b0db09d9e
ms.date: 12/05/2018
ms.keywords: GetDeviceStreamCategory, GetDeviceStreamCategory method [Media Foundation], GetDeviceStreamCategory method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetDeviceStreamCategory method, IMFCaptureSource.GetDeviceStreamCategory, IMFCaptureSource::GetDeviceStreamCategory, mf.imfcapturesource_getdevicestreamcategory, mfcaptureengine/IMFCaptureSource::GetDeviceStreamCategory
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
 - IMFCaptureSource::GetDeviceStreamCategory
 - mfcaptureengine/IMFCaptureSource::GetDeviceStreamCategory
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
 - IMFCaptureSource.GetDeviceStreamCategory
---

# IMFCaptureSource::GetDeviceStreamCategory


## -description

Gets the stream category for the specified source stream index.

## -parameters

### -param dwSourceStreamIndex [in]

The index of the source stream.

### -param pStreamCategory [out]

Receives the MF_CAPTURE_ENGINE_STREAM_CATEGORY of the specified source stream.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource">IMFCaptureSource</a>