---
UID: NF:mfcaptureengine.IMFCaptureSource.GetCaptureDeviceSource
title: IMFCaptureSource::GetCaptureDeviceSource
author: windows-sdk-content
description: Gets the current capture device's IMFMediaSource object pointer.
old-location: mf\imfcapturesource_getcapturedevicesource.htm
tech.root: medfound
ms.assetid: 98bce6e3-02f2-449e-aba4-4bfc9de6d1db
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetCaptureDeviceSource, GetCaptureDeviceSource method [Media Foundation], GetCaptureDeviceSource method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetCaptureDeviceSource method, IMFCaptureSource.GetCaptureDeviceSource, IMFCaptureSource::GetCaptureDeviceSource, mf.imfcapturesource_getcapturedevicesource, mfcaptureengine/IMFCaptureSource::GetCaptureDeviceSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureSource.GetCaptureDeviceSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSource::GetCaptureDeviceSource


## -description


Gets the current capture device's <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> object pointer.


## -parameters




### -param mfCaptureEngineDeviceType [in]

The capture engine device type.


### -param ppMediaSource [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> that represent the device.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a>
 

 

