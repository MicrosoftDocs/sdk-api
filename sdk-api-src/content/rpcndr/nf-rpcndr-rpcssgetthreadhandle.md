---
UID: NF:rpcndr.RpcSsGetThreadHandle
title: RpcSsGetThreadHandle function (rpcndr.h)
description: The RpcSsGetThreadHandle function returns a thread handle for the stub memory—management environment.
helpviewer_keywords: ["RpcSsGetThreadHandle","RpcSsGetThreadHandle function [RPC]","_rpc_rpcssgetthreadhandle","rpc.rpcssgetthreadhandle","rpcndr/RpcSsGetThreadHandle"]
old-location: rpc\rpcssgetthreadhandle.htm
tech.root: Rpc
ms.assetid: f3b10f9c-7383-4665-96e3-1518f554f23e
ms.date: 12/05/2018
ms.keywords: RpcSsGetThreadHandle, RpcSsGetThreadHandle function [RPC], _rpc_rpcssgetthreadhandle, rpc.rpcssgetthreadhandle, rpcndr/RpcSsGetThreadHandle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcSsGetThreadHandle
 - rpcndr/RpcSsGetThreadHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcSsGetThreadHandle
---

# RpcSsGetThreadHandle function


## -description

The 
<b>RpcSsGetThreadHandle</b> function returns a thread handle for the stub memory–management environment.



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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls 
<b>RpcSsGetThreadHandle</b> to obtain a thread handle for the stub memory–management environment. A thread used to manage memory for the stub memory–management environment uses 
<b>RpcSsGetThreadHandle</b> to receive a handle for its memory environment. In this way, another thread that calls 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetthreadhandle">RpcSsSetThreadHandle</a> by using this handle can then use the same memory-management environment.

The same thread handle must be used by multiple threads calling 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a> to manage the same memory. Before spawning new threads to manage the same memory, the thread that established the memory-management environment (parent thread) calls 
<b>RpcSsGetThreadHandle</b> to obtain a thread handle for this environment. Then, the spawned threads call 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetthreadhandle">RpcSsSetThreadHandle</a> with the handle provided by the parent thread.

Typically, a server manager procedure calls 
<b>RpcSsGetThreadHandle</b> before additional threads are spawned. The stub sets up the memory-management environment for the manager procedure, and the manager calls 
<b>RpcSsGetThreadHandle</b> to make this environment available to the other threads.

A thread can also call 
<b>RpcSsGetThreadHandle</b> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetthreadhandle">RpcSsSetThreadHandle</a> to save and restore its memory-management environment.

<div class="alert"><b>Note</b>  <b>RpcSsGetThreadHandle</b> raises exceptions, while 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmgetthreadhandle">RpcSmGetThreadHandle</a> returns the error code.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmgetthreadhandle">RpcSmGetThreadHandle</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsssetthreadhandle">RpcSsSetThreadHandle</a>
