---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.SetCustomSink
title: IMFCaptureRecordSink::SetCustomSink
author: windows-driver-content
description: Sets a custom media sink for recording.
old-location: mf\imfcapturerecordsink_setcustomsink.htm
old-project: medfound
ms.assetid: 76140ECF-E7A2-4C41-A710-813B2DF8F52C
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IMFCaptureRecordSink interface [Media Foundation],SetCustomSink method, IMFCaptureRecordSink.SetCustomSink, IMFCaptureRecordSink::SetCustomSink, SetCustomSink, SetCustomSink method [Media Foundation], SetCustomSink method [Media Foundation],IMFCaptureRecordSink interface, mf.imfcapturerecordsink_setcustomsink, mfcaptureengine/IMFCaptureRecordSink::SetCustomSink
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
-	IMFCaptureRecordSink.SetCustomSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureRecordSink::SetCustomSink


## -description


Sets a custom media sink for recording.


## -parameters




### -param pMediaSink [in]

A pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface of the media sink.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method overrides the default selection of the media sink for recording.




## -see-also




<a href="https://msdn.microsoft.com/AEF5923D-C4ED-4BEA-A969-163ED837A5BD">IMFCaptureRecordSink</a>
 

 

