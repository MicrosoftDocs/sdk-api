---
UID: NF:rpcdce.RpcMgmtInqStats
title: RpcMgmtInqStats function (rpcdce.h)
description: The RpcMgmtInqStats function returns RPC run-time statistics.
helpviewer_keywords: ["RpcMgmtInqStats","RpcMgmtInqStats function [RPC]","_rpc_rpcmgmtinqstats","rpc.rpcmgmtinqstats","rpcdce/RpcMgmtInqStats"]
old-location: rpc\rpcmgmtinqstats.htm
tech.root: Rpc
ms.assetid: 478b9f33-db01-4a1d-9b5b-dc2662ee8d7b
ms.date: 12/05/2018
ms.keywords: RpcMgmtInqStats, RpcMgmtInqStats function [RPC], _rpc_rpcmgmtinqstats, rpc.rpcmgmtinqstats, rpcdce/RpcMgmtInqStats
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
 - RpcMgmtInqStats
 - rpcdce/RpcMgmtInqStats
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
 - RpcMgmtInqStats
---

# RpcMgmtInqStats function


## -description

The 
<b>RpcMgmtInqStats</b> function returns RPC run-time statistics.

## -parameters

### -param Binding

To receive statistics about a remote application, specify a server binding handle for that application. To receive statistics about your own (local) application, specify a value of <b>NULL</b>.

### -param Statistics

Returns a pointer to a pointer to the statistics about the server specified by the <i>Binding</i> parameter. Each statistic is an <b>unsigned long</b> value.

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
<b>RpcMgmtInqStats</b> function to obtain statistics about the specified server from the RPC run-time library.

Each array element in the returned statistics vector contains an <b>unsigned long</b> value. The following table describes the statistics indexed by the specified constant.

<table>
<tr>
<th>Statistic</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_C_STATS_CALLS_IN</td>
<td>Number of remote procedure calls received by the RPC server specified by the binding handle.</td>
</tr>
<tr>
<td>RPC_C_STATS_CALLS_OUT</td>
<td>Number of remote procedure calls initiated by the RPC server specified by the binding handle.</td>
</tr>
<tr>
<td>RPC_C_STATS_PKTS_IN</td>
<td>Number of network packets received by the RPC server specified by the binding handle.</td>
</tr>
<tr>
<td>RPC_C_STATS_PKTS_OUT</td>
<td>Number of network packets sent by the RPC server specified by the binding handle.</td>
</tr>
</table>
 


<div> </div>


The RPC run-time library allocates memory for the statistics vector. The application is responsible for calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstatsvectorfree">RpcMgmtStatsVectorFree</a> function to release the memory used by the statistics vector.

The server must be listening for remote procedure calls for this function to succeed.  If the server is not listening, the function fails.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepresolvebinding">RpcEpResolveBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstatsvectorfree">RpcMgmtStatsVectorFree</a>