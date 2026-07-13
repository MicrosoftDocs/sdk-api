---
UID: NF:rpcdce.RpcSsDontSerializeContext
title: RpcSsDontSerializeContext function (rpcdce.h)
description: The RpcSsDontSerializeContext function disables run-time serialization of multiple calls dispatched to server-manager routines on the same context handle.
helpviewer_keywords: ["RpcSsDontSerializeContext","RpcSsDontSerializeContext function [RPC]","_rpc_rpcssdontserializecontext","rpc.rpcssdontserializecontext","rpcdce/RpcSsDontSerializeContext"]
old-location: rpc\rpcssdontserializecontext.htm
tech.root: Rpc
ms.assetid: 75c8bf34-1522-4db2-9c33-e1ca5ac11e4c
ms.date: 12/05/2018
ms.keywords: RpcSsDontSerializeContext, RpcSsDontSerializeContext function [RPC], _rpc_rpcssdontserializecontext, rpc.rpcssdontserializecontext, rpcdce/RpcSsDontSerializeContext
req.header: rpcdce.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - RpcSsDontSerializeContext
 - rpcdce/RpcSsDontSerializeContext
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
 - RpcSsDontSerializeContext
---

# RpcSsDontSerializeContext function


## -description

The 
<b>RpcSsDontSerializeContext</b> function disables run-time serialization of multiple calls dispatched to server-manager routines on the same context handle. Use of this function is not recommended. Developers should use mixed mode–content handle serialization instead. The See Also section provides links to more appropriate functions.



## -remarks

The 
<b>RpcSsDontSerializeContext</b> function prevents the run time from performing this serialization service, allowing multiple calls to be dispatched on a given context handle. Calling this function does not disable serialization entirely—when a context run down occurs, your context run-down routine will not run until all outstanding client requests have completed. Changes to the context handle state, including freeing the context handle typically, must continue to be serialized.

It is recommended that, if your distributed application invokes the 
<b>RpcSsDontSerializeContext</b> function, the call should be made before the server program begins handling remote procedure calls.

<div class="alert"><b>Note</b>  Typically, the RPC run-time serializes calls on the same context handle dispatched to server manager routines. Context handles are maintained on a per-client basis and typically represent the server-side state. This means that your server manager does not have to guard against another thread from the same client changing the context or against the context running down while a call is dispatched.</div>
<div> </div>
<div class="alert"><b>Note</b>  After it is called, the 
<b>RpcSsDontSerializeContext</b> function is not revertible for the life of the process.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Rpc/multithreaded-clients-and-context-handles">Multithreaded Clients and Context Handles</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcsscontextlockexclusive">RpcSsContextLockExclusive</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcsscontextlockshared">RpcSsContextLockShared</a>



<a href="/windows/desktop/Rpc/server-context-run-down-routine">Server
		  Context Run-down Routine</a>



<a href="/windows/desktop/Midl/context-handle-noserialize">context_handle_noserialize</a>



<a href="/windows/desktop/Midl/context-handle-serialize">context_handle_serialize</a>
