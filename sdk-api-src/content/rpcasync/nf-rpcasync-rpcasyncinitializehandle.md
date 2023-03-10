---
UID: NF:rpcasync.RpcAsyncInitializeHandle
title: RpcAsyncInitializeHandle function (rpcasync.h)
description: The client calls the RpcAsyncInitializeHandle function to initialize the RPC_ASYNC_STATE structure to be used to make an asynchronous call.
helpviewer_keywords: ["RpcAsyncInitializeHandle","RpcAsyncInitializeHandle function [RPC]","_rpc_rpcasyncinitializehandle","rpc.rpcasyncinitializehandle","rpcasync/RpcAsyncInitializeHandle"]
old-location: rpc\rpcasyncinitializehandle.htm
tech.root: Rpc
ms.assetid: 97121e6c-af5c-4da8-ad28-24b961c105d2
ms.date: 12/05/2018
ms.keywords: RpcAsyncInitializeHandle, RpcAsyncInitializeHandle function [RPC], _rpc_rpcasyncinitializehandle, rpc.rpcasyncinitializehandle, rpcasync/RpcAsyncInitializeHandle
req.header: rpcasync.h
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
 - RpcAsyncInitializeHandle
 - rpcasync/RpcAsyncInitializeHandle
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
 - RpcAsyncInitializeHandle
---

# RpcAsyncInitializeHandle function


## -description

The client calls the 
<b>RpcAsyncInitializeHandle</b> function to initialize the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure to be used to make an asynchronous call.

## -parameters

### -param pAsync

Pointer to the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure that contains asynchronous call information.

### -param Size

Size of the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure.

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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The size is either too small or too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ASYNC_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>pAsync</i> points to invalid memory.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The client creates a new 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure and a pointer to that structure and calls 
<b>RpcAsyncInitializeHandle</b> with the pointer as an input parameter. The 
<b>RpcAsyncInitializeHandle</b> function initializes the fields that it uses to maintain the state of an asynchronous remote call. When the call to 
<b>RpcAsyncInitializeHandle</b> returns successfully, the client can set the notification type and any fields related to that notification type in the 
<b>RPC_ASYNC_STATE</b> structure. The client application uses a pointer to this structure to make an asynchronous call.

The client should not attempt to alter the <b>Size</b>, <b>Signature</b>, <b>Lock</b>, and <b>StubInfo</b> members of the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure; doing so will invalidate the handle.

<div class="alert"><b>Note</b>  In Windows 2000, after an asynchronous call is completed, the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure must be reinitialized prior to being used for another asynchronous call. In Windows XP and later, the 
<b>RPC_ASYNC_STATE</b> structure is ready for immediate re-use subsequent to a completed asynchronous call.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Rpc/asynchronous-rpc">Asynchronous RPC</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncabortcall">RpcAsyncAbortCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccompletecall">RpcAsyncCompleteCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallstatus">RpcAsyncGetCallStatus</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcservertestcancel">RpcServerTestCancel</a>