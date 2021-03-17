---
UID: NF:rpcdce.RpcServerInqBindingHandle
title: RpcServerInqBindingHandle function (rpcdce.h)
description: Obtains the binding handle for RPC calls serviced by the thread in which RpcServerInqBindingHandle is called.
helpviewer_keywords: ["RpcServerInqBindingHandle","RpcServerInqBindingHandle function [RPC]","rpc.rpcserverinqbindinghandle","rpcdce/RpcServerInqBindingHandle"]
old-location: rpc\rpcserverinqbindinghandle.htm
tech.root: Rpc
ms.assetid: 1b5fa031-ce25-4963-9085-df8786eb88d5
ms.date: 12/05/2018
ms.keywords: RpcServerInqBindingHandle, RpcServerInqBindingHandle function [RPC], rpc.rpcserverinqbindinghandle, rpcdce/RpcServerInqBindingHandle
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - RpcServerInqBindingHandle
 - rpcdce/RpcServerInqBindingHandle
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
 - RpcServerInqBindingHandle
---

# RpcServerInqBindingHandle function


## -description

The <b>RpcServerInqBindingHandle</b> function  obtains the binding handle for RPC calls serviced by the thread in which <b>RpcServerInqBindingHandle</b> is called.

## -parameters

### -param Binding

<a href="/windows/desktop/Rpc/rpc-binding-handle">RPC_BINDING_HANDLE</a> structure that, upon success, receives the binding handle for the call serviced by the thread on which <b>RpcServerInqBindingHandle</b> is also called.

If the call fails, this parameter is undefined.

## -returns

This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned. This function cannot fail unless it is called on a thread that is not currently servicing an RPC call.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

<b>RpcServerInqBindingHandle</b> is used to obtain the binding handle for the RPC call that is currently executing on the thread from which this API is also called. Since many RPC APIs require a binding handle as input, this is a convenient way to obtain a binding handle.

Note that all server-side RPC APIs that take a binding handle as a parameter allow you to pass NULL as an accepted value. Passing NULL instead of a binding handle indicates  that the binding handle for the RPC call currently executing in the same thread should be used. However, if you call a server-side API from a separate thread, then you will need to supply a non-NULL binding handle to them.

If you use explicit binding handles and do not use thread-specific context handles, the binding handle for the call is the first parameter to your server manager routine. However, if you do not use explicit handles or if you use context handles, <b>RpcServerInqBindingHandle</b> is the only way to obtain a binding handle to use in another thread.

This API can be used for both asynchronous and synchronous calls, although it is less useful for asynchronous calls since the binding handle can be obtained as the async state is always the first parameter for all asynchronous RPC calls and the binding handle can be obtained directly from it using <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a>.

## -see-also

<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a>