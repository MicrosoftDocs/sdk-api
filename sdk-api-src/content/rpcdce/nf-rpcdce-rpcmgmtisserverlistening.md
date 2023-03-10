---
UID: NF:rpcdce.RpcMgmtIsServerListening
title: RpcMgmtIsServerListening function (rpcdce.h)
description: The RpcMgmtIsServerListening function tells whether a server is listening for remote procedure calls.
helpviewer_keywords: ["RpcMgmtIsServerListening","RpcMgmtIsServerListening function [RPC]","_rpc_rpcmgmtisserverlistening","rpc.rpcmgmtisserverlistening","rpcdce/RpcMgmtIsServerListening"]
old-location: rpc\rpcmgmtisserverlistening.htm
tech.root: Rpc
ms.assetid: e4c5e8aa-764d-489f-ac98-ab40ca4a3534
ms.date: 12/05/2018
ms.keywords: RpcMgmtIsServerListening, RpcMgmtIsServerListening function [RPC], _rpc_rpcmgmtisserverlistening, rpc.rpcmgmtisserverlistening, rpcdce/RpcMgmtIsServerListening
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - RpcMgmtIsServerListening
 - rpcdce/RpcMgmtIsServerListening
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
 - RpcMgmtIsServerListening
---

# RpcMgmtIsServerListening function


## -description

The 
<b>RpcMgmtIsServerListening</b> function tells whether a server is listening for remote procedure calls.

## -parameters

### -param Binding

To determine whether a remote application is listening for remote procedure calls, specify a server binding handle for that application. To determine whether your own (local) application is listening for remote procedure calls, specify a value of <b>NULL</b>.

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
Server listening for remote procedure calls.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NOT_LISTENING</b></dt>
</dl>
</td>
<td width="60%">
Server not listening for remote procedure calls, or the interface is auto-listening.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

<div> </div>


The 
<b>RpcMgmtIsServerListening</b> function returns correct results only for interfaces that are not auto-listening. If the server application is auto-listening and calls the 
<b>RpcMgmtIsServerListening</b> function, 
<b>RpcMgmtIsServerListening</b> returns RPC_SERVER_NOT_LISTENING, yet the server may be listening, and subsequent RPC calls may succeed.

## -remarks

An application calls the 
<b>RpcMgmtIsServerListening</b> function to determine whether the server specified in the <i>Binding</i> parameter is listening for remote procedure calls.

The 
<b>RpcMgmtIsServerListening</b> function returns a value of <b>RPC_S_OK</b> if the server has called 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a>.

The server must be listening for remote procedure calls for this function to succeed.  If the server is not listening, the function fails.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepresolvebinding">RpcEpResolveBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a>