---
UID: NF:mfcaptureengine.IMFCaptureEngineOnSampleCallback.OnSample
title: IMFCaptureEngineOnSampleCallback::OnSample
author: windows-sdk-content
description: Called when the capture sink receives a sample.
old-location: mf\imfcaptureengineonsamplecallback_onsample.htm
tech.root: medfound
ms.assetid: 83FEFE33-DEAD-4CE0-9EEE-B8F3801ADC1C
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IMFCaptureEngineOnSampleCallback interface [Media Foundation],OnSample method, IMFCaptureEngineOnSampleCallback.OnSample, IMFCaptureEngineOnSampleCallback::OnSample, OnSample, OnSample method [Media Foundation], OnSample method [Media Foundation],IMFCaptureEngineOnSampleCallback interface, mf.imfcaptureengineonsamplecallback_onsample, mfcaptureengine/IMFCaptureEngineOnSampleCallback::OnSample
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
 - IMFCaptureEngineOnSampleCallback.OnSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureEngineOnSampleCallback::OnSample


## -description


Called when the capture sink receives a sample.


## -parameters




### -param pSample [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface. Use this interface to get the time stamp, duration, and stream data. For more information, see <a href="https://msdn.microsoft.com/14389eea-8091-4c10-849e-53db3e98a7c8">Media Samples</a>. This parameter can be <b>NULL</b>, so make sure to check for a <b>NULL</b> value before you dereference the pointer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7C621525-CCD2-45EC-9E7A-3A774B96EA6F">IMFCaptureEngineOnSampleCallback</a>
 

 

