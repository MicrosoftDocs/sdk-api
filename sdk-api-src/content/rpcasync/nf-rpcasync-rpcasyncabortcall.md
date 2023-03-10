---
UID: NF:rpcasync.RpcAsyncAbortCall
title: RpcAsyncAbortCall function (rpcasync.h)
description: The server calls RpcAsyncAbortCall to abort an asynchronous call.
helpviewer_keywords: ["RpcAsyncAbortCall","RpcAsyncAbortCall function [RPC]","_rpc_rpcasyncabortcall","rpc.rpcasyncabortcall","rpcasync/RpcAsyncAbortCall"]
old-location: rpc\rpcasyncabortcall.htm
tech.root: Rpc
ms.assetid: 651c53f3-8bb5-4162-a8a8-2da5a0d05d21
ms.date: 12/05/2018
ms.keywords: RpcAsyncAbortCall, RpcAsyncAbortCall function [RPC], _rpc_rpcasyncabortcall, rpc.rpcasyncabortcall, rpcasync/RpcAsyncAbortCall
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
 - RpcAsyncAbortCall
 - rpcasync/RpcAsyncAbortCall
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
 - RpcAsyncAbortCall
---

# RpcAsyncAbortCall function


## -description

The server calls 
<b>RpcAsyncAbortCall</b> to abort an asynchronous call.

## -parameters

### -param pAsync

Pointer to the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure that contains asynchronous call information.

### -param ExceptionCode

A nonzero application-specific exception code. Can be an application-defined error code, or a standard RPC error code. For more information, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.

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
Call cancelation successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ASYNC_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Asynchronous handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The server calls 
<b>RpcAsyncAbortCall</b> when circumstances require it to abort an asynchronous call before completion. For example, the caller may not have the necessary permissions to make the request, or the server may be too busy to process the call. Use the <i>ExceptionCode</i> parameter to specify the reason for the abort. The run-time environment propagates the exception code to the client as a fault.

When an asynchronous call is aborted with 
<b>RpcAsyncAbortCall</b>, no marshaling of the output arguments is performed, and all input arguments are freed by RPC. When 
<b>RpcAsyncAbortCall</b> is called, a call to the 
<b>RpcAsyncCompleteCall</b> function is not necessary. The 
<b>RpcAsyncAbortCall</b> function should be called only once for any asynchronous call; a second call may crash the process or fail in other unexpected ways.

## -see-also

<a href="/windows/desktop/Rpc/asynchronous-rpc">Asynchronous RPC</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccompletecall">RpcAsyncCompleteCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallstatus">RpcAsyncGetCallStatus</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcservertestcancel">RpcServerTestCancel</a>