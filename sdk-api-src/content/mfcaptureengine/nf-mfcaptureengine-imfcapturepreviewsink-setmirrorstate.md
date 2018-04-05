---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.SetMirrorState
title: IMFCapturePreviewSink::SetMirrorState method
author: windows-driver-content
description: Enables or disables mirroring of the video preview stream.
old-location: mf\imfcapturepreviewsink_setmirrorstate.htm
old-project: medfound
ms.assetid: F7F04E29-E7AD-46BD-AAF9-5B7BA68822EE
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMFCapturePreviewSink, IMFCapturePreviewSink interface [Media Foundation], SetMirrorState method, IMFCapturePreviewSink::SetMirrorState, SetMirrorState method [Media Foundation], SetMirrorState method [Media Foundation], IMFCapturePreviewSink interface, SetMirrorState,IMFCapturePreviewSink.SetMirrorState, mf.imfcapturepreviewsink_setmirrorstate, mfcaptureengine/IMFCapturePreviewSink::SetMirrorState
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
-	IMFCapturePreviewSink.SetMirrorState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCapturePreviewSink::SetMirrorState method


## -description


Enables or disables mirroring of the video preview stream.


## -parameters




### -param fMirrorState [in]

If   <b>TRUE</b>, mirroring is enabled. If <b>FALSE</b>, mirror is disabled.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5E64C24D-D6EC-419B-9DC8-309EBCE0077E">IMFCapturePreviewSink</a>
 

 

