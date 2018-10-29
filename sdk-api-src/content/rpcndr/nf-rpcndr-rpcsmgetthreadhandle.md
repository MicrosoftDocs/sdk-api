---
UID: NF:rpcndr.RpcSmGetThreadHandle
title: RpcSmGetThreadHandle function
author: windows-sdk-content
description: The RpcSmGetThreadHandle function returns a thread handle, or NULL, for the stub memory&#8211;management environment.
old-location: rpc\rpcsmgetthreadhandle.htm
tech.root: Rpc
ms.assetid: 5bf2c93c-8273-484b-a79f-821b2068692d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RpcSmGetThreadHandle, RpcSmGetThreadHandle function [RPC], _rpc_rpcsmgetthreadhandle, rpc.rpcsmgetthreadhandle, rpcndr/RpcSmGetThreadHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcSmGetThreadHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcSmGetThreadHandle function


## -description


The 
<b>RpcSmGetThreadHandle</b> function returns a thread handle, or <b>NULL</b>, for the stub memory–management environment.


## -parameters




### -param pStatus

Pointer to the returned status.


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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Applications call 
<b>RpcSmGetThreadHandle</b> to obtain a thread handle for the stub memory–management environment. A thread used to manage memory for the stub memory–management environment uses 
<b>RpcSmGetThreadHandle</b> to receive a handle for its memory environment. In this way, another thread that calls 
<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a> by using this handle can then use the same memory-management environment.

The same memory management thread handle must be used by multiple threads calling 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a> and 
<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a> in order to manage the same memory. Before spawning new threads to manage the same memory, the thread that established the memory-management environment (parent thread) calls 
<b>RpcSmGetThreadHandle</b> to obtain a thread handle for this environment. Then, the spawned threads call 
<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a> with the new manager handle provided by the parent thread.

Typically a server manager procedure calls 
<b>RpcSmGetThreadHandle</b> before additional threads are spawned. The stub sets up the memory-management environment for the manager procedure, and the manager calls 
<b>RpcSmGetThreadHandle</b> to make this environment available to the other threads.

A thread can also call 
<b>RpcSmGetThreadHandle</b> and 
<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a> to save and restore its memory-management environment.




## -see-also




<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>



<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a>



<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a>
 

 

