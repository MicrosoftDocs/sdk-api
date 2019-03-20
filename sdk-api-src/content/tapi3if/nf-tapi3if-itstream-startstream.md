---
UID: NF:tapi3if.ITStream.StartStream
title: ITStream::StartStream (tapi3if.h)
author: windows-sdk-content
description: The StartStream method starts the stream.
old-location: tapi3\itstream_startstream.htm
tech.root: Tapi
ms.assetid: 23553f00-5ce5-465e-b455-8bf2d73dae9d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITStream interface [TAPI 2.2],StartStream method, ITStream.StartStream, ITStream::StartStream, StartStream, StartStream method [TAPI 2.2], StartStream method [TAPI 2.2],ITStream interface, _tapi3_itstream_startstream, tapi3.itstream_startstream, tapi3if/ITStream::StartStream
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITStream.StartStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITStream::StartStream


## -description


The 
<b>StartStream</b> method starts the stream.


## -parameters






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
<a href="https://msdn.microsoft.com/6014e76e-ce2c-4ab8-b6f2-c09fc2acf315">ITStream::StopStream</a> or 
<a href="https://msdn.microsoft.com/d7d70dd9-dcac-4b25-9954-10b4d6b436de">ITStream::PauseStream</a>.

This call generates events that the application can retrieve if it has registered. Please see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview for information on receiving events.

If the stream starts successfully, the MSP fires a 
<a href="https://msdn.microsoft.com/835759f4-652b-4d01-911a-e580bb29d292">CALL_MEDIA_EVENT</a> with a value of CME_STREAM_ACTIVE event and 
<a href="https://msdn.microsoft.com/c43e0a72-decc-47e3-bd5e-d94a95a2e404">CALL_MEDIA_EVENT_CAUSE</a> equaling CMC_LOCAL_REQUEST.

If the stream fails to pause, the MSP fires a CME_STREAM_FAIL event with cause CMC_LOCAL_REQUEST.




## -see-also




<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

