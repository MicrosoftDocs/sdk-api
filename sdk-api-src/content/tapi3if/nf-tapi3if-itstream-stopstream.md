---
UID: NF:tapi3if.ITStream.StopStream
title: ITStream::StopStream
author: windows-sdk-content
description: The StopStream method stops the stream.
old-location: tapi3\itstream_stopstream.htm
old-project: tapi
ms.assetid: 6014e76e-ce2c-4ab8-b6f2-c09fc2acf315
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITStream interface [TAPI 2.2],StopStream method, ITStream.StopStream, ITStream::StopStream, StopStream, StopStream method [TAPI 2.2], StopStream method [TAPI 2.2],ITStream interface, _tapi3_itstream_stopstream, tapi3.itstream_stopstream, tapi3if/ITStream::StopStream
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITStream.StopStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITStream::StopStream


## -description


The 
<b>StopStream</b> method stops the stream.


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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a> overview for information on receiving events.

If the stream stops successfully, the application receives a 
<a href="https://msdn.microsoft.com/835759f4-652b-4d01-911a-e580bb29d292">CALL_MEDIA_EVENT</a> with a value of CME_STREAM_INACTIVE event and 
<a href="https://msdn.microsoft.com/c43e0a72-decc-47e3-bd5e-d94a95a2e404">CALL_MEDIA_EVENT_CAUSE</a> equaling CMC_LOCAL_REQUEST.

If the stream fails to pause, the application receives a CME_STREAM_FAIL event with cause CMC_LOCAL_REQUEST.

To subsequently restart the stream, the application must call 
<a href="https://msdn.microsoft.com/23553f00-5ce5-465e-b455-8bf2d73dae9d">StartStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

