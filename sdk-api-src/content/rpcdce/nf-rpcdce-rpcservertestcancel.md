---
UID: NF:rpcdce.RpcServerTestCancel
title: RpcServerTestCancel function (rpcdce.h)
description: The server calls RpcServerTestCancel to test for client cancel requests.
helpviewer_keywords: ["RpcServerTestCancel","RpcServerTestCancel function [RPC]","_rpc_rpcservertestcancel","rpc.rpcservertestcancel","rpcdce/RpcServerTestCancel"]
old-location: rpc\rpcservertestcancel.htm
tech.root: Rpc
ms.assetid: de4b45a8-0516-4185-a342-364e0f5a633e
ms.date: 12/05/2018
ms.keywords: RpcServerTestCancel, RpcServerTestCancel function [RPC], _rpc_rpcservertestcancel, rpc.rpcservertestcancel, rpcdce/RpcServerTestCancel
req.header: rpcdce.h
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcServerTestCancel
 - rpcdce/RpcServerTestCancel
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
 - RpcServerTestCancel
---

# RpcServerTestCancel function


## -description

The server calls 
<b>RpcServerTestCancel</b> to test for client cancel requests.

## -parameters

### -param BindingHandle

Call to test for cancel commands. If a value of zero is specified, the server impersonates the client that is being served by this server thread.

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
The call was canceled by the client. The server must still complete or abort the call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_CALL_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
There is no active call on the current thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CALL_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The call was not canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The server calls 
<b>RpcServerTestCancel</b> to find out if the client has requested cancelation of an outstanding call. The 
<b>RpcServerTestCancel</b> function only indicates whether a client has canceled the call; state is not changed on the server or client. The canceled call must still be completed or aborted by the RPC server, using 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccompletecall">RpcAsyncCompleteCall</a> or 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncabortcall">RpcAsyncAbortCall</a> function calls, respectively.

The <i>BindingHandle</i> parameter specifies the call on which to test. If the parameter has a value of zero, the call on the current thread is tested. The server can call the 
<b>RpcServerTestCancel(RpcAsyncGetCallHandle(pAsync))</b> function to test for a cancel message using the asynchronous handle to obtain the binding handle.

## -see-also

<a href="/windows/desktop/Rpc/asynchronous-rpc">Asynchronous RPC</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncabortcall">RpcAsyncAbortCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccompletecall">RpcAsyncCompleteCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallstatus">RpcAsyncGetCallStatus</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a>