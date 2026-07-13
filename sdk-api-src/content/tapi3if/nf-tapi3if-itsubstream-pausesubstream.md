---
UID: NF:tapi3if.ITSubStream.PauseSubStream
title: ITSubStream::PauseSubStream (tapi3if.h)
description: The PauseSubStream method pauses the substream.
helpviewer_keywords: ["ITSubStream interface [TAPI 2.2]","PauseSubStream method","ITSubStream.PauseSubStream","ITSubStream::PauseSubStream","PauseSubStream","PauseSubStream method [TAPI 2.2]","PauseSubStream method [TAPI 2.2]","ITSubStream interface","_tapi3_itsubstream_pausesubstream","tapi3.itsubstream_pausesubstream","tapi3if/ITSubStream::PauseSubStream"]
old-location: tapi3\itsubstream_pausesubstream.htm
tech.root: tapi3
ms.assetid: 77bd3726-3996-45a6-88be-cb033f5dddc0
ms.date: 12/05/2018
ms.keywords: ITSubStream interface [TAPI 2.2],PauseSubStream method, ITSubStream.PauseSubStream, ITSubStream::PauseSubStream, PauseSubStream, PauseSubStream method [TAPI 2.2], PauseSubStream method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_pausesubstream, tapi3.itsubstream_pausesubstream, tapi3if/ITSubStream::PauseSubStream
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
 - ITSubStream::PauseSubStream
 - tapi3if/ITSubStream::PauseSubStream
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
 - ITSubStream.PauseSubStream
---

# ITSubStream::PauseSubStream


## -description

The 
<b>PauseSubStream</b> method pauses the substream.



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
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This operation is not supported.

</td>
</tr>
</table>

## -remarks

The difference between pausing and stopping a stream depends on the type of transport.

If the substream pauses successfully, the application receives a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event">CALL_MEDIA_EVENT</a> with a value of CME_STREAM_INACTIVE and 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event_cause">CALL_MEDIA_EVENT_CAUSE</a> equaling CMC_LOCAL_REQUEST.

If the substream fails to pause, the event will be CME_STREAM_FAIL with cause CMC_LOCAL_REQUEST.

A call to 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-startsubstream">StartSubStream</a> restarts the substream.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
