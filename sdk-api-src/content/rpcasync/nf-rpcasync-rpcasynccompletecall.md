---
UID: NF:rpcasync.RpcAsyncCompleteCall
title: RpcAsyncCompleteCall function (rpcasync.h)
description: The client and the server call the RpcAsyncCompleteCall function to complete an asynchronous remote procedure call.
helpviewer_keywords: ["RpcAsyncCompleteCall","RpcAsyncCompleteCall function [RPC]","_rpc_rpcasynccompletecall","rpc.rpcasynccompletecall","rpcasync/RpcAsyncCompleteCall"]
old-location: rpc\rpcasynccompletecall.htm
tech.root: Rpc
ms.assetid: 76b6bc3a-f5d1-4780-8071-9b221a6fd7d8
ms.date: 12/05/2018
ms.keywords: RpcAsyncCompleteCall, RpcAsyncCompleteCall function [RPC], _rpc_rpcasynccompletecall, rpc.rpcasynccompletecall, rpcasync/RpcAsyncCompleteCall
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
 - RpcAsyncCompleteCall
 - rpcasync/RpcAsyncCompleteCall
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
 - RpcAsyncCompleteCall
---

# RpcAsyncCompleteCall function


## -description

The client and the server call the 
<b>RpcAsyncCompleteCall</b> function to complete an asynchronous remote procedure call.

## -parameters

### -param pAsync

Pointer to the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure that contains asynchronous call information.

### -param Reply

Pointer to a buffer containing the return value of the remote procedure call.

## -returns

In addition to the following values, 
<b>RpcAsyncCompleteCall</b> can also return any general RPC or application-specific error. 

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
The call was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ASYNC_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous call handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_ASYNC_CALL_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The call has not yet completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CALL_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The call was canceled.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

Completes the asynchronous RPC call. Both client and server call this function.

Client: <i>Reply</i> points to a buffer that will receive the reply. If the client calls this function before the reply has arrived, the call returns RPC_S_ASYNC_CALL_PENDING. The buffer must be valid and it must be big enough to receive the return value. If this call is successful, the 
				<a href="/windows/desktop/Midl/out-idl">[out]</a> and the 
				<a href="/windows/desktop/Midl/in">[in,</a> <b>out]</b> parameters are valid. If the call does not return RPC_S_ASYNC_CALL_PENDING, this 
<b>RpcAsyncCompleteCall</b> invocation is final for the RPC call. After this function call, regardless of success or failure, all resources allocated by the RPC runtime are freed. Subsequent calls to the 
<b>RpcAsyncCompleteCall</b> or 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a> functions have undefined results until a new call on the RPC_ASYNC_STATE structure is initiated.

Server: <i>Reply</i> points to a buffer that contains the return value that needs to be sent to the client. You only need to set a valid buffer for <i>Reply</i> if your function is declared with a return type.  Before a call to 
<b>RpcAsyncCompleteCall</b> is made, the <a href="/windows/desktop/Midl/out-idl">[out]</a> and 
				<a href="/windows/desktop/Midl/in">[in,</a> <b>out]</b> parameters must be updated. These parameters, and the asynchronous handle, should not be touched after the call to 
<b>RpcAsyncCompleteCall</b> returns. The invocation of <b>RpcAsyncCompleteCall</b> on the server is final. If the  <b>RpcAsyncCompleteCall</b> function call fails, the RPC runtime frees the parameters.

Any <a href="/windows/desktop/Midl/out-idl">[out]</a> parameters, including 
				<a href="/windows/desktop/Midl/comm-status">[comm_status]</a> and 
				<a href="https://msdn.microsoft.com/">[fault_status]</a> parameters, are only valid if the return value of 
<b>RpcAsyncCompleteCall</b> is RPC_S_OK.

## -see-also

<a href="/windows/desktop/Rpc/asynchronous-rpc">Asynchronous RPC</a>



<a href="/windows/desktop/Rpc/error-handling">Error Handling</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncabortcall">RpcAsyncAbortCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallstatus">RpcAsyncGetCallStatus</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcservertestcancel">RpcServerTestCancel</a>