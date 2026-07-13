---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.SetMirrorState
title: IMFCapturePreviewSink::SetMirrorState (mfcaptureengine.h)
description: Enables or disables mirroring of the video preview stream. (IMFCapturePreviewSink.SetMirrorState)
helpviewer_keywords: ["IMFCapturePreviewSink interface [Media Foundation]","SetMirrorState method","IMFCapturePreviewSink.SetMirrorState","IMFCapturePreviewSink::SetMirrorState","SetMirrorState","SetMirrorState method [Media Foundation]","SetMirrorState method [Media Foundation]","IMFCapturePreviewSink interface","mf.imfcapturepreviewsink_setmirrorstate","mfcaptureengine/IMFCapturePreviewSink::SetMirrorState"]
old-location: mf\imfcapturepreviewsink_setmirrorstate.htm
tech.root: mf
ms.assetid: F7F04E29-E7AD-46BD-AAF9-5B7BA68822EE
ms.date: 12/05/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],SetMirrorState method, IMFCapturePreviewSink.SetMirrorState, IMFCapturePreviewSink::SetMirrorState, SetMirrorState, SetMirrorState method [Media Foundation], SetMirrorState method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_setmirrorstate, mfcaptureengine/IMFCapturePreviewSink::SetMirrorState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFCapturePreviewSink::SetMirrorState
 - mfcaptureengine/IMFCapturePreviewSink::SetMirrorState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCapturePreviewSink.SetMirrorState
---

# IMFCapturePreviewSink::SetMirrorState


## -description

Enables or disables mirroring of the video preview stream.

## -parameters

### -param fMirrorState [in]

If   <b>TRUE</b>, mirroring is enabled. If <b>FALSE</b>, mirror is disabled.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink">IMFCapturePreviewSink</a>
