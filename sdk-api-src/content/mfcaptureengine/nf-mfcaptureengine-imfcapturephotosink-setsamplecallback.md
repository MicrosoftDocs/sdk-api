---
UID: NF:mfcaptureengine.IMFCapturePhotoSink.SetSampleCallback
title: IMFCapturePhotoSink::SetSampleCallback
author: windows-sdk-content
description: Sets a callback to receive the still-image data.
old-location: mf\imfcapturephotosink_setsamplecallback.htm
tech.root: medfound
ms.assetid: 595716F6-8059-4B56-9FB3-906846BA3CBB
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMFCapturePhotoSink interface [Media Foundation],SetSampleCallback method, IMFCapturePhotoSink.SetSampleCallback, IMFCapturePhotoSink::SetSampleCallback, SetSampleCallback, SetSampleCallback method [Media Foundation], SetSampleCallback method [Media Foundation],IMFCapturePhotoSink interface, mf.imfcapturephotosink_setsamplecallback, mfcaptureengine/IMFCapturePhotoSink::SetSampleCallback
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
 - IMFCapturePhotoSink.SetSampleCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCapturePhotoSink::SetSampleCallback


## -description


Sets a callback to receive the still-image data.


## -parameters




### -param pCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7C621525-CCD2-45EC-9E7A-3A774B96EA6F">IMFCaptureEngineOnSampleCallback</a> interface. The caller must implement this interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this method overrides any previous call to <a href="https://msdn.microsoft.com/D67C2D66-FC40-4AF3-9E83-29D0DBF99AD3">IMFCapturePhotoSink::SetOutputByteStream</a> or  <a href="https://msdn.microsoft.com/CAA9F7CF-A92F-4039-BEA5-07A730E82EE4">IMFCapturePhotoSink::SetOutputFileName</a>.




## -see-also




<a href="https://msdn.microsoft.com/14BB9A86-47F2-4CFE-A932-3F2C7B6AF2BA">IMFCapturePhotoSink</a>
 

 

