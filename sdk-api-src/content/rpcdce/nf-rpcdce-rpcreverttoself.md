---
UID: NF:rpcdce.RpcRevertToSelf
title: RpcRevertToSelf function (rpcdce.h)
description: After calling RpcImpersonateClient and completing any tasks that require client impersonation, the server calls RpcRevertToSelf to end impersonation and to reestablish its own security identity.
helpviewer_keywords: ["RpcRevertToSelf","RpcRevertToSelf function [RPC]","_rpc_rpcreverttoself","rpc.rpcreverttoself","rpcdce/RpcRevertToSelf"]
old-location: rpc\rpcreverttoself.htm
tech.root: Rpc
ms.assetid: 07bbf6fa-f1df-4d9c-ae67-e79e2ccc12c8
ms.date: 12/05/2018
ms.keywords: RpcRevertToSelf, RpcRevertToSelf function [RPC], _rpc_rpcreverttoself, rpc.rpcreverttoself, rpcdce/RpcRevertToSelf
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
 - RpcRevertToSelf
 - rpcdce/RpcRevertToSelf
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
 - RpcRevertToSelf
---

# RpcRevertToSelf function


## -description

After calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a> and completing any tasks that require client impersonation, the server calls 
<b>RpcRevertToSelf</b> to end impersonation and to reestablish its own security identity.



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

In a multithreaded application, if the call to 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a> is with a handle to another client thread, you must call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex">RpcRevertToSelfEx</a> with the handle to that thread to end impersonation.

## -see-also

<a href="/windows/desktop/Rpc/client-impersonation">Client
		  Impersonation</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a>
