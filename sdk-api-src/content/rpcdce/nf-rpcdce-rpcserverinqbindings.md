---
UID: NF:rpcdce.RpcServerInqBindings
title: RpcServerInqBindings function (rpcdce.h)
description: The RpcServerInqBindings function returns the binding handles over which remote procedure calls can be received.
helpviewer_keywords: ["RpcServerInqBindings","RpcServerInqBindings function [RPC]","_rpc_rpcserverinqbindings","rpc.rpcserverinqbindings","rpcdce/RpcServerInqBindings"]
old-location: rpc\rpcserverinqbindings.htm
tech.root: Rpc
ms.assetid: 96f081ab-6210-4ca0-a913-182477463981
ms.date: 12/05/2018
ms.keywords: RpcServerInqBindings, RpcServerInqBindings function [RPC], _rpc_rpcserverinqbindings, rpc.rpcserverinqbindings, rpcdce/RpcServerInqBindings
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
 - RpcServerInqBindings
 - rpcdce/RpcServerInqBindings
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
 - RpcServerInqBindings
---

# RpcServerInqBindings function


## -description

The 
<b>RpcServerInqBindings</b> function returns the binding handles over which remote procedure calls can be received.

## -parameters

### -param BindingVector

Returns a pointer to a pointer to a vector of server binding handles.

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
<dt><b>RPC_S_NO_BINDINGS</b></dt>
</dl>
</td>
<td width="60%">
There are no bindings.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A server application calls 
<b>RpcServerInqBindings</b> to obtain a vector of server binding handles. The RPC run-time library creates binding handles when a server application calls the following functions to register protocol sequences:

<ul>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsex">RpcServerUseAllProtseqsEx</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif">RpcServerUseAllProtseqsIf</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex">RpcServerUseAllProtseqsIfEx</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseq">RpcServerUseProtseq</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqex">RpcServerUseProtseqEx</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex">RpcServerUseProtseqEpEx</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif">RpcServerUseProtseqIf</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqifex">RpcServerUseProtseqIfEx</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqep">RpcServerUseProtseqEp</a>
</li>
</ul>
The returned binding vector can contain binding handles with dynamic endpoints or binding handles with well-known endpoints, depending on which of the above functions the server application called.

A server uses the vector of binding handles for exporting to the name service, for registering with the local endpoint-map database, or for conversion to string bindings. If there are no binding handles (no registered protocol sequences), this routine returns the RPC_S_NO_BINDINGS status code and a <i>BindingVector</i> parameter value of NULL. The server is responsible for calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingvectorfree">RpcBindingVectorFree</a> function to release the memory used by the vector.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingvectorfree">RpcBindingVectorFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif">RpcServerUseAllProtseqsIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseq">RpcServerUseProtseq</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqep">RpcServerUseProtseqEp</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif">RpcServerUseProtseqIf</a>