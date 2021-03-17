---
UID: NF:rpcdce.RpcRevertToSelfEx
title: RpcRevertToSelfEx function (rpcdce.h)
description: The RpcRevertToSelfEx function allows a server to impersonate a client and then revert in a multithreaded operation where the call to impersonate a client can come from a thread other than the thread originally dispatched from the RPC.
helpviewer_keywords: ["RpcRevertToSelfEx","RpcRevertToSelfEx function [RPC]","_rpc_rpcreverttoselfex","rpc.rpcreverttoselfex","rpcdce/RpcRevertToSelfEx"]
old-location: rpc\rpcreverttoselfex.htm
tech.root: Rpc
ms.assetid: 8860cee2-7e53-4a07-a379-fd00f3d01def
ms.date: 12/05/2018
ms.keywords: RpcRevertToSelfEx, RpcRevertToSelfEx function [RPC], _rpc_rpcreverttoselfex, rpc.rpcreverttoselfex, rpcdce/RpcRevertToSelfEx
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
 - RpcRevertToSelfEx
 - rpcdce/RpcRevertToSelfEx
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
 - RpcRevertToSelfEx
---

# RpcRevertToSelfEx function


## -description

The 
<b>RpcRevertToSelfEx</b> function allows a server to impersonate a client and then revert in a multithreaded operation where the call to impersonate a client can come from a thread other than the thread originally dispatched from the RPC.

## -parameters

### -param BindingHandle

Binding handle on the server that represents a binding to the client that the server impersonated. A value of zero specifies the client handle of the current thread; in this case, the functionality of 
<b>RpcRevertToSelfEx</b> is identical to that of the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself">RpcRevertToSelf</a> function.

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
<dt><b>RPC_S_NO_CALL_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The server does not have a client to impersonate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This is the wrong kind of binding for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
The call is not supported for this operating system, this transport, or this security subsystem.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

After calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a> and completing any tasks that require client impersonation, the server calls 
<b>RpcRevertToSelfEx</b> to end impersonation and to reestablish its own security identity. For example, consider a primary thread, called thread1, which is dispatched from a remote client and wakes up a worker thread, called thread2. If thread2 requires that the server impersonate the client, the server calls 
<b>RpcImpersonateClient</b>(THREAD1_CALL_HANDLE), performs the required task, calls 
<b>RpcRevertToSelfEx</b>(THREAD1_CALL_HANDLE) to end the impersonation, and then wakes up thread1.

## -see-also

<a href="/windows/desktop/Rpc/client-impersonation">Client
		  Impersonation</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself">RpcRevertToSelf</a>