---
UID: NF:rpcdce.RpcImpersonateClient
title: RpcImpersonateClient function (rpcdce.h)
description: A server thread that is processing client remote procedure calls can call the RpcImpersonateClient function to impersonate the active client.
helpviewer_keywords: ["RpcImpersonateClient","RpcImpersonateClient function [RPC]","_rpc_rpcimpersonateclient","rpc.rpcimpersonateclient","rpcdce/RpcImpersonateClient"]
old-location: rpc\rpcimpersonateclient.htm
tech.root: Rpc
ms.assetid: 1b91c4dc-ac49-4002-b293-a25ca2ffcb21
ms.date: 12/05/2018
ms.keywords: RpcImpersonateClient, RpcImpersonateClient function [RPC], _rpc_rpcimpersonateclient, rpc.rpcimpersonateclient, rpcdce/RpcImpersonateClient
req.header: rpcdce.h
req.include-header: 
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
 - RpcImpersonateClient
 - rpcdce/RpcImpersonateClient
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
 - RpcImpersonateClient
---

# RpcImpersonateClient function


## -description

A server thread that is processing client remote procedure calls can call the 
<b>RpcImpersonateClient</b> function to impersonate the active client.

## -parameters

### -param BindingHandle

Binding handle on the server that represents a binding to a client. The server impersonates the client indicated by this handle. If a value of zero is specified, the server impersonates the client that is being served by this server thread.

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
No client is active on this server thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
The function is not supported for either the operating system, the transport, or this security subsystem.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_CONTEXT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The server does not have permission to impersonate the client.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

In a multithreaded application, if the call to 
<b>RpcImpersonateClient</b> is with a handle to another client thread, you must call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex">RpcRevertToSelfEx</a> with the handle to that thread to end impersonation.

All  functions that impersonate check to determine whether the caller of this function (the RPC Server) has the SeImpersonatePrivilege privilege. If the caller has the SeImpersonatePrivilege, or if the authenticated identity is the same as the identity of the caller of this function, the requested impersonation is allowed. Otherwise, the impersonation succeeds at Identify level only.

<b>Windows XP/2000/NT:  </b>The SeImpersonatePrivilege privilege is not supported until Windows XP with Service Pack 2 (SP2).

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
If the call to 
<b>RpcImpersonateClient</b> fails for any reason, the client connection is not impersonated and the client request is made in the security context of the process. If the process is running as a highly privileged account, such as LocalSystem, or as a member of an administrative group, the user may be able to perform actions they would otherwise be disallowed. Therefore it is important to always check the return value of the call, and if it fails, raise an error; do not continue execution of the client request.

## -see-also

<a href="/windows/desktop/Rpc/client-impersonation">Client
		  Impersonation</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself">RpcRevertToSelf</a>