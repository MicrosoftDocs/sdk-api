---
UID: NF:mfidl.IMFMediaSource.Pause
title: IMFMediaSource::Pause (mfidl.h)
description: Pauses all active streams in the media source.
helpviewer_keywords: ["113b3dc7-918e-427e-aa70-cf474b951c6d","IMFMediaSource interface [Media Foundation]","Pause method","IMFMediaSource.Pause","IMFMediaSource::Pause","Pause","Pause method [Media Foundation]","Pause method [Media Foundation]","IMFMediaSource interface","mf.imfmediasource_pause","mfidl/IMFMediaSource::Pause"]
old-location: mf\imfmediasource_pause.htm
tech.root: mf
ms.assetid: 113b3dc7-918e-427e-aa70-cf474b951c6d
ms.date: 12/05/2018
ms.keywords: 113b3dc7-918e-427e-aa70-cf474b951c6d, IMFMediaSource interface [Media Foundation],Pause method, IMFMediaSource.Pause, IMFMediaSource::Pause, Pause, Pause method [Media Foundation], Pause method [Media Foundation],IMFMediaSource interface, mf.imfmediasource_pause, mfidl/IMFMediaSource::Pause
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
 - IMFMediaSource::Pause
 - mfidl/IMFMediaSource::Pause
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
 - IMFMediaSource.Pause
---

# IMFMediaSource::Pause


## -description

Pauses all active streams in the media source.



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
<dt><b>MF_E_INVALID_STATE_TRANSITION</b></dt>
</dl>
</td>
<td width="60%">
Invalid state transition. The media source must be in the started state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media source's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">Shutdown</a> method has been called.

</td>
</tr>
</table>

## -remarks

This method is asynchronous. When the operation completes, the media source sends and <a href="/windows/desktop/medfound/mesourcepaused">MESourcePaused</a> event, and every active stream sends an <a href="/windows/desktop/medfound/mestreampaused">MEStreamPaused</a> event. If the method returns a failure code, no events are raised.

The media source must be in the started state. The method fails if the media source is paused or stopped.

While the source is paused, calls to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample">IMFMediaStream::RequestSample</a> succeed, but the streams will not deliver any samples until after the source is started again. Note that the source's event queue is not serialized with the stream event queues, so the client might receive some samples after the <a href="/windows/desktop/medfound/mesourcepaused">MESourcePaused</a> event, due to multi-threading issues. But the client will not receive any samples from a stream after the <a href="/windows/desktop/medfound/mestreampaused">MEStreamPaused</a> event.

Not every media source can pause. If a media source can pause, the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics">IMFMediaSource::GetCharacteristics</a> method returns the MFMEDIASOURCE_CAN_PAUSE flag.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>



<a href="/windows/desktop/medfound/media-sources">Media Sources</a>
