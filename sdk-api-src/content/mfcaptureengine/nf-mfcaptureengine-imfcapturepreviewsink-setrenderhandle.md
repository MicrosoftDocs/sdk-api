---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.SetRenderHandle
title: IMFCapturePreviewSink::SetRenderHandle
author: windows-sdk-content
description: Specifies a window for preview.
old-location: mf\imfcapturepreviewsink_setrenderhandle.htm
old-project: medfound
ms.assetid: 98D3EFC4-841D-41EC-BC5C-E67029663864
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],SetRenderHandle method, IMFCapturePreviewSink.SetRenderHandle, IMFCapturePreviewSink::SetRenderHandle, SetRenderHandle, SetRenderHandle method [Media Foundation], SetRenderHandle method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_setrenderhandle, mfcaptureengine/IMFCapturePreviewSink::SetRenderHandle
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
-	IMFCapturePreviewSink.SetRenderHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCapturePreviewSink::SetRenderHandle


## -description


Specifies a window for preview.


## -parameters




### -param handle [in]

A handle to the window. The preview sink draws the video frames inside this window.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this method overrides any previous call to <a href="https://msdn.microsoft.com/0E14E3E4-25C7-4FCA-B220-20E346E66933">IMFCapturePreviewSink::SetSampleCallback</a>.




## -see-also




<a href="https://msdn.microsoft.com/5E64C24D-D6EC-419B-9DC8-309EBCE0077E">IMFCapturePreviewSink</a>
 

 

