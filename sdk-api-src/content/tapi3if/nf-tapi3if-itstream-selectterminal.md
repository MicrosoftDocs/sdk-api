---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITStream::SelectTerminal


## -description


The 
<b>SelectTerminal</b> method selects an 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> object onto the stream.


## -parameters




### -param pTerminal [in]

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface of selected terminal.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTerminal</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_MAXTERMINALS</b></dt>
</dl>
</td>
<td width="60%">
Multiple terminals have been selected on the stream, but media mixing or splitting is not possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALIDTERMINAL</b></dt>
</dl>
</td>
<td width="60%">
The terminal selected is not valid.

</td>
</tr>
</table>
 




## -remarks



Terminals can be selected at any time, irrespective of whether the transport is in a state that allows it to stream media. If the transport is in a state that allows it to stream media, and the application has not successfully invoked 
<a href="https://msdn.microsoft.com/d7d70dd9-dcac-4b25-9954-10b4d6b436de">ITStream::PauseStream</a> or 
<a href="https://msdn.microsoft.com/6014e76e-ce2c-4ab8-b6f2-c09fc2acf315">ITStream::StopStream</a> on the stream, or has successfully invoked 
<a href="https://msdn.microsoft.com/23553f00-5ce5-465e-b455-8bf2d73dae9d">ITStream::StartStream</a> for this stream more recently than it has successfully invoked <b>ITStream::PauseStream</b> or <b>ITStream::StopStream</b> for this stream, then streaming starts automatically as soon as the terminal is selected. If a terminal is selected on the stream before the transport enters a state in which it can stream media, and no subsequent calls to 
<b>StopStream</b> or 
<b>PauseStream</b> are made, then the stream starts automatically when the transport enters a state in which it can stream media.

The CME_STREAM_ACTIVE event is generated when streaming actually starts, which may be later than the 
<b>SelectTerminal</b> call. The CME_STREAM_FAIL or CME_TERMINAL_FAIL event is generated when streaming actually fails, which may also be later than the 
<b>SelectTerminal</b> call.

A terminal can be selected onto a stream only if the results of 
<a href="https://msdn.microsoft.com/8c2006ad-d2f9-4e21-b0ae-583ec3ff82f4">ITTerminal::get_MediaType</a> match 
<a href="https://msdn.microsoft.com/871caaf3-12c4-457c-8d0f-0ee9be52a58b">ITStream::get_MediaType</a>. In addition, some MSPs may require a match between 
<a href="https://msdn.microsoft.com/e0a69c3d-1780-4088-8249-961788dbf184">ITTerminal::get_Direction</a> and 
<a href="https://msdn.microsoft.com/196abe2a-d88d-4b2d-8867-4e6cc15dee33">ITStream::get_Direction</a>, although the interface does not enforce this.

Some MSPs may not allow more than a certain number of terminals, typically one, to be simultaneously selected on the same stream, but the interface itself does not enforce any such restriction. Selecting multiple terminals at one time on the same stream is useful, for example, to allow recording of an incoming audio stream to a file while listening to the stream on a pair of speakers.

A given terminal can be selected onto only one stream.




## -see-also




<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

