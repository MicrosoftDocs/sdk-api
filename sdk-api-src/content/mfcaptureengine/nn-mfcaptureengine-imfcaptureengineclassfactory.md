---
UID: NN:mfcaptureengine.IMFCaptureEngineClassFactory
title: IMFCaptureEngineClassFactory (mfcaptureengine.h)
description: Creates an instance of the capture engine. (IMFCaptureEngineClassFactory)
helpviewer_keywords: ["IMFCaptureEngineClassFactory","IMFCaptureEngineClassFactory interface [Media Foundation]","IMFCaptureEngineClassFactory interface [Media Foundation]","described","mf.imfcaptureengineclassfactory","mfcaptureengine/IMFCaptureEngineClassFactory"]
old-location: mf\imfcaptureengineclassfactory.htm
tech.root: mf
ms.assetid: FAFA52AD-B96E-4ADC-BE79-3BE5F1ACC92A
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngineClassFactory, IMFCaptureEngineClassFactory interface [Media Foundation], IMFCaptureEngineClassFactory interface [Media Foundation],described, mf.imfcaptureengineclassfactory, mfcaptureengine/IMFCaptureEngineClassFactory
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
 - IMFCaptureEngineClassFactory
 - mfcaptureengine/IMFCaptureEngineClassFactory
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
 - IMFCaptureEngineClassFactory
---

# IMFCaptureEngineClassFactory interface


## -description

Creates an instance of the capture engine.

## -inheritance

The <b>IMFCaptureEngineClassFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureEngineClassFactory</b> also has these types of members:

## -remarks

To get a pointer to this interface, call the <a href="/windows/desktop/medfound/using-an-encoder-s-imftransform--interface">CoCreateInstance</a> function and specify the CLSID equal to <b>CLSID_MFCaptureEngineClassFactory</b>. 

Calling the <a href="/windows/desktop/medfound/mfcreatecaptureengine">MFCreateCaptureEngine</a> function is equivalent to calling <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineclassfactory-createinstance">IMFCaptureEngineClassFactory::CreateInstance</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
