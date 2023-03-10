---
UID: NF:rpcasync.RpcBindingBind
title: RpcBindingBind function (rpcasync.h)
description: The RpcBindingBind function contacts an RPC server and binds to it.
helpviewer_keywords: ["RpcBindingBind","RpcBindingBind function [RPC]","rpc.rpcbindingbind","rpcasync/RpcBindingBind"]
old-location: rpc\rpcbindingbind.htm
tech.root: Rpc
ms.assetid: dbc73a66-b1ca-4a53-b662-430b611f8c20
ms.date: 12/05/2018
ms.keywords: RpcBindingBind, RpcBindingBind function [RPC], rpc.rpcbindingbind, rpcasync/RpcBindingBind
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps \| UWP apps]
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
 - RpcBindingBind
 - rpcasync/RpcBindingBind
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
 - RpcBindingBind
---

# RpcBindingBind function


## -description

The <b>RpcBindingBind</b> function contacts an RPC server and binds to it.

## -parameters

### -param pAsync [in, optional]

Pointer to the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a> structure that contains asynchronous call information. This state information contains the completion method used to signal when the bind operation is complete.

### -param Binding [in]

<a href="/windows/desktop/Rpc/rpc-binding-handle">RPC_BINDING_HANDLE</a> structure that contains the binding handle created with a previous call to <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcreatea">RpcBindingCreate</a>.

### -param IfSpec [in]

<a href="/windows/desktop/Rpc/rpc-if-handle">RPC_IF_HANDLE</a> value that specifies the interface on which calls for this binding handle will be made.

## -returns

This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned. For information on these error codes, see <a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The RPC is successfully bound to the server and remote calls can be made.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
An obsolete feature of RPC was requested for this binding operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

<b>RpcBindingBind</b> contacts the RPC server and binds to it using the binding handle returned by a previous call to <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcreatea">RpcBindingCreate</a>. Binding handles established using this method are referred to as "fast" binding handles.

If the value of the <i>pAsync</i> parameter is not <b>NULL</b>, then the bind will be asynchronous and calls to <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a> and <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallstatus">RpcAsyncGetCallStatus</a> can be made on the supplied async state. The completion method specified in the async state information wis used to signal the caller that the bind is complete. Upon notification of completion, calls can be made using the newly-bound binding handle.

The bind method does not determine what calls can be made using the binding handle — if the bind is synchronous, asynchronous calls can still be made on the binding handle, and vice versa. The bind method determines how notification for a successful bind is signaled, specifically in the case of asynchronous binds.

Since this API exchanges messages with the RPC server, bind operations can take a long time based on a number of independent factors including network traffic and server blocking. If the binding is synchronous, the bind operation can block if the server is blocked.

After the bind is complete, the semantics of calls made on the binding handle are the same as calls made on any other type of binding handle, but with four notable differences, listed below:


<ul>
<li>All calls on this binding handle must be made on the interface specified in <i>IfSpec</i>. The binding handle is uniquely tied to this interface. The interface itself can be unloaded before the binding handle is destroyed, but extensive information about the interface is cached in the binding handle, and if a call is made on the same binding handle for a different interface, the results are undefined.</li>
<li>RPC callbacks are not allowed on a binding handle. If the RPC server attempts to make a callback using a method with the [callback] attribute, the call is rejected with the RPC_S_CANNOT_SUPPORT error status code.</li>
<li>With classic binding handles, RPC will attempt to transparently reconnect with the server  if the connection is dropped. For fast binding handles, RPC will not attempt to transparently reconnect to the server; instead, it  will return one of the following errors: RPC_S_SERVER_UNAVAILABLE, RPC_S_CALL_FAILED, and RPC_C_CALL_FAILED_DNE.  If the connection is dropped due to rejected credentials, RPC_S_ACCESS_DENIED is returned; and if the server encounters a transient error due to a lack of memory, RPC_S_OUT_OF_MEMORY is returned. Any other connectivity errors are the result of marshaling or unmarshaling errors returned by server routines.In the case of a lost connection, the called must unbind by calling <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcbindingunbind">RpcBindingUnbind</a> and then rebind with another call to <b>RpcBindingBind</b>.

</li>
</ul>


If the call to <b>RpcBindingBind</b> fails, then the binding handle is not bound to the server and the caller can attempt to bind again with another call to the same API, or it can free the binding handle. Since a failed bind operation does not move the binding handle to the bound state, <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcbindingunbind">RpcBindingUnbind</a> must not be called on it.

Certain functions must not be called until the bind operation has signaled completion, specifically:<ul>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingreset">RpcBindingReset</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a> and <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa">RpcBindingSetAuthInfoEx</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetobject">RpcBindingSetObject</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption">RpcBindingSetOption</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout">RpcMgmtSetComTimeout</a>
</li>
</ul>


<div class="alert"><b>Note</b>  Currently, this function supports only the <b>ncalrpc</b> protocol sequence.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcreatea">RpcBindingCreate</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcbindingunbind">RpcBindingUnbind</a>