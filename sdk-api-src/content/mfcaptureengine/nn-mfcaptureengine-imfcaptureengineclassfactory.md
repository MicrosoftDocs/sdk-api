---
UID: NN:mfcaptureengine.IMFCaptureEngineClassFactory
title: IMFCaptureEngineClassFactory (mfcaptureengine.h)
description: Creates an instance of the capture engine.
helpviewer_keywords: ["IMFCaptureEngineClassFactory","IMFCaptureEngineClassFactory interface [Media Foundation]","IMFCaptureEngineClassFactory interface [Media Foundation]","described","mf.imfcaptureengineclassfactory","mfcaptureengine/IMFCaptureEngineClassFactory"]
old-location: mf\imfcaptureengineclassfactory.htm
tech.root: medfound
ms.assetid: FAFA52AD-B96E-4ADC-BE79-3BE5F1ACC92A
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngineClassFactory, IMFCaptureEngineClassFactory interface [Media Foundation], IMFCaptureEngineClassFactory interface [Media Foundation],described, mf.imfcaptureengineclassfactory, mfcaptureengine/IMFCaptureEngineClassFactory
f1_keywords:
- mfcaptureengine/IMFCaptureEngineClassFactory
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
- IMFCaptureEngineClassFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCaptureEngineClassFactory interface


## -description


Creates an instance of the capture engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureEngineClassFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureEngineClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureEngineClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineclassfactory-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an instance of the capture engine.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call the <a href="https://docs.microsoft.com/windows/desktop/medfound/using-an-encoder-s-imftransform--interface">CoCreateInstance</a> function and specify the CLSID equal to <b>CLSID_MFCaptureEngineClassFactory</b>. 

Calling the <a href="https://docs.microsoft.com/windows/desktop/medfound/mfcreatecaptureengine">MFCreateCaptureEngine</a> function is equivalent to calling <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineclassfactory-createinstance">IMFCaptureEngineClassFactory::CreateInstance</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

