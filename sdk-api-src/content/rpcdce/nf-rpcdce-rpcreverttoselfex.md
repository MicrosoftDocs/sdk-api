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

# RpcRevertToSelfEx function


## -description


The 
<b>RpcRevertToSelfEx</b> function allows a server to impersonate a client and then revert in a multithreaded operation where the call to impersonate a client can come from a thread other than the thread originally dispatched from the RPC.


## -parameters




### -param BindingHandle

Binding handle on the server that represents a binding to the client that the server impersonated. A value of zero specifies the client handle of the current thread; in this case, the functionality of 
<b>RpcRevertToSelfEx</b> is identical to that of the 
<a href="https://msdn.microsoft.com/07bbf6fa-f1df-4d9c-ae67-e79e2ccc12c8">RpcRevertToSelf</a> function.


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
<dt><b>RPC_S_NO_CALL_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The server does not have a client to impersonate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This is the wrong kind of binding for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
The call is not supported for this operating system, this transport, or this security subsystem.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



After calling 
<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a> and completing any tasks that require client impersonation, the server calls 
<b>RpcRevertToSelfEx</b> to end impersonation and to reestablish its own security identity. For example, consider a primary thread, called thread1, which is dispatched from a remote client and wakes up a worker thread, called thread2. If thread2 requires that the server impersonate the client, the server calls 
<b>RpcImpersonateClient</b>(THREAD1_CALL_HANDLE), performs the required task, calls 
<b>RpcRevertToSelfEx</b>(THREAD1_CALL_HANDLE) to end the impersonation, and then wakes up thread1.




## -see-also




<a href="https://msdn.microsoft.com/49d833d8-c61c-4746-91cf-c0753847cd3d">Client
		  Impersonation</a>



<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a>



<a href="https://msdn.microsoft.com/07bbf6fa-f1df-4d9c-ae67-e79e2ccc12c8">RpcRevertToSelf</a>
 

 

