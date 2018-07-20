---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.UpdateVideo
title: IMFCapturePreviewSink::UpdateVideo
author: windows-sdk-content
description: Updates the video frame.
old-location: mf\imfcapturepreviewsink_updatevideo.htm
old-project: medfound
ms.assetid: B541D209-BB03-4FCF-834C-82002037C357
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],UpdateVideo method, IMFCapturePreviewSink.UpdateVideo, IMFCapturePreviewSink::UpdateVideo, UpdateVideo, UpdateVideo method [Media Foundation], UpdateVideo method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_updatevideo, mfcaptureengine/IMFCapturePreviewSink::UpdateVideo
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
tech.root: 
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCapturePreviewSink.UpdateVideo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCapturePreviewSink::UpdateVideo


## -description


Updates the video frame.  Call this method when the preview window receives a <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> or <a href="https://msdn.microsoft.com/e3e14dcd-9236-48bd-a692-6985d8146f81">WM_SIZE</a> message.


## -parameters




### -param pSrc [in]

A pointer to an <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure that specifies the source rectangle. The source rectangle defines the area of the video frame that is displayed. If this parameter is <b>NULL</b>, the entire video frame is displayed.


### -param pDst [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the destination rectangle. The destination rectangle defines the area of the window or DirectComposition visual where the video is drawn.


### -param pBorderClr [in]

The border color. Use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro to create this value. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5E64C24D-D6EC-419B-9DC8-309EBCE0077E">IMFCapturePreviewSink</a>
 

 

