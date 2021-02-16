---
UID: NF:mfcaptureengine.IMFCaptureEngine.GetSink
title: IMFCaptureEngine::GetSink (mfcaptureengine.h)
description: Gets a pointer to one of the capture sink objects.
helpviewer_keywords: ["GetSink","GetSink method [Media Foundation]","GetSink method [Media Foundation]","IMFCaptureEngine interface","IMFCaptureEngine interface [Media Foundation]","GetSink method","IMFCaptureEngine.GetSink","IMFCaptureEngine::GetSink","mf.imfcaptureengine_getsink","mfcaptureengine/IMFCaptureEngine::GetSink"]
old-location: mf\imfcaptureengine_getsink.htm
tech.root: mf
ms.assetid: 7DAF5EA3-BA65-4CF9-B7BA-B427A48BF3BC
ms.date: 12/05/2018
ms.keywords: GetSink, GetSink method [Media Foundation], GetSink method [Media Foundation],IMFCaptureEngine interface, IMFCaptureEngine interface [Media Foundation],GetSink method, IMFCaptureEngine.GetSink, IMFCaptureEngine::GetSink, mf.imfcaptureengine_getsink, mfcaptureengine/IMFCaptureEngine::GetSink
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
 - IMFCaptureEngine::GetSink
 - mfcaptureengine/IMFCaptureEngine::GetSink
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
 - IMFCaptureEngine.GetSink
---

# IMFCaptureEngine::GetSink


## -description

Gets a pointer to one of the capture sink objects. You can use the capture sinks to configure preview, recording, or still-image capture.

## -parameters

### -param mfCaptureEngineSinkType [in]

An <a href="/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type">MF_CAPTURE_ENGINE_SINK_TYPE</a> value that specifies the capture sink to retrieve.

### -param ppSink [out]

Receives a pointer to the <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a> interface. The caller must release the interface.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine">IMFCaptureEngine</a>