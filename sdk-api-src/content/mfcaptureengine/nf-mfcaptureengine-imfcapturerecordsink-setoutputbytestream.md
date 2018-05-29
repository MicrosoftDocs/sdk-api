---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.SetOutputByteStream
title: IMFCaptureRecordSink::SetOutputByteStream
author: windows-sdk-content
description: Specifies a byte stream that will receive the data for the recording.
old-location: mf\imfcapturerecordsink_setoutputbytestream.htm
old-project: medfound
ms.assetid: C33357C8-882A-4350-8638-46C2220FC445
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFCaptureRecordSink interface [Media Foundation],SetOutputByteStream method, IMFCaptureRecordSink.SetOutputByteStream, IMFCaptureRecordSink::SetOutputByteStream, SetOutputByteStream, SetOutputByteStream method [Media Foundation], SetOutputByteStream method [Media Foundation],IMFCaptureRecordSink interface, mf.imfcapturerecordsink_setoutputbytestream, mfcaptureengine/IMFCaptureRecordSink::SetOutputByteStream
ms.prod: windows
ms.technology: windows-sdk
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
-	IMFCaptureRecordSink.SetOutputByteStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureRecordSink::SetOutputByteStream


## -description


Specifies a byte stream that will receive the data for the recording.


## -parameters




### -param pByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream. The byte stream must be writable.


### -param guidContainerType [in]

A GUID that specifies the file container type. Possible values are documented in the <a href="https://msdn.microsoft.com/97fd968a-6843-4695-aece-02f9acd618fd">MF_TRANSCODE_CONTAINERTYPE</a>  attribute.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this method overrides any previous call to <a href="https://msdn.microsoft.com/96BEE09C-1B17-4857-B0DC-553D14B908E7">IMFCaptureRecordSink::SetOutputFileName</a> or <a href="https://msdn.microsoft.com/1D7BB0D1-3F77-4AF3-9624-73EE4D0D0BCE">IMFCaptureRecordSink::SetSampleCallback</a>.




## -see-also




<a href="https://msdn.microsoft.com/AEF5923D-C4ED-4BEA-A969-163ED837A5BD">IMFCaptureRecordSink</a>
 

 

