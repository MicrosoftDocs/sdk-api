---
UID: NF:mfcaptureengine.IMFCapturePreviewSink.SetRotation
title: IMFCapturePreviewSink::SetRotation (mfcaptureengine.h)
description: Rotates the video preview stream.
helpviewer_keywords: ["IMFCapturePreviewSink interface [Media Foundation]","SetRotation method","IMFCapturePreviewSink.SetRotation","IMFCapturePreviewSink::SetRotation","SetRotation","SetRotation method [Media Foundation]","SetRotation method [Media Foundation]","IMFCapturePreviewSink interface","mf.imfcapturepreviewsink_setrotation","mfcaptureengine/IMFCapturePreviewSink::SetRotation"]
old-location: mf\imfcapturepreviewsink_setrotation.htm
tech.root: mf
ms.assetid: 84C53A34-B2FB-4D13-9A45-5172E9E3CEE8
ms.date: 12/05/2018
ms.keywords: IMFCapturePreviewSink interface [Media Foundation],SetRotation method, IMFCapturePreviewSink.SetRotation, IMFCapturePreviewSink::SetRotation, SetRotation, SetRotation method [Media Foundation], SetRotation method [Media Foundation],IMFCapturePreviewSink interface, mf.imfcapturepreviewsink_setrotation, mfcaptureengine/IMFCapturePreviewSink::SetRotation
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
 - IMFCapturePreviewSink::SetRotation
 - mfcaptureengine/IMFCapturePreviewSink::SetRotation
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
 - IMFCapturePreviewSink.SetRotation
---

# IMFCapturePreviewSink::SetRotation


## -description

Rotates the video preview stream.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream to rotate. You must specify a video stream.

### -param dwRotationValue [in]

The amount to rotate the video, in degrees. Valid values are 0, 90, 180, and 270. The value zero restores the video to its original orientation.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink">IMFCapturePreviewSink</a>