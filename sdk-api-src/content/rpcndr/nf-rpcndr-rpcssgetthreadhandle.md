---
UID: NF:rpcndr.RpcSsGetThreadHandle
title: RpcSsGetThreadHandle function
author: windows-sdk-content
description: The RpcSsGetThreadHandle function returns a thread handle for the stub memory&#8211;management environment.
old-location: rpc\rpcssgetthreadhandle.htm
old-project: rpc
ms.assetid: f3b10f9c-7383-4665-96e3-1518f554f23e
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: RpcSsGetThreadHandle, RpcSsGetThreadHandle function [RPC], _rpc_rpcssgetthreadhandle, rpc.rpcssgetthreadhandle, rpcndr/RpcSsGetThreadHandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcSsGetThreadHandle
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcSsGetThreadHandle function


## -description


The 
<b>RpcSsGetThreadHandle</b> function returns a thread handle for the stub memory–management environment.


## -parameters






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



An application calls 
<b>RpcSsGetThreadHandle</b> to obtain a thread handle for the stub memory–management environment. A thread used to manage memory for the stub memory–management environment uses 
<b>RpcSsGetThreadHandle</b> to receive a handle for its memory environment. In this way, another thread that calls 
<a href="https://msdn.microsoft.com/8984e253-ea78-4ca2-bf24-83100a0ac79d">RpcSsSetThreadHandle</a> by using this handle can then use the same memory-management environment.

The same thread handle must be used by multiple threads calling 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a> and 
<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a> to manage the same memory. Before spawning new threads to manage the same memory, the thread that established the memory-management environment (parent thread) calls 
<b>RpcSsGetThreadHandle</b> to obtain a thread handle for this environment. Then, the spawned threads call 
<a href="https://msdn.microsoft.com/8984e253-ea78-4ca2-bf24-83100a0ac79d">RpcSsSetThreadHandle</a> with the handle provided by the parent thread.

Typically, a server manager procedure calls 
<b>RpcSsGetThreadHandle</b> before additional threads are spawned. The stub sets up the memory-management environment for the manager procedure, and the manager calls 
<b>RpcSsGetThreadHandle</b> to make this environment available to the other threads.

A thread can also call 
<b>RpcSsGetThreadHandle</b> and 
<a href="https://msdn.microsoft.com/8984e253-ea78-4ca2-bf24-83100a0ac79d">RpcSsSetThreadHandle</a> to save and restore its memory-management environment.

<div class="alert"><b>Note</b>  <b>RpcSsGetThreadHandle</b> raises exceptions, while 
<a href="https://msdn.microsoft.com/5bf2c93c-8273-484b-a79f-821b2068692d">RpcSmGetThreadHandle</a> returns the error code.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5bf2c93c-8273-484b-a79f-821b2068692d">RpcSmGetThreadHandle</a>



<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>



<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a>



<a href="https://msdn.microsoft.com/8984e253-ea78-4ca2-bf24-83100a0ac79d">RpcSsSetThreadHandle</a>
 

 

