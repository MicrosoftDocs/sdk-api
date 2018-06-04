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

# RpcMgmtSetComTimeout function


## -description


The 
<b>RpcMgmtSetComTimeout</b> function sets the binding-communications time-out value in a binding handle.


## -parameters




### -param Binding

Server binding handle whose time-out value is set.


### -param Timeout

Communications time-out value, from zero to 10. These values are not seconds; they represent a relative amount of time on a scale of zero to 10.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out value was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



In Windows XP and Windows 2000, during bind the RPC run time uses the shorter of a 15-minute call time-out, and the time-out set using the 
<b>RpcMgmtSetComTimeout</b> function. In exchanges subsequent to binding, the RPC run time uses only the time-out set in using the 
<b>RpcMgmtSetComTimeout</b> function. This option is ignored for <b>ncalrpc</b> and <b>ncadg_*</b> protocol sequences.

A client application calls 
<b>RpcMgmtSetComTimeout</b> to change the communications time-out value for a server binding handle. Depending on the protocol sequence for the specified binding handle, the time-out value acts only as a hint to the RPC run-time library. Each protocol sequence interprets this setting differently; for <b>ncacn_ip_tcp</b>, the value is used to turn on keep-alives for all calls. For example, for <b>ncacn_ip_tcp</b>, setting <i>Timeout</i> to zero instructs RPC to turn on keep-alives if a response isn't received in 60 seconds (the 60 second interval is implementation-specific and subject to change). In this situation, the client call is not timed out as long as the server us running; however, if the server fails or loses its IP address, RPC fails the call. The TCP time-out hint is used during connection establishment, as well as during request/reply exchanges.

<div class="alert"><b>Note</b>  Using the TCP time-out hint is the best practice for detecting failed servers.<p class="note">In Windows XP, keep-alives for a given connection are turned off when the server responds.

</div>
<div> </div>
For convenience, constants are provided for certain values in the time-out range. For a list of the RPC-defined values that an application can use for the time-out argument, see 
<a href="https://msdn.microsoft.com/bf5f3f08-ab29-4732-9ce3-d6d7ad699369">Binding Time-out Constants</a>.




## -see-also




<a href="https://msdn.microsoft.com/e7bb9955-68a7-49fe-bcdb-2450518ffe0a">RpcMgmtInqComTimeout</a>
 

 

