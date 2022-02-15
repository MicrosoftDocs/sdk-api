---
UID: NF:mfcaptureengine.IMFCaptureSink.Prepare
title: IMFCaptureSink::Prepare (mfcaptureengine.h)
description: Prepares the capture sink by loading any required pipeline components, such as encoders, video processors, and media sinks.
helpviewer_keywords: ["IMFCaptureSink interface [Media Foundation]","Prepare method","IMFCaptureSink.Prepare","IMFCaptureSink::Prepare","Prepare","Prepare method [Media Foundation]","Prepare method [Media Foundation]","IMFCaptureSink interface","mf.imfcapturesink_prepare","mfcaptureengine/IMFCaptureSink::Prepare"]
old-location: mf\imfcapturesink_prepare.htm
tech.root: mf
ms.assetid: 244FD291-AD1D-4A51-87C3-C98B33978AA1
ms.date: 12/05/2018
ms.keywords: IMFCaptureSink interface [Media Foundation],Prepare method, IMFCaptureSink.Prepare, IMFCaptureSink::Prepare, Prepare, Prepare method [Media Foundation], Prepare method [Media Foundation],IMFCaptureSink interface, mf.imfcapturesink_prepare, mfcaptureengine/IMFCaptureSink::Prepare
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
 - IMFCaptureSink::Prepare
 - mfcaptureengine/IMFCaptureSink::Prepare
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
 - IMFCaptureSink.Prepare
---

# IMFCaptureSink::Prepare


## -description

Prepares the capture sink by loading any required pipeline components, such as encoders, video processors, and media sinks.



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
Invalid request.

</td>
</tr>
</table>

## -remarks

Calling this method is optional. This method gives the application an opportunity to configure the pipeline components before they are used. The method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_SINK_PREPARED</b> event through the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent">IMFCaptureEngineOnEventCallback::OnEvent</a> method.  After this event is received, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-getservice">IMFCaptureSink::GetService</a> to configure individual components.

Before calling this method, configure the capture sink by adding at least one stream. To add a stream, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">IMFCaptureSink::AddStream</a>.

The <b>Prepare</b> method fails if the capture sink is currently in use. For example, calling <b>Prepare</b> on the preview sink fails if the capture engine is currently previewing.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>
