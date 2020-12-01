---
UID: NF:rpcdce.RpcMgmtSetAuthorizationFn
title: RpcMgmtSetAuthorizationFn function (rpcdce.h)
description: The RpcMgmtSetAuthorizationFn function establishes an authorization function for processing remote calls to a server's management functions.
helpviewer_keywords: ["RpcMgmtSetAuthorizationFn","RpcMgmtSetAuthorizationFn function [RPC]","_rpc_rpcmgmtsetauthorizationfn","rpc.rpcmgmtsetauthorizationfn","rpcdce/RpcMgmtSetAuthorizationFn"]
old-location: rpc\rpcmgmtsetauthorizationfn.htm
tech.root: Rpc
ms.assetid: bb381a52-17e4-4ebe-9a1a-a561c12d73d4
ms.date: 12/05/2018
ms.keywords: RpcMgmtSetAuthorizationFn, RpcMgmtSetAuthorizationFn function [RPC], _rpc_rpcmgmtsetauthorizationfn, rpc.rpcmgmtsetauthorizationfn, rpcdce/RpcMgmtSetAuthorizationFn
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
 - RpcMgmtSetAuthorizationFn
 - rpcdce/RpcMgmtSetAuthorizationFn
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
 - RpcMgmtSetAuthorizationFn
---

# RpcMgmtSetAuthorizationFn function


## -description

The 
<b>RpcMgmtSetAuthorizationFn</b> function establishes an authorization function for processing remote calls to a server's management functions.

## -parameters

### -param AuthorizationFn

Specifies an authorization function. The RPC server run-time library automatically calls this function whenever the server run-time receives a client request to execute one of the remote management functions. The server must implement this function. Applications specify a value of <b>NULL</b> to unregister a previously registered authorization function. After such a call, default authorizations are used.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

Server applications call the 
<b>RpcMgmtSetAuthorizationFn</b> function to establish an authorization function that controls access to the server's remote management functions. When a server has not called 
<b>RpcMgmtSetAuthorizationFn</b>, or calls with a <b>null</b> value for <i>AuthorizationFn</i>, the server run-time library uses the following default authorizations.

<table>
<tr>
<th>Remote function</th>
<th>Default authorization</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqifids">RpcMgmtInqIfIds</a>
</td>
<td>Enabled</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqserverprincname">RpcMgmtInqServerPrincName</a>
</td>
<td>Enabled</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqstats">RpcMgmtInqStats</a>
</td>
<td>Enabled</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtisserverlistening">RpcMgmtIsServerListening</a>
</td>
<td>Enabled</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstopserverlistening">RpcMgmtStopServerListening</a>
</td>
<td>Disabled</td>
</tr>
</table>
 


<div> </div>


In the preceding table, "Enabled" indicates that all clients can execute the remote function, and "Disabled" indicates that all clients are prevented from executing the remote function.

## -see-also

<a href="/windows/desktop/api/rpcdce/nc-rpcdce-rpc_mgmt_authorization_fn">RPC_MGMT_AUTHORIZATION_FN</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqstats">RpcMgmtInqStats</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtisserverlistening">RpcMgmtIsServerListening</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstopserverlistening">RpcMgmtStopServerListening</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten">RpcMgmtWaitServerListen</a>