---
UID: NF:tapi3if.ITStream.PauseStream
title: ITStream::PauseStream
author: windows-sdk-content
description: The PauseStream method pauses the stream.
old-location: tapi3\itstream_pausestream.htm
tech.root: Tapi
ms.assetid: d7d70dd9-dcac-4b25-9954-10b4d6b436de
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITStream interface [TAPI 2.2],PauseStream method, ITStream.PauseStream, ITStream::PauseStream, PauseStream, PauseStream method [TAPI 2.2], PauseStream method [TAPI 2.2],ITStream interface, _tapi3_itstream_pausestream, tapi3.itstream_pausestream, tapi3if/ITStream::PauseStream
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITStream.PauseStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITStream::PauseStream


## -description


The 
<b>PauseStream</b> method pauses the stream.


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
</table>
 




## -remarks



The difference between pausing and stopping a stream depends on the type of transport.

If the stream pauses successfully, the MSP should fire 
<a href="https://msdn.microsoft.com/835759f4-652b-4d01-911a-e580bb29d292">CALL_MEDIA_EVENT</a> with a value of CME_STREAM_INACTIVE and 
<a href="https://msdn.microsoft.com/c43e0a72-decc-47e3-bd5e-d94a95a2e404">CALL_MEDIA_EVENT_CAUSE</a> equaling CMC_LOCAL_REQUEST.

If the stream fails to pause, the event will be CME_STREAM_FAIL with cause CMC_LOCAL_REQUEST.

A call to 
<a href="https://msdn.microsoft.com/23553f00-5ce5-465e-b455-8bf2d73dae9d">StartStream</a> restarts the stream.




## -see-also




<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

