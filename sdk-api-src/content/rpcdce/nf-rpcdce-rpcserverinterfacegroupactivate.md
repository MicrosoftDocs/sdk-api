---
UID: NF:rpcdce.RpcServerInterfaceGroupActivate
title: RpcServerInterfaceGroupActivate function (rpcdce.h)
description: The RpcServerInterfaceGroupActivate function tells the RPC server runtime to register the interface group’s interfaces and endpoints and begin listening for calls.
helpviewer_keywords: ["RpcServerInterfaceGroupActivate","RpcServerInterfaceGroupActivate function [RPC]","rpc.rpcserverinterfacegroupactivate","rpcdce/RpcServerInterfaceGroupActivate"]
old-location: rpc\rpcserverinterfacegroupactivate.htm
tech.root: Rpc
ms.assetid: A467DDEC-BEB1-4050-B540-4A1E819E7373
ms.date: 12/05/2018
ms.keywords: RpcServerInterfaceGroupActivate, RpcServerInterfaceGroupActivate function [RPC], rpc.rpcserverinterfacegroupactivate, rpcdce/RpcServerInterfaceGroupActivate
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
 - RpcServerInterfaceGroupActivate
 - rpcdce/RpcServerInterfaceGroupActivate
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
 - RpcServerInterfaceGroupActivate
---

# RpcServerInterfaceGroupActivate function


## -description

The <b>RpcServerInterfaceGroupActivate</b> function tells the RPC server runtime to register the interface group’s interfaces and endpoints and begin listening for calls.

## -parameters

### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a> that defines the interface group to activate.

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
<dt><b>RPC_S_PROTSEQ_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The protocol sequence is not supported on this host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_RPC_PROTSEQ</b></dt>
</dl>
</td>
<td width="60%">
The protocol sequence is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ENDPOINT_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The endpoint format is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_SECURITY_DESC</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor for an endpoint or interface is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

<b>RpcServerInterfaceGroupActivate</b> does the bulk of the initialization work that the RPC server applications need to do.  It performs the following operations:<ul>
<li>Instructs the RPC runtime to begin listening for calls.</li>
<li>Registers the endpoints with the server runtime.</li>
<li>Registers the interfaces with the server runtime.</li>
<li>Registers the endpoints and interfaces with the RPC endpoint mapper.</li>
</ul>


<b>RpcServerInterfaceGroupActivate</b> is atomic.  If at any point the operation fails, any items that were previously registered are undone.  

Calls may be dispatched to the server application before this function returns.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupclose">RpcServerInterfaceGroupClose</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupdeactivate">RpcServerInterfaceGroupDeactivate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupinqbindings">RpcServerInterfaceGroupInqBindings</a>