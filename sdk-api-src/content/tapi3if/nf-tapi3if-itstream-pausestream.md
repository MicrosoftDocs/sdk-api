---
UID: NF:tapi3if.ITStream.PauseStream
title: ITStream::PauseStream (tapi3if.h)
description: The PauseStream method pauses the stream.
helpviewer_keywords: ["ITStream interface [TAPI 2.2]","PauseStream method","ITStream.PauseStream","ITStream::PauseStream","PauseStream","PauseStream method [TAPI 2.2]","PauseStream method [TAPI 2.2]","ITStream interface","_tapi3_itstream_pausestream","tapi3.itstream_pausestream","tapi3if/ITStream::PauseStream"]
old-location: tapi3\itstream_pausestream.htm
tech.root: tapi3
ms.assetid: d7d70dd9-dcac-4b25-9954-10b4d6b436de
ms.date: 12/05/2018
ms.keywords: ITStream interface [TAPI 2.2],PauseStream method, ITStream.PauseStream, ITStream::PauseStream, PauseStream, PauseStream method [TAPI 2.2], PauseStream method [TAPI 2.2],ITStream interface, _tapi3_itstream_pausestream, tapi3.itstream_pausestream, tapi3if/ITStream::PauseStream
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
 - ITStream::PauseStream
 - tapi3if/ITStream::PauseStream
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
 - ITStream.PauseStream
---

# ITStream::PauseStream


## -description

The 
<b>PauseStream</b> method pauses the stream.



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
</table>

## -remarks

The difference between pausing and stopping a stream depends on the type of transport.

If the stream pauses successfully, the MSP should fire 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event">CALL_MEDIA_EVENT</a> with a value of CME_STREAM_INACTIVE and 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event_cause">CALL_MEDIA_EVENT_CAUSE</a> equaling CMC_LOCAL_REQUEST.

If the stream fails to pause, the event will be CME_STREAM_FAIL with cause CMC_LOCAL_REQUEST.

A call to 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">StartStream</a> restarts the stream.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
