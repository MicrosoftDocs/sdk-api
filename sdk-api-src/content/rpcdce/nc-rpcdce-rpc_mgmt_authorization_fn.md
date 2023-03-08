---
UID: NC:rpcdce.RPC_MGMT_AUTHORIZATION_FN
title: RPC_MGMT_AUTHORIZATION_FN (rpcdce.h)
description: The RPC_MGMT_AUTHORIZATION_FN enables server programs to implement custom RPC authorization techniques.
helpviewer_keywords: ["RPC_MGMT_AUTHORIZATION_FN","RPC_MGMT_AUTHORIZATION_FN callback","RPC_MGMT_AUTHORIZATION_FN callback function [RPC]","RpcMgmtInqIfIds","RpcMgmtInqServerPrincName","RpcMgmtInqStats","RpcMgmtIsServerListening","RpcMgmtStopServerListening","_rpc_rpc_mgmt_authorization_fn","rpc.rpc_mgmt_authorization_fn","rpcdce/RPC_MGMT_AUTHORIZATION_FN"]
old-location: rpc\rpc_mgmt_authorization_fn.htm
tech.root: Rpc
ms.assetid: 9b7ab901-1dcf-458c-858f-f411825f324b
ms.date: 12/05/2018
ms.keywords: RPC_MGMT_AUTHORIZATION_FN, RPC_MGMT_AUTHORIZATION_FN callback, RPC_MGMT_AUTHORIZATION_FN callback function [RPC], RpcMgmtInqIfIds, RpcMgmtInqServerPrincName, RpcMgmtInqStats, RpcMgmtIsServerListening, RpcMgmtStopServerListening, _rpc_rpc_mgmt_authorization_fn, rpc.rpc_mgmt_authorization_fn, rpcdce/RPC_MGMT_AUTHORIZATION_FN
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RPC_MGMT_AUTHORIZATION_FN
 - rpcdce/RPC_MGMT_AUTHORIZATION_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rpcdce.h
api_name:
 - RPC_MGMT_AUTHORIZATION_FN
---

# RPC_MGMT_AUTHORIZATION_FN callback function


## -description

The 
<i>RPC_MGMT_AUTHORIZATION_FN</i> enables server programs to implement custom RPC authorization techniques.

## -parameters

### -param ClientBinding

Client/server binding handle.

### -param RequestedMgmtOperation

The value for <i>RequestedMgmtOperation</i> depends on the remote function requested, as shown in the following table. 



<table>
<tr>
<th>Called remote function</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RpcMgmtInqIfIds"></a><a id="rpcmgmtinqifids"></a><a id="RPCMGMTINQIFIDS"></a><dl>
<dt><b>RpcMgmtInqIfIds</b></dt>
</dl>
</td>
<td width="60%">
RPC_C_MGMT_INQ_IF_IDS

</td>
</tr>
<tr>
<td width="40%"><a id="RpcMgmtInqServerPrincName"></a><a id="rpcmgmtinqserverprincname"></a><a id="RPCMGMTINQSERVERPRINCNAME"></a><dl>
<dt><b>RpcMgmtInqServerPrincName</b></dt>
</dl>
</td>
<td width="60%">
RPC_C_MGMT_INQ_PRINC_NAME

</td>
</tr>
<tr>
<td width="40%"><a id="RpcMgmtInqStats"></a><a id="rpcmgmtinqstats"></a><a id="RPCMGMTINQSTATS"></a><dl>
<dt><b>RpcMgmtInqStats</b></dt>
</dl>
</td>
<td width="60%">
RPC_C_MGMT_INQ_STATS

</td>
</tr>
<tr>
<td width="40%"><a id="RpcMgmtIsServerListening"></a><a id="rpcmgmtisserverlistening"></a><a id="RPCMGMTISSERVERLISTENING"></a><dl>
<dt><b>RpcMgmtIsServerListening</b></dt>
</dl>
</td>
<td width="60%">
RPC_C_MGMT_IS_SERVER_LISTEN

</td>
</tr>
<tr>
<td width="40%"><a id="RpcMgmtStopServerListening"></a><a id="rpcmgmtstopserverlistening"></a><a id="RPCMGMTSTOPSERVERLISTENING"></a><dl>
<dt><b>RpcMgmtStopServerListening</b></dt>
</dl>
</td>
<td width="60%">
RPC_C_MGMT_STOP_SERVER_LISTEN

</td>
</tr>
</table>
 

The authorization function must handle all of these values.

### -param Status

If <i>Status</i> is either 0 (zero) or RPC_S_OK, the <i>Status</i> value RPC_S_ACCESS_DENIED is returned to the client by the remote management function. If the authorization function returns any other value for <i>Status</i>, that <i>Status</i> value is returned to the client by the remote management function.

## -returns

Returns <b>TRUE</b> if the calling client is allowed access to the requested management function. If the authorization function returns <b>FALSE</b>, the management function cannot execute. In this case, the function returns a <i>Status</i> value to the client:

## -remarks

When a client requests one of the server's remote management functions, the server run-time library calls the authorization function with <i>ClientBinding</i> and <i>RequestedMgmtOperation</i>. The authorization function uses these parameters to determine whether the calling client can execute the requested management function.

## -see-also

<a href="/windows/desktop/Rpc/authorization-functions">Authorization Functions</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn">RpcMgmtSetAuthorizationFn</a>
