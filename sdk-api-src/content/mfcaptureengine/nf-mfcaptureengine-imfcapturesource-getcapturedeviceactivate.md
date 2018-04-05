---
UID: NF:mfcaptureengine.IMFCaptureSource.GetCaptureDeviceActivate
title: IMFCaptureSource::GetCaptureDeviceActivate method
author: windows-driver-content
description: Gets the current capture device's IMFActivate object pointer.
old-location: mf\imfcapturesource_getcapturedeviceactivate.htm
old-project: medfound
ms.assetid: 5f69321f-67df-4d6c-a98a-51a9859f8a22
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetCaptureDeviceActivate method [Media Foundation], GetCaptureDeviceActivate method [Media Foundation], IMFCaptureSource interface, GetCaptureDeviceActivate,IMFCaptureSource.GetCaptureDeviceActivate, IMFCaptureSource, IMFCaptureSource interface [Media Foundation], GetCaptureDeviceActivate method, IMFCaptureSource::GetCaptureDeviceActivate, mf.imfcapturesource_getcapturedeviceactivate, mfcaptureengine/IMFCaptureSource::GetCaptureDeviceActivate
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
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfcaptureengine.h
api_name:
-	IMFCaptureSource.GetCaptureDeviceActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureSource::GetCaptureDeviceActivate method


## -description


 Gets the current capture device's <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> object pointer.


## -parameters




### -param mfCaptureEngineDeviceType [in]

The capture engine device type.


### -param ppActivate [out]

Receives the pointer to a <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> that represents a device.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a>
 

 

