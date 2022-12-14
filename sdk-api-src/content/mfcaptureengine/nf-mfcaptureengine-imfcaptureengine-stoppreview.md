---
UID: NF:mfcaptureengine.IMFCaptureEngine.StopPreview
title: IMFCaptureEngine::StopPreview (mfcaptureengine.h)
description: Stops preview.
helpviewer_keywords: ["IMFCaptureEngine interface [Media Foundation]","StopPreview method","IMFCaptureEngine.StopPreview","IMFCaptureEngine::StopPreview","StopPreview","StopPreview method [Media Foundation]","StopPreview method [Media Foundation]","IMFCaptureEngine interface","mf.imfcaptureengine_stoppreview","mfcaptureengine/IMFCaptureEngine::StopPreview"]
old-location: mf\imfcaptureengine_stoppreview.htm
tech.root: mf
ms.assetid: 36DE5079-D4D5-4FC5-8CF6-1F5B3F9E8B66
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],StopPreview method, IMFCaptureEngine.StopPreview, IMFCaptureEngine::StopPreview, StopPreview, StopPreview method [Media Foundation], StopPreview method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_stoppreview, mfcaptureengine/IMFCaptureEngine::StopPreview
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
 - IMFCaptureEngine::StopPreview
 - mfcaptureengine/IMFCaptureEngine::StopPreview
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
 - IMFCaptureEngine.StopPreview
---

# IMFCaptureEngine::StopPreview


## -description

Stops preview.



## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The capture engine is not currently previewing.

</td>
</tr>
</table>

## -remarks

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_PREVIEW_STOPPED</b> event through the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine">IMFCaptureEngine</a>
