---
UID: NF:rpcasync.RpcAsyncGetCallHandle
title: RpcAsyncGetCallHandle macro (rpcasync.h)
description: The RpcAsyncGetCallHandle macro returns the binding handle on an asynchronous remote procedure call.
helpviewer_keywords: ["RpcAsyncGetCallHandle","RpcAsyncGetCallHandle macro [RPC]","_rpc_rpcasyncgetcallhandle","rpc.rpcasyncgetcallhandle","rpcasync/RpcAsyncGetCallHandle"]
old-location: rpc\rpcasyncgetcallhandle.htm
tech.root: Rpc
ms.assetid: 5a218d25-187e-4899-8a27-a955f77af8c2
ms.date: 07/01/2025
ms.keywords: RpcAsyncGetCallHandle, RpcAsyncGetCallHandle macro [RPC], _rpc_rpcasyncgetcallhandle, rpc.rpcasyncgetcallhandle, rpcasync/RpcAsyncGetCallHandle
req.header: rpcasync.h
req.include-header: Rpc.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcAsyncGetCallHandle
 - rpcasync/RpcAsyncGetCallHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RpcAsyncGetCallHandle
---

# RpcAsyncGetCallHandle macro

## -syntax

```cpp
void RpcAsyncGetCallHandle(
    PRPC_ASYNC_STATE pAsync
);
```


## -description

The <b>RpcAsyncGetCallHandle</b> macro returns the 
    binding handle on an asynchronous remote procedure call.

## -parameters

### -param pAsync

Pointer to the <a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure that 
       contains asynchronous call information.

## -remarks

Given an asynchronous handle, it returns the corresponding binding handle. For example, the 
     <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcservertestcancel">RpcServerTestCancel</a> function uses the 
     <i>pAsync</i> parameter of 
     <b>RpcAsyncGetCallHandle</b> as a parameter to test for 
     cancel requests.

## -see-also

<a href="/windows/desktop/Rpc/asynchronous-rpc">Asynchronous RPC</a>



<a href="/windows/desktop/Rpc/rpc-macros">RPC Macros</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncabortcall">RpcAsyncAbortCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccompletecall">RpcAsyncCompleteCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallstatus">RpcAsyncGetCallStatus</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcservertestcancel">RpcServerTestCancel</a>
