---
UID: NF:rpcdce.RpcMgmtWaitServerListen
title: RpcMgmtWaitServerListen function (rpcdce.h)
description: The RpcMgmtWaitServerListen function performs the wait operation usually associated with RpcServerListen.
helpviewer_keywords: ["RpcMgmtWaitServerListen","RpcMgmtWaitServerListen function [RPC]","_rpc_rpcmgmtwaitserverlisten","rpc.rpcmgmtwaitserverlisten","rpcdce/RpcMgmtWaitServerListen"]
old-location: rpc\rpcmgmtwaitserverlisten.htm
tech.root: Rpc
ms.assetid: 19fa750f-76f8-4005-992f-9c2707e48668
ms.date: 12/05/2018
ms.keywords: RpcMgmtWaitServerListen, RpcMgmtWaitServerListen function [RPC], _rpc_rpcmgmtwaitserverlisten, rpc.rpcmgmtwaitserverlisten, rpcdce/RpcMgmtWaitServerListen
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
 - RpcMgmtWaitServerListen
 - rpcdce/RpcMgmtWaitServerListen
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
 - RpcMgmtWaitServerListen
---

# RpcMgmtWaitServerListen function


## -description

The 
<b>RpcMgmtWaitServerListen</b> function performs the <i>wait</i> operation usually associated with 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a>.



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
All remote procedure calls are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_ALREADY_LISTENING</b></dt>
</dl>
</td>
<td width="60%">
Another thread has called 
<b>RpcMgmtWaitServerListen</b> and has not yet returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NOT_LISTENING</b></dt>
</dl>
</td>
<td width="60%">
The server application must call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a> before calling 
<b>RpcMgmtWaitServerListen</b>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

When the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a> flag parameter <i>DontWait</i> has a nonzero value, the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a> function returns to the server application without performing the wait operation. In this case, the wait can be performed by 
<b>RpcMgmtWaitServerListen</b>.

Applications must call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a> with a nonzero value for the <i>DontWait</i> parameter before calling 
<b>RpcMgmtWaitServerListen</b>. The 
<b>RpcMgmtWaitServerListen</b> function returns after the server application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstopserverlistening">RpcMgmtStopServerListening</a> and all active remote procedure calls complete, or after a fatal error occurs in the RPC run-time library.

<div class="alert"><b>Note</b>  <b>RpcMgmtWaitServerListen</b> is a Microsoft extension to the DCE API set.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstopserverlistening">RpcMgmtStopServerListening</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a>
