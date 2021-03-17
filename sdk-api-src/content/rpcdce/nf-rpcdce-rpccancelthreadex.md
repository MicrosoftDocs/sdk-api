---
UID: NF:rpcdce.RpcCancelThreadEx
title: RpcCancelThreadEx function (rpcdce.h)
description: The RpcCancelThreadEx function stops the execution of a thread.
helpviewer_keywords: ["RpcCancelThreadEx","RpcCancelThreadEx function [RPC]","_rpc_rpccancelthreadex","rpc.rpccancelthreadex","rpcdce/RpcCancelThreadEx"]
old-location: rpc\rpccancelthreadex.htm
tech.root: Rpc
ms.assetid: ecf00da0-bc26-4762-94e1-9a5e1cdbc32e
ms.date: 12/05/2018
ms.keywords: RpcCancelThreadEx, RpcCancelThreadEx function [RPC], _rpc_rpccancelthreadex, rpc.rpccancelthreadex, rpcdce/RpcCancelThreadEx
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
 - RpcCancelThreadEx
 - rpcdce/RpcCancelThreadEx
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
 - RpcCancelThreadEx
---

# RpcCancelThreadEx function


## -description

The <b>RpcCancelThreadEx</b> function stops the execution of a thread. The <b>RpcCancelThreadEx</b> function should not be used to stop the execution of an asynchronous RPC call; instead, use the <a href="/windows/win32/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a> function to stop the execution of an asynchronous RPC call.

## -parameters

### -param Thread

Handle of the thread to cancel.

### -param Timeout

Number of seconds to wait for the thread to be canceled before this function returns. To specify that a client waits an indefinite amount of time, pass the value RPC_C_CANCEL_INFINITE_TIMEOUT.

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
<dt><b>RPC_S_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Thread handle does not have privilege. Thread handles must have THREAD_SET_CONTEXT set properly for the function to execute properly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
Called by an MS-DOS or Windows 3.<i>x</i> client.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/win32/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The <b>RpcCancelThreadEx</b> function allows one client thread to cancel an RPC in progress on another client thread. When the function is called, the server run-time is informed of the cancel operation. The server stub can determine if the call has been canceled by calling 
<a href="/windows/win32/api/rpcdce/nf-rpcdce-rpctestcancel">RpcTestCancel</a>. If the call has been canceled, the server stub should clean up and return control to the client.

Using the <i>Timeout</i> parameter, your application can specify the number of seconds to wait for a response. If the server does not return within this interval, the call fails at the client with an RPC_S_CALL_CANCELLED exception. The server stub continues to execute.

If you are using the named pipes protocol, <a href="/windows/win32/midl/ncacn-np">ncacn_np</a>, you must specify a finite time-out.

<div class="alert"><b>Note</b>  You can use <b>RpcCancelThreadEx</b> with any of the connection-oriented protocols (<b>ncacn_*</b>) except 
<a href="/windows/win32/midl/ncacn-http">ncacn_http</a>, and with any of the datagram protocols except 
<a href="/windows/win32/midl/ncadg-mq">ncadg_mq</a> and 
<a href="/windows/win32/midl/ncalrpc">ncalrpc</a>.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a>
<a href="/windows/win32/api/rpcdce/nf-rpcdce-rpccancelthread">RpcCancelThread</a>
<a href="/windows/win32/api/rpcdce/nf-rpcdce-rpctestcancel">RpcTestCancel</a>
<a href="/windows/win32/midl/ncacn-http">ncacn_http</a>
<a href="/windows/win32/midl/ncacn-np">ncacn_np</a>
<a href="/windows/win32/midl/ncadg-mq">ncadg_mq</a>
<a href="/windows/win32/midl/ncalrpc">ncalrpc</a>

