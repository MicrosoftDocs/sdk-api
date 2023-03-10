---
UID: NN:mfmediaengine.IMFMediaEngineClassFactory
title: IMFMediaEngineClassFactory (mfmediaengine.h)
description: Creates an instance of the Media Engine.
helpviewer_keywords: ["IMFMediaEngineClassFactory","IMFMediaEngineClassFactory interface [Media Foundation]","IMFMediaEngineClassFactory interface [Media Foundation]","described","mf.imfmediaengineclassfactory","mfmediaengine/IMFMediaEngineClassFactory"]
old-location: mf\imfmediaengineclassfactory.htm
tech.root: mf
ms.assetid: 8E4E84A0-BCFC-4CBF-813B-4FEE2B42A83E
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineClassFactory, IMFMediaEngineClassFactory interface [Media Foundation], IMFMediaEngineClassFactory interface [Media Foundation],described, mf.imfmediaengineclassfactory, mfmediaengine/IMFMediaEngineClassFactory
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineClassFactory
 - mfmediaengine/IMFMediaEngineClassFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineClassFactory
---

# IMFMediaEngineClassFactory interface


## -description

Creates an instance of the Media Engine.

## -inheritance

The <b>IMFMediaEngineClassFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineClassFactory</b> also has these types of members:

## -remarks

Before using this interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> and <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a>.

To get a pointer to this interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. The class identifier is <b>CLSID_MFMediaEngineClassFactory</b>.

## -see-also

<a href="https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Media%20engine%20native%20C%2B%2B%20video%20playback%20sample%20(Windows%208)">Media Engine Sample</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
