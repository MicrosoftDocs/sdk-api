---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.GetMirrorState
title: IMFCapturePreviewSink::GetMirrorState
author: windows-sdk-content
description: Gets the current mirroring state of the video preview stream.
old-location: mf\imfcapturepreviewsink_getmirrorstate.htm
old-project: medfound
ms.assetid: 6EFC9DFF-4029-46F0-9357-983FE528D4FE
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetMirrorState, GetMirrorState method [Media Foundation], GetMirrorState method [Media Foundation],IMFCapturePreviewSink interface, IMFCapturePreviewSink interface [Media Foundation],GetMirrorState method, IMFCapturePreviewSink.GetMirrorState, IMFCapturePreviewSink::GetMirrorState, mf.imfcapturepreviewsink_getmirrorstate, mfcaptureengine/IMFCapturePreviewSink::GetMirrorState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfcaptureengine.h
req.include-header: 
req.redist: 
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
 - IMFCapturePreviewSink.GetMirrorState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCapturePreviewSink::GetMirrorState


## -description


Gets the current mirroring state of the video preview stream.


## -parameters




### -param pfMirrorState [out]

Receives the value <b>TRUE</b> if mirroring is enabled, or <b>FALSE</b> if mirroring is disabled.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5E64C24D-D6EC-419B-9DC8-309EBCE0077E">IMFCapturePreviewSink</a>
 

 

