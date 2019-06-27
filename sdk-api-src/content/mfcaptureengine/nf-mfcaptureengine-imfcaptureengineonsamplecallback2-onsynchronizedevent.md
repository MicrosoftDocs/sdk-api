---
UID: NF:mfcaptureengine.IMFCaptureEngineOnSampleCallback2.OnSynchronizedEvent
title: IMFCaptureEngineOnSampleCallback2::OnSynchronizedEvent (mfcaptureengine.h)
author: windows-sdk-content
description: Called by the capture sink when the format of the sample is changed.
old-location: mf\imfcaptureengineonsamplecallback2_onsynchronizedevent.htm
tech.root: medfound
ms.assetid: f82a657a-bc6a-407b-ad72-1e9c6ec17bed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngineOnSampleCallback2 interface [Media Foundation],OnSynchronizedEvent method, IMFCaptureEngineOnSampleCallback2.OnSynchronizedEvent, IMFCaptureEngineOnSampleCallback2::OnSynchronizedEvent, OnSynchronizedEvent, OnSynchronizedEvent method [Media Foundation], OnSynchronizedEvent method [Media Foundation],IMFCaptureEngineOnSampleCallback2 interface, mf.imfcaptureengineonsamplecallback2_onsynchronizedevent, mfcaptureengine/IMFCaptureEngineOnSampleCallback2::OnSynchronizedEvent
ms.topic: method
f1_keywords: 
 - "mfcaptureengine/IMFCaptureEngineOnSampleCallback2.OnSynchronizedEvent"
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfcaptureengine.idl
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
 - IMFCaptureEngineOnSampleCallback2.OnSynchronizedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCaptureEngineOnSampleCallback2::OnSynchronizedEvent


## -description


Called by the capture sink when the format of the sample is changed.


## -parameters




### -param pEvent [in]

The new media type.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The return value is ignored.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback2">IMFCaptureEngineOnSampleCallback2</a>
 

 

