---
UID: NF:mfidl.IMFMediaSource.Stop
title: IMFMediaSource::Stop (mfidl.h)
description: Stops all active streams in the media source.
helpviewer_keywords: ["IMFMediaSource interface [Media Foundation]","Stop method","IMFMediaSource.Stop","IMFMediaSource::Stop","Stop","Stop method [Media Foundation]","Stop method [Media Foundation]","IMFMediaSource interface","aa7af7a0-a6c2-4c9e-9f98-d36716679297","mf.imfmediasource_stop","mfidl/IMFMediaSource::Stop"]
old-location: mf\imfmediasource_stop.htm
tech.root: mf
ms.assetid: aa7af7a0-a6c2-4c9e-9f98-d36716679297
ms.date: 12/05/2018
ms.keywords: IMFMediaSource interface [Media Foundation],Stop method, IMFMediaSource.Stop, IMFMediaSource::Stop, Stop, Stop method [Media Foundation], Stop method [Media Foundation],IMFMediaSource interface, aa7af7a0-a6c2-4c9e-9f98-d36716679297, mf.imfmediasource_stop, mfidl/IMFMediaSource::Stop
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
 - IMFMediaSource::Stop
 - mfidl/IMFMediaSource::Stop
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
 - IMFMediaSource.Stop
---

# IMFMediaSource::Stop


## -description

Stops all active streams in the media source.



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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media source's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">Shutdown</a> method has been called.

</td>
</tr>
</table>

## -remarks

This method is asynchronous. When the operation completes, the media source sends and <a href="/windows/desktop/medfound/mesourcestopped">MESourceStopped</a> event, and every active stream sends an <a href="/windows/desktop/medfound/mestreamstopped">MEStreamStopped</a> event. If the method returns a failure code, no events are raised.

When a media source is stopped, its current position reverts to zero. After that, if the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start">Start</a> method is called with VT_EMPTY for the starting position, playback starts from the beginning of the presentation.

While the source is stopped, no streams produce data.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>



<a href="/windows/desktop/medfound/media-sources">Media Sources</a>
