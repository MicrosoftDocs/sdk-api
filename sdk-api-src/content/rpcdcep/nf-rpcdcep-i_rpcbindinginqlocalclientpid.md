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

# I_RpcBindingInqLocalClientPID function


## -description


<p class="CCE_Message">[The <b>I_RpcBindingInqLocalClientPID</b> function is available for use in the operating systems specified in the Requirements section. Instead, call <a href="https://msdn.microsoft.com/563b70ed-bc9a-40be-a77b-17b993cc64f3">RpcServerInqCallAttributes</a>.]

The <b>I_RpcBindingInqLocalClientPID</b> function obtains a client process ID.


## -parameters




### -param Binding

TBD


### -param Pid

TBD




#### - ClientBinding [in, optional]

<b>RPC_BINDING_HANDLE</b> that specifies the binding handle for an explicit RPC binding from the client to a server application. 


#### - ClientPID [out]

Contains the process ID of the client that issued the call upon return.


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
The function call was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_CALL_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The current thread does not have an active RPC call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The RPC binding handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The client process ID is only returned in <i>ClientBinding</i> when the "ncalrpc" protocol sequence is used. Until the process terminates, the process ID value uniquely identifies it on the client. When the process terminates, the process ID can be used by new processes.



