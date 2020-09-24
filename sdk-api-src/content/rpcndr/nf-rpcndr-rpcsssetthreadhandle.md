---
UID: NF:rpcndr.RpcSsSetThreadHandle
title: RpcSsSetThreadHandle function (rpcndr.h)
description: The RpcSsSetThreadHandle function sets a thread handle for the stub memory–management environment.
helpviewer_keywords: ["RpcSsSetThreadHandle","RpcSsSetThreadHandle function [RPC]","_rpc_rpcsssetthreadhandle","rpc.rpcsssetthreadhandle","rpcndr/RpcSsSetThreadHandle"]
old-location: rpc\rpcsssetthreadhandle.htm
tech.root: Rpc
ms.assetid: 8984e253-ea78-4ca2-bf24-83100a0ac79d
ms.date: 12/05/2018
ms.keywords: RpcSsSetThreadHandle, RpcSsSetThreadHandle function [RPC], _rpc_rpcsssetthreadhandle, rpc.rpcsssetthreadhandle, rpcndr/RpcSsSetThreadHandle
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
 - RpcSsSetThreadHandle
 - rpcndr/RpcSsSetThreadHandle
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
 - RpcSsSetThreadHandle
---

# RpcSsSetThreadHandle function


## -description

The 
<b>RpcSsSetThreadHandle</b> function sets a thread handle for the stub memory–management environment.

## -parameters

### -param Id

Thread handle returned by a call to 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a>.

## -remarks

An application calls 
<b>RpcSsSetThreadHandle</b> to set a thread handle for the stub memory–management environment. A thread used to manage memory for the stub memory–management environment calls 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a> to obtain a handle for its memory environment. In this way, another thread that calls 
<b>RpcSsSetThreadHandle</b> by using this handle can then use the same memory-management environment.

The same thread handle must be used by multiple threads calling 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a> and 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a> in order to manage the same memory. Before spawning new threads to manage the same memory, the thread that established the memory-management environment (parent thread) calls 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a> to obtain a thread handle for this environment. Then, the spawned threads call 
<b>RpcSsSetThreadHandle</b> with the handle provided by the parent thread.

Typically, a thread spawned by a server manager procedure calls 
<b>RpcSsSetThreadHandle</b>. The stub sets up the memory-management environment for the manager procedure, and the manager calls 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a> to obtain a thread handle. Then, each spawned thread calls 
<b>RpcSsGetThreadHandle</b> to get access to the manager's memory-management environment.

A thread can also call 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a> and 
<b>RpcSsSetThreadHandle</b> to save and restore its memory-management environment.

<div class="alert"><b>Note</b>  The 
<b>RpcSsSetThreadHandle</b> routine raises exceptions, while the 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetthreadhandle">RpcSmSetThreadHandle</a> routine returns the error code.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmsetthreadhandle">RpcSmSetThreadHandle</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssallocate">RpcSsAllocate</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssfree">RpcSsFree</a>



<a href="/windows/desktop/api/rpcndr/nf-rpcndr-rpcssgetthreadhandle">RpcSsGetThreadHandle</a>