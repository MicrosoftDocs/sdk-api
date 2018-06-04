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

# RpcMgmtIsServerListening function


## -description


The 
<b>RpcMgmtIsServerListening</b> function tells whether a server is listening for remote procedure calls.


## -parameters




### -param Binding

To determine whether a remote application is listening for remote procedure calls, specify a server binding handle for that application. To determine whether your own (local) application is listening for remote procedure calls, specify a value of <b>NULL</b>.


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
Server listening for remote procedure calls.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NOT_LISTENING</b></dt>
</dl>
</td>
<td width="60%">
Server not listening for remote procedure calls, or the interface is auto-listening.

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

<div> </div>


The 
<b>RpcMgmtIsServerListening</b> function returns correct results only for interfaces that are not auto-listening. If the server application is auto-listening and calls the 
<b>RpcMgmtIsServerListening</b> function, 
<b>RpcMgmtIsServerListening</b> returns RPC_SERVER_NOT_LISTENING, yet the server may be listening, and subsequent RPC calls may succeed.




## -remarks



An application calls the 
<b>RpcMgmtIsServerListening</b> function to determine whether the server specified in the <i>Binding</i> parameter is listening for remote procedure calls.

The 
<b>RpcMgmtIsServerListening</b> function returns a value of <b>RPC_S_OK</b> if the server has called 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a>.

The server must be listening for remote procedure calls for this function to succeed.  If the server is not listening, the function fails.




## -see-also




<a href="https://msdn.microsoft.com/839eefea-f06d-412b-9637-4af01b783121">RpcEpResolveBinding</a>



<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a>
 

 

