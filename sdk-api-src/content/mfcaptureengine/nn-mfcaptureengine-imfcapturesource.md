---
UID: NN:mfcaptureengine.IMFCaptureSource
title: IMFCaptureSource (mfcaptureengine.h)
description: Controls the capture source object. The capture source manages the audio and video capture devices.
helpviewer_keywords: ["IMFCaptureSource","IMFCaptureSource interface [Media Foundation]","IMFCaptureSource interface [Media Foundation]","described","mf.imfcapturesource","mfcaptureengine/IMFCaptureSource"]
old-location: mf\imfcapturesource.htm
tech.root: mf
ms.assetid: 864B6B5D-EB7E-4C49-A326-9B6704A27635
ms.date: 12/05/2018
ms.keywords: IMFCaptureSource, IMFCaptureSource interface [Media Foundation], IMFCaptureSource interface [Media Foundation],described, mf.imfcapturesource, mfcaptureengine/IMFCaptureSource
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
 - IMFCaptureSource
 - mfcaptureengine/IMFCaptureSource
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
 - IMFCaptureSource
---

# IMFCaptureSource interface


## -description

Controls the capture source object. The capture source manages the audio and video capture devices.

## -inheritance

The <b>IMFCaptureSource</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureSource</b> also has these types of members:

## -remarks

To get a pointer to the capture source, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-getsource">IMFCaptureEngine::GetSource</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
