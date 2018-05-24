---
UID: NF:mfcaptureengine.IMFCapturePhotoSink.SetOutputByteStream
title: IMFCapturePhotoSink::SetOutputByteStream
author: windows-driver-content
description: Specifies a byte stream that will receive the still image data.
old-location: mf\imfcapturephotosink_setoutputbytestream.htm
old-project: medfound
ms.assetid: D67C2D66-FC40-4AF3-9E83-29D0DBF99AD3
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IMFCapturePhotoSink interface [Media Foundation],SetOutputByteStream method, IMFCapturePhotoSink.SetOutputByteStream, IMFCapturePhotoSink::SetOutputByteStream, SetOutputByteStream, SetOutputByteStream method [Media Foundation], SetOutputByteStream method [Media Foundation],IMFCapturePhotoSink interface, mf.imfcapturephotosink_setoutputbytestream, mfcaptureengine/IMFCapturePhotoSink::SetOutputByteStream
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
-	IMFCapturePhotoSink.SetOutputByteStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCapturePhotoSink::SetOutputByteStream


## -description


Specifies a byte stream that will receive the still image data.


## -parameters




### -param pByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream. The byte stream must be writable.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this method overrides any previous call to <a href="https://msdn.microsoft.com/CAA9F7CF-A92F-4039-BEA5-07A730E82EE4">IMFCapturePhotoSink::SetOutputFileName</a> or <a href="https://msdn.microsoft.com/595716F6-8059-4B56-9FB3-906846BA3CBB">IMFCapturePhotoSink::SetSampleCallback</a>.




## -see-also




<a href="https://msdn.microsoft.com/14BB9A86-47F2-4CFE-A932-3F2C7B6AF2BA">IMFCapturePhotoSink</a>
 

 

