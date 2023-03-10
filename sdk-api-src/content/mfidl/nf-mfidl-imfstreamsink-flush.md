---
UID: NF:mfidl.IMFStreamSink.Flush
title: IMFStreamSink::Flush (mfidl.h)
description: Causes the stream sink to drop any samples that it has received and has not rendered yet.
helpviewer_keywords: ["514d29bd-571d-46b1-9948-5d623c6703aa","Flush","Flush method [Media Foundation]","Flush method [Media Foundation]","IMFStreamSink interface","IMFStreamSink interface [Media Foundation]","Flush method","IMFStreamSink.Flush","IMFStreamSink::Flush","mf.imfstreamsink_flush","mfidl/IMFStreamSink::Flush"]
old-location: mf\imfstreamsink_flush.htm
tech.root: mf
ms.assetid: 514d29bd-571d-46b1-9948-5d623c6703aa
ms.date: 12/05/2018
ms.keywords: 514d29bd-571d-46b1-9948-5d623c6703aa, Flush, Flush method [Media Foundation], Flush method [Media Foundation],IMFStreamSink interface, IMFStreamSink interface [Media Foundation],Flush method, IMFStreamSink.Flush, IMFStreamSink::Flush, mf.imfstreamsink_flush, mfidl/IMFStreamSink::Flush
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFStreamSink::Flush
 - mfidl/IMFStreamSink::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFStreamSink.Flush
---

# IMFStreamSink::Flush


## -description

Causes the stream sink to drop any samples that it has received and has not rendered yet.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The stream sink has not been initialized yet. You might need to set a media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">Shutdown</a> method has been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINK_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
This stream was removed from the media sink and is no longer valid.

</td>
</tr>
</table>

## -remarks

If any samples are still queued from previous calls to the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample">IMFStreamSink::ProcessSample</a> method, the media sink immediately discards them, without processing them. This can cause a glitch in the rendered output. The running state of the sink (running, paused, or stopped) does not change.

Any pending marker events from the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker">IMFStreamSink::PlaceMarker</a> method are dispatched immediately, with the status code E_ABORT.

This method is synchronous. It does not return until the sink has discarded all pending samples.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>
