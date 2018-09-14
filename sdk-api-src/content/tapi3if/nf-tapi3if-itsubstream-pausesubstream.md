---
UID: NF:tapi3if.ITSubStream.PauseSubStream
title: ITSubStream::PauseSubStream
author: windows-sdk-content
description: The PauseSubStream method pauses the substream.
old-location: tapi3\itsubstream_pausesubstream.htm
tech.root: TAPI
ms.assetid: 77bd3726-3996-45a6-88be-cb033f5dddc0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITSubStream interface [TAPI 2.2],PauseSubStream method, ITSubStream.PauseSubStream, ITSubStream::PauseSubStream, PauseSubStream, PauseSubStream method [TAPI 2.2], PauseSubStream method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_pausesubstream, tapi3.itsubstream_pausesubstream, tapi3if/ITSubStream::PauseSubStream
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
 - ITSubStream.PauseSubStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSubStream::PauseSubStream


## -description


The 
<b>PauseSubStream</b> method pauses the substream.


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
<a href="https://msdn.microsoft.com/835759f4-652b-4d01-911a-e580bb29d292">CALL_MEDIA_EVENT</a> with a value of CME_STREAM_INACTIVE and 
<a href="https://msdn.microsoft.com/c43e0a72-decc-47e3-bd5e-d94a95a2e404">CALL_MEDIA_EVENT_CAUSE</a> equaling CMC_LOCAL_REQUEST.

If the substream fails to pause, the event will be CME_STREAM_FAIL with cause CMC_LOCAL_REQUEST.

A call to 
<a href="https://msdn.microsoft.com/603cb667-a108-4e47-9808-99fddad5d894">StartSubStream</a> restarts the substream.




## -see-also




<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

