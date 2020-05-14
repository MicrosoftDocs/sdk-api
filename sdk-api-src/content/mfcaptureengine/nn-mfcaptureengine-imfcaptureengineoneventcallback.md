---
UID: NN:mfcaptureengine.IMFCaptureEngineOnEventCallback
title: IMFCaptureEngineOnEventCallback (mfcaptureengine.h)
description: Callback interface for receiving events from the capture engine.helpviewer_keywords: ["IMFCaptureEngineOnEventCallback","IMFCaptureEngineOnEventCallback interface [Media Foundation]","IMFCaptureEngineOnEventCallback interface [Media Foundation]","described","mf.imfcaptureengineoneventcallback","mfcaptureengine/IMFCaptureEngineOnEventCallback"]
old-location: mf\imfcaptureengineoneventcallback.htm
tech.root: medfound
ms.assetid: 6F04F843-160C-4F49-9841-ECC1450F4A58
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngineOnEventCallback, IMFCaptureEngineOnEventCallback interface [Media Foundation], IMFCaptureEngineOnEventCallback interface [Media Foundation],described, mf.imfcaptureengineoneventcallback, mfcaptureengine/IMFCaptureEngineOnEventCallback
f1_keywords:
- mfcaptureengine/IMFCaptureEngineOnEventCallback
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
- IMFCaptureEngineOnEventCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCaptureEngineOnEventCallback interface


## -description


Callback interface for receiving events from the capture engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureEngineOnEventCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCaptureEngineOnEventCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureEngineOnEventCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent">OnEvent</a>
</td>
<td align="left" width="63%">
Called by the capture engine to notify the application of a capture event.

</td>
</tr>
</table> 


## -remarks



To set the callback interface on the capture engine, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize">IMFCaptureEngine::Initialize</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

