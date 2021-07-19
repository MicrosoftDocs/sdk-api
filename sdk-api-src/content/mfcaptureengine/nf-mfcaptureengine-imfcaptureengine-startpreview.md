---
UID: NF:mfcaptureengine.IMFCaptureEngine.StartPreview
title: IMFCaptureEngine::StartPreview (mfcaptureengine.h)
description: Starts preview.
helpviewer_keywords: ["IMFCaptureEngine interface [Media Foundation]","StartPreview method","IMFCaptureEngine.StartPreview","IMFCaptureEngine::StartPreview","StartPreview","StartPreview method [Media Foundation]","StartPreview method [Media Foundation]","IMFCaptureEngine interface","mf.imfcaptureengine_startpreview","mfcaptureengine/IMFCaptureEngine::StartPreview"]
old-location: mf\imfcaptureengine_startpreview.htm
tech.root: mf
ms.assetid: C5BCF990-E7F9-48E9-B082-79953F5ED27C
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],StartPreview method, IMFCaptureEngine.StartPreview, IMFCaptureEngine::StartPreview, StartPreview, StartPreview method [Media Foundation], StartPreview method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_startpreview, mfcaptureengine/IMFCaptureEngine::StartPreview
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
 - IMFCaptureEngine::StartPreview
 - mfcaptureengine/IMFCaptureEngine::StartPreview
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
 - IMFCaptureEngine.StartPreview
---

# IMFCaptureEngine::StartPreview


## -description

Starts preview.



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
The preview sink was not initialized.

</td>
</tr>
</table>

## -remarks

Before calling this method, configure the preview sink by calling <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">IMFCaptureSink::AddStream</a>. To get a pointer to the preview sink, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-getsink">IMFCaptureEngine::GetSink</a>. 

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_PREVIEW_STARTED</b> event through the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.

After the preview sink is configured, you can stop and start preview by calling <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-stoppreview">IMFCaptureEngine::StopPreview</a> and <b>IMFCaptureEngine::StartPreview</b>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine">IMFCaptureEngine</a>
