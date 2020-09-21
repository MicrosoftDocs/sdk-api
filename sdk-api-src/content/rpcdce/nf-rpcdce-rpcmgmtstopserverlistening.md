---
UID: NF:rpcdce.RpcMgmtStopServerListening
title: RpcMgmtStopServerListening function (rpcdce.h)
description: The RpcMgmtStopServerListening function tells a server to stop listening for remote procedure calls. This function will not affect auto-listen interfaces. See RpcServerRegisterIfEx for more details.
helpviewer_keywords: ["RpcMgmtStopServerListening","RpcMgmtStopServerListening function [RPC]","_rpc_rpcmgmtstopserverlistening","rpc.rpcmgmtstopserverlistening","rpcdce/RpcMgmtStopServerListening"]
old-location: rpc\rpcmgmtstopserverlistening.htm
tech.root: Rpc
ms.assetid: aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84
ms.date: 12/05/2018
ms.keywords: RpcMgmtStopServerListening, RpcMgmtStopServerListening function [RPC], _rpc_rpcmgmtstopserverlistening, rpc.rpcmgmtstopserverlistening, rpcdce/RpcMgmtStopServerListening
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
 - RpcMgmtStopServerListening
 - rpcdce/RpcMgmtStopServerListening
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
 - RpcMgmtStopServerListening
---

# RpcMgmtStopServerListening function


## -description

The 
<b>RpcMgmtStopServerListening</b> function tells a server to stop listening for remote procedure calls. This function will not affect auto-listen interfaces. See 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex">RpcServerRegisterIfEx</a> for more details.

## -parameters

### -param Binding

To direct a remote application to stop listening for remote procedure calls, specify a server binding handle for that application. To direct your own (local) application to stop listening for remote procedure calls, specify a value of <b>NULL</b>.

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

## -remarks

An application calls the 
<b>RpcMgmtStopServerListening</b> function to direct a server to stop listening for remote procedure calls. If <i>DontWait</i> was <b>TRUE</b>, the application should call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten">RpcMgmtWaitServerListen</a> to wait for all calls to complete.

When it receives a stop-listening request, the RPC run-time library stops accepting new remote procedure calls for all registered interfaces. Executing calls are allowed to complete, including callbacks. After all calls complete, this function signals <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a> function that it must stop listening and return to the caller. If the <i>DontWait</i> parameter of <b>RpcServerListen</b> was set to <b>TRUE</b>, the application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten">RpcMgmtWaitServerListen</a> for all remaining calls to complete.

<div class="alert"><b>Note</b>  From the client-side, 
<b>RpcMgmtStopServerListening</b> is disabled by default. To enable this function, create an authorization function in your server application that returns <b>TRUE</b> (to allow a remote shutdown) whenever 
<b>RpcMgmtStopServerListening</b> is called. Use 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn">RpcMgmtSetAuthorizationFn</a> to give the client access to the management function.</div>
<div> </div>
The server must be listening for remote procedure calls for this function to succeed.  If the server is not listening, the function fails.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepresolvebinding">RpcEpResolveBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten">RpcMgmtWaitServerListen</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex">RpcServerRegisterIfEx</a>