---
UID: NF:tapi3if.ITStream.StartStream
title: ITStream::StartStream (tapi3if.h)
description: The StartStream method starts the stream.
helpviewer_keywords: ["ITStream interface [TAPI 2.2]","StartStream method","ITStream.StartStream","ITStream::StartStream","StartStream","StartStream method [TAPI 2.2]","StartStream method [TAPI 2.2]","ITStream interface","_tapi3_itstream_startstream","tapi3.itstream_startstream","tapi3if/ITStream::StartStream"]
old-location: tapi3\itstream_startstream.htm
tech.root: tapi3
ms.assetid: 23553f00-5ce5-465e-b455-8bf2d73dae9d
ms.date: 12/05/2018
ms.keywords: ITStream interface [TAPI 2.2],StartStream method, ITStream.StartStream, ITStream::StartStream, StartStream, StartStream method [TAPI 2.2], StartStream method [TAPI 2.2],ITStream interface, _tapi3_itstream_startstream, tapi3.itstream_startstream, tapi3if/ITStream::StartStream
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ITStream::StartStream
 - tapi3if/ITStream::StartStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITStream.StartStream
---

# ITStream::StartStream


## -description

The 
<b>StartStream</b> method starts the stream.



## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTERMINALSELECTED</b></dt>
</dl>
</td>
<td width="60%">
No terminal has been selected on the stream, so it cannot be started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSTOPPED</b></dt>
</dl>
</td>
<td width="60%">
Stream has already been started.

</td>
</tr>
</table>

## -remarks

Streams start automatically as soon as a call is connected and ready to stream and a terminal is selected. Therefore, most applications do not need to call this method. Applications have to call this method only to start a stream that the application has previously stopped or paused by calling 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-pausestream">ITStream::PauseStream</a>.

This call generates events that the application can retrieve if it has registered. Please see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview for information on receiving events.

If the stream starts successfully, the MSP fires a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event">CALL_MEDIA_EVENT</a> with a value of CME_STREAM_ACTIVE event and 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event_cause">CALL_MEDIA_EVENT_CAUSE</a> equaling CMC_LOCAL_REQUEST.

If the stream fails to pause, the MSP fires a CME_STREAM_FAIL event with cause CMC_LOCAL_REQUEST.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
