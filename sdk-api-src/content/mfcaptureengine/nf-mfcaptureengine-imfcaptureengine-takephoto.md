---
UID: NF:mfcaptureengine.IMFCaptureEngine.TakePhoto
title: IMFCaptureEngine::TakePhoto
author: windows-sdk-content
description: Captures a still image from the video stream.
old-location: mf\imfcaptureengine_takephoto.htm
tech.root: medfound
ms.assetid: 6E633E90-9C8B-44B6-9149-704872143147
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],TakePhoto method, IMFCaptureEngine.TakePhoto, IMFCaptureEngine::TakePhoto, TakePhoto, TakePhoto method [Media Foundation], TakePhoto method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_takephoto, mfcaptureengine/IMFCaptureEngine::TakePhoto
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
 - IMFCaptureEngine.TakePhoto
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureEngine::TakePhoto


## -description


Captures a still image from the video stream.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before calling this method, configure the photo sink by calling <a href="https://msdn.microsoft.com/5D7A1FE0-92B9-4CC4-A268-17FA848055A9">IMFCaptureSink::AddStream</a>. To get a pointer to the photo sink, call <a href="https://msdn.microsoft.com/7DAF5EA3-BA65-4CF9-B7BA-B427A48BF3BC">IMFCaptureEngine::GetSink</a>. 

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_PHOTO_TAKEN</b> event through the <a href="https://msdn.microsoft.com/26C5B2E5-0543-49FC-915A-DCE097FF66BA">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.




## -see-also




<a href="https://msdn.microsoft.com/4A2A0536-4255-40AB-BCAB-228B09343583">IMFCaptureEngine</a>
 

 

