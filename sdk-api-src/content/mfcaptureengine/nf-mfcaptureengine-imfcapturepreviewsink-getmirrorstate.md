---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.GetMirrorState
title: IMFCapturePreviewSink::GetMirrorState (mfcaptureengine.h)
description: Gets the current mirroring state of the video preview stream.
helpviewer_keywords: ["GetMirrorState","GetMirrorState method [Media Foundation]","GetMirrorState method [Media Foundation]","IMFCapturePreviewSink interface","IMFCapturePreviewSink interface [Media Foundation]","GetMirrorState method","IMFCapturePreviewSink.GetMirrorState","IMFCapturePreviewSink::GetMirrorState","mf.imfcapturepreviewsink_getmirrorstate","mfcaptureengine/IMFCapturePreviewSink::GetMirrorState"]
old-location: mf\imfcapturepreviewsink_getmirrorstate.htm
tech.root: mf
ms.assetid: 6EFC9DFF-4029-46F0-9357-983FE528D4FE
ms.date: 12/05/2018
ms.keywords: GetMirrorState, GetMirrorState method [Media Foundation], GetMirrorState method [Media Foundation],IMFCapturePreviewSink interface, IMFCapturePreviewSink interface [Media Foundation],GetMirrorState method, IMFCapturePreviewSink.GetMirrorState, IMFCapturePreviewSink::GetMirrorState, mf.imfcapturepreviewsink_getmirrorstate, mfcaptureengine/IMFCapturePreviewSink::GetMirrorState
f1_keywords:
- mfcaptureengine/IMFCapturePreviewSink.GetMirrorState
dev_langs:
- c++
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
- IMFCapturePreviewSink.GetMirrorState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink">IMFCapturePreviewSink</a>
 

 

