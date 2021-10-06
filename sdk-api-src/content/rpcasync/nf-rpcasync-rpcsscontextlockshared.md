---
UID: NF:rpcasync.RpcSsContextLockShared
title: RpcSsContextLockShared function (rpcasync.h)
description: The RpcSsContextLockShared function enables an application to begin using a context handle in shared mode.
helpviewer_keywords: ["RpcSsContextLockShared","RpcSsContextLockShared function [RPC]","_rpc_rpcsscontextlockshared","rpc.rpcsscontextlockshared","rpcasync/RpcSsContextLockShared"]
old-location: rpc\rpcsscontextlockshared.htm
tech.root: Rpc
ms.assetid: 469f0995-54ff-40a6-9322-3d173e2c9861
ms.date: 12/05/2018
ms.keywords: RpcSsContextLockShared, RpcSsContextLockShared function [RPC], _rpc_rpcsscontextlockshared, rpc.rpcsscontextlockshared, rpcasync/RpcSsContextLockShared
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - RpcSsContextLockShared
 - rpcasync/RpcSsContextLockShared
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
 - RpcSsContextLockShared
---

# RpcSsContextLockShared function


## -description

The 
<b>RpcSsContextLockShared</b> function enables an application to begin using a context handle in shared mode.

## -parameters

### -param ServerBindingHandle [in]

Binding handle on the server that represents a binding to a client. The server impersonates the client indicated by this handle. If a value of zero is specified, the server impersonates the client that is being served by this server thread.

### -param UserContext [in]

Pointer passed to the manager or server routine by RPC. See Remarks for more information. 




For [out] only context handles, the 
<b>RpcSsContextLockShared</b> function performs no operation.

## -returns

Returns RPC_S_OK upon successful execution, indicating the thread now has access to the context handle in shared mode.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

Modifying whether a context handle is serialized or nonserialized can be useful to applications that determine whether to close a context handle based on conditions detected upon execution. To change a context handle from nonserialized (shared) to serialized (exclusive), use the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcsscontextlockexclusive">RpcSsContextLockExclusive</a> function.

For the <i>UserContext</i> parameter, if the manager routine receives a pointer to a context handle, it must pass the 
<b>RpcSsContextLockShared</b> function the same pointer it received from RPC. If the manager routine receives the context handle itself, which is typical for [in] only context handles, it must pass the context handle itself to the 
<b>RpcSsContextLockShared</b> function. The following code example demonstrates this:


``` syntax
UseExclusive (..., /* [in] */ TestContextHandleExclusive *Ctx, ...)
{
    ...
    // we decided that we're done changing the context handle exclusively
    // and that we have extensive processing ahead - downgrade the exclusive
    // lock to shared, and do the processing allowing other readers in
    RpcSsContextLockShared (NULL,    // use the explicit context
        Ctx
        );
    ...
}
```

If a manager routine takes multiple [in, out] context handles as an argument, RPC gives the manager routine a pointer to the context handle, not the context handle itself. The pointer is guaranteed to be unique, and therefore passing it to the 
<b>RpcSsContextLockShared</b> function is unambiguous. However, if a function takes multiple [in] only context handles, RPC gives the manager routine the context handle itself. Therefore, the context handle may not be unique. In this case, RPC executes this function on the first context handle with the given value.

Methods should not modify a context handle when in shared mode. Calling the 
<b>RpcSsContextLockShared</b> function does not eliminate a writer lock on the specified context handle; this ensures the context handle will not be changed by another thread.

Asynchronous calls must not use the 
<b>RpcSsContextLockShared</b> function on the same call object from more than one thread at a time.

The 
<b>RpcSsContextLockShared</b> function can fail due to out-of-memory conditions, and RPC servers must therefore be prepared to handle such errors.

## -see-also

<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcsscontextlockexclusive">RpcSsContextLockExclusive</a>



<a href="/windows/desktop/Midl/context-handle">context_handle</a>



<a href="/windows/desktop/Midl/context-handle-noserialize">context_handle_noserialize</a>



<a href="/windows/desktop/Midl/context-handle-serialize">context_handle_serialize</a>
