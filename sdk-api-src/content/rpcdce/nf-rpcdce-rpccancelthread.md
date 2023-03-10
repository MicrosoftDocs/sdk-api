---
UID: NF:rpcdce.RpcCancelThread
title: RpcCancelThread function (rpcdce.h)
description: The RpcCancelThread function cancels a thread. The RpcCancelThread function should not be used to cancel asynchronous RPC calls; instead, use the RpcAsyncCancelCall function to cancel an asynchronous RPC call.
helpviewer_keywords: ["RpcCancelThread","RpcCancelThread function [RPC]","_rpc_rpccancelthread","rpc.rpccancelthread","rpcdce/RpcCancelThread"]
old-location: rpc\rpccancelthread.htm
tech.root: Rpc
ms.assetid: 4315562e-674b-40a4-a2d9-133e6ab27c25
ms.date: 12/05/2018
ms.keywords: RpcCancelThread, RpcCancelThread function [RPC], _rpc_rpccancelthread, rpc.rpccancelthread, rpcdce/RpcCancelThread
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
 - RpcCancelThread
 - rpcdce/RpcCancelThread
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
 - RpcCancelThread
---

# RpcCancelThread function


## -description

The 
<b>RpcCancelThread</b> function cancels a thread. The 
<b>RpcCancelThread</b> function should not be used to cancel asynchronous RPC calls; instead, use the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a> function to cancel an asynchronous RPC call.

## -parameters

### -param Thread

Handle of the thread to cancel.

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
Called by an MS-DOS or Windows 3.x client.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcCancelThread</b> function allows one client thread to cancel an RPC in progress on another client thread. When the function is called, the server run-time is informed of the cancel operation. The server stub can determine if the call has been canceled by calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpctestcancel">RpcTestCancel</a>. If the call has been canceled, the server stub should clean up and return control to the client.

The <b>RpcCancelThread</b> function cannot be used to cancel a call that has issued a static callback.  Do not cancel remote procedure calls that may call a function declared with the <b>[callback]</b> attribute in the IDL-file.

By default, the client waits forever for the server to return control after a cancel. To reduce this time, call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtsetcanceltimeout">RpcMgmtSetCancelTimeout</a>, specifying the number of seconds to wait for a response. If the server does not return within this interval, the call fails at the client with an <b>RPC_S_CALL_FAILED</b> exception. The server stub continues to run.

If you are using the named pipes protocol, <b>ncacn_np</b>, you must specify a finite time-out.

You can use 
<b>RpcCancelThread</b> with any of the connection-oriented protocols <b>(ncacn_*)</b> and with any of the datagram protocols except <b>ncadg_mq</b> and <b>ncalrpc</b>. 

<b>Note</b>  Windows XP/2000 The <b>RpcCancelThread</b> function is not available for <b>ncacn_http</b>.  The <b>RpcCancelThread</b> function supports <b>ncacn_http</b> on Windows Server 2003 or later operating systems and Windows XP with Service Pack 1 (SP1) and later.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpctestcancel">RpcTestCancel</a>



<a href="/windows/win32/midl/ncacn-http">ncacn_http</a>



<a href="/windows/win32/midl/ncadg-mq">ncadg_mq</a>



<a href="/windows/win32/midl/ncalrpc">ncalrpc</a>