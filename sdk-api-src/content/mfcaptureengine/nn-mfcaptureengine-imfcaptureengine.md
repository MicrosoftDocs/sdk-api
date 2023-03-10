---
UID: NN:mfcaptureengine.IMFCaptureEngine
title: IMFCaptureEngine (mfcaptureengine.h)
description: Controls one or more capture devices.
helpviewer_keywords: ["IMFCaptureEngine","IMFCaptureEngine interface [Media Foundation]","IMFCaptureEngine interface [Media Foundation]","described","mf.imfcaptureengine","mfcaptureengine/IMFCaptureEngine"]
old-location: mf\imfcaptureengine.htm
tech.root: mf
ms.assetid: 4A2A0536-4255-40AB-BCAB-228B09343583
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngine, IMFCaptureEngine interface [Media Foundation], IMFCaptureEngine interface [Media Foundation],described, mf.imfcaptureengine, mfcaptureengine/IMFCaptureEngine
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
 - IMFCaptureEngine
 - mfcaptureengine/IMFCaptureEngine
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
 - IMFCaptureEngine
---

# IMFCaptureEngine interface


## -description

Controls one or more capture devices. The capture engine implements this interface. To get a pointer to this interface, call either <a href="/windows/desktop/medfound/mfcreatecaptureengine">MFCreateCaptureEngine</a> or <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineclassfactory-createinstance">IMFCaptureEngineClassFactory::CreateInstance</a>.

## -inheritance

The <b>IMFCaptureEngine</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureEngine</b> also has these types of members:

## -remarks

<b>IMFCaptureEngine</b> only supports one pass CBR encoding.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
