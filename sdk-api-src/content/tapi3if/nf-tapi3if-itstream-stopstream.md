---
UID: NF:tapi3if.ITStream.StopStream
title: ITStream::StopStream (tapi3if.h)
description: The StopStream method stops the stream.
helpviewer_keywords: ["ITStream interface [TAPI 2.2]","StopStream method","ITStream.StopStream","ITStream::StopStream","StopStream","StopStream method [TAPI 2.2]","StopStream method [TAPI 2.2]","ITStream interface","_tapi3_itstream_stopstream","tapi3.itstream_stopstream","tapi3if/ITStream::StopStream"]
old-location: tapi3\itstream_stopstream.htm
tech.root: tapi3
ms.assetid: 6014e76e-ce2c-4ab8-b6f2-c09fc2acf315
ms.date: 12/05/2018
ms.keywords: ITStream interface [TAPI 2.2],StopStream method, ITStream.StopStream, ITStream::StopStream, StopStream, StopStream method [TAPI 2.2], StopStream method [TAPI 2.2],ITStream interface, _tapi3_itstream_stopstream, tapi3.itstream_stopstream, tapi3if/ITStream::StopStream
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
 - ITStream::StopStream
 - tapi3if/ITStream::StopStream
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
 - ITStream.StopStream
---

# ITStream::StopStream


## -description

The 
<b>StopStream</b> method stops the stream.



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
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The provider does not support this operation.

</td>
</tr>
</table>

## -remarks

An application can call this method to stop a stream. The difference between pausing a stream and stopping a stream depends on the type of transport used for the call.

This call generates events that the application can retrieve if it has registered. Please see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview for information on receiving events.

If the stream stops successfully, the application receives a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event">CALL_MEDIA_EVENT</a> with a value of CME_STREAM_INACTIVE event and 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event_cause">CALL_MEDIA_EVENT_CAUSE</a> equaling CMC_LOCAL_REQUEST.

If the stream fails to pause, the application receives a CME_STREAM_FAIL event with cause CMC_LOCAL_REQUEST.

To subsequently restart the stream, the application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">StartStream</a>.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
