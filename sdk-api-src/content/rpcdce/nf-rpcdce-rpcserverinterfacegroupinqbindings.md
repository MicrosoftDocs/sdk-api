---
UID: NF:rpcdce.RpcServerInterfaceGroupInqBindings
title: RpcServerInterfaceGroupInqBindings function (rpcdce.h)
description: The RpcServerInterfaceGroupInqBindings function returns the binding handles over which remote procedure calls can be received for the given interface group.
helpviewer_keywords: ["RpcServerInterfaceGroupInqBindings","RpcServerInterfaceGroupInqBindings function [RPC]","rpc.rpcserverinterfacegroupinqbindings","rpcdce/RpcServerInterfaceGroupInqBindings"]
old-location: rpc\rpcserverinterfacegroupinqbindings.htm
tech.root: Rpc
ms.assetid: 90535A05-9835-45F2-A62F-718736A80ED3
ms.date: 12/05/2018
ms.keywords: RpcServerInterfaceGroupInqBindings, RpcServerInterfaceGroupInqBindings function [RPC], rpc.rpcserverinterfacegroupinqbindings, rpcdce/RpcServerInterfaceGroupInqBindings
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - RpcServerInterfaceGroupInqBindings
 - rpcdce/RpcServerInterfaceGroupInqBindings
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
 - RpcServerInterfaceGroupInqBindings
---

# RpcServerInterfaceGroupInqBindings function


## -description

The <b>RpcServerInterfaceGroupInqBindings</b> function returns the binding handles over which remote procedure calls can be received for the given interface group.

## -parameters

### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a> that defines the interface group for which the bindings should be queried.

### -param BindingVector [out]

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

A server application calls <b>RpcServerInterfaceGroupInqBindings</b> to obtain a vector of server binding handles for the given interface group. The RPC run-time library creates binding handles for an interface group when a server application calls the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupactivate">RpcServerInterfaceGroupActivate</a> function.

The returned binding vector can contain binding handles with dynamic endpoints or binding handles with well-known endpoints, depending on the interface group’s endpoint specification.

A server uses the vector of binding handles for exporting to the name service or for conversion to string bindings.  If there are no binding handles (no registered protocol sequences), <b>RpcServerInterfaceGroupInqBindings</b> returns <b>RPC_S_NO_BINDINGS</b> and <i>BindingVector</i> is <b>NULL</b>. The server is responsible for calling <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingvectorfree">RpcBindingVectorFree</a> to release the vector's memory.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupactivate">RpcServerInterfaceGroupActivate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupclose">RpcServerInterfaceGroupClose</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupdeactivate">RpcServerInterfaceGroupDeactivate</a>