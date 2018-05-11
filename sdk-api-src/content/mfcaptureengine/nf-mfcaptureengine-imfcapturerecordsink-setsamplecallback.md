---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.SetSampleCallback
title: IMFCaptureRecordSink::SetSampleCallback
author: windows-driver-content
description: Sets a callback to receive the recording data for one stream.
old-location: mf\imfcapturerecordsink_setsamplecallback.htm
old-project: medfound
ms.assetid: 1D7BB0D1-3F77-4AF3-9624-73EE4D0D0BCE
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFCaptureRecordSink interface [Media Foundation],SetSampleCallback method, IMFCaptureRecordSink.SetSampleCallback, IMFCaptureRecordSink::SetSampleCallback, SetSampleCallback, SetSampleCallback method [Media Foundation], SetSampleCallback method [Media Foundation],IMFCaptureRecordSink interface, mf.imfcapturerecordsink_setsamplecallback, mfcaptureengine/IMFCaptureRecordSink::SetSampleCallback
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
-	IMFCaptureRecordSink.SetSampleCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureRecordSink::SetSampleCallback


## -description


Sets a callback to receive the recording data for one stream.


## -parameters




### -param dwStreamSinkIndex [in]

The zero-based index of the stream. The index is returned in the <i>pdwSinkStreamIndex</i> parameter of the <a href="https://msdn.microsoft.com/5D7A1FE0-92B9-4CC4-A268-17FA848055A9">IMFCaptureSink::AddStream</a> method.


### -param pCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7C621525-CCD2-45EC-9E7A-3A774B96EA6F">IMFCaptureEngineOnSampleCallback</a> interface. The caller must implement this interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this method overrides any previous call to <a href="https://msdn.microsoft.com/C33357C8-882A-4350-8638-46C2220FC445">IMFCaptureRecordSink::SetOutputByteStream</a> or  <a href="https://msdn.microsoft.com/96BEE09C-1B17-4857-B0DC-553D14B908E7">IMFCaptureRecordSink::SetOutputFileName</a>.




## -see-also




<a href="https://msdn.microsoft.com/AEF5923D-C4ED-4BEA-A969-163ED837A5BD">IMFCaptureRecordSink</a>
 

 

