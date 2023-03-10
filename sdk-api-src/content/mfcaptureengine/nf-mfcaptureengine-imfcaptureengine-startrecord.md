---
UID: NF:mfcaptureengine.IMFCaptureEngine.StartRecord
title: IMFCaptureEngine::StartRecord (mfcaptureengine.h)
description: Starts recording audio and/or video to a file.
helpviewer_keywords: ["IMFCaptureEngine interface [Media Foundation]","StartRecord method","IMFCaptureEngine.StartRecord","IMFCaptureEngine::StartRecord","StartRecord","StartRecord method [Media Foundation]","StartRecord method [Media Foundation]","IMFCaptureEngine interface","mf.imfcaptureengine_startrecord","mfcaptureengine/IMFCaptureEngine::StartRecord"]
old-location: mf\imfcaptureengine_startrecord.htm
tech.root: mf
ms.assetid: 22084409-B2E6-47EF-A59B-A762E9A9191D
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],StartRecord method, IMFCaptureEngine.StartRecord, IMFCaptureEngine::StartRecord, StartRecord, StartRecord method [Media Foundation], StartRecord method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_startrecord, mfcaptureengine/IMFCaptureEngine::StartRecord
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
 - IMFCaptureEngine::StartRecord
 - mfcaptureengine/IMFCaptureEngine::StartRecord
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
 - IMFCaptureEngine.StartRecord
---

# IMFCaptureEngine::StartRecord


## -description

Starts recording audio and/or video to a file.



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
The recording sink was not initialized.

</td>
</tr>
</table>

## -remarks

Before calling this method, configure the recording sink by calling <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">IMFCaptureSink::AddStream</a>. To get a pointer to the recording sink, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-getsink">IMFCaptureEngine::GetSink</a>.

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_RECORD_STARTED</b> event through the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.

To stop recording, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-stoprecord">IMFCaptureEngine::StopRecord</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine">IMFCaptureEngine</a>
