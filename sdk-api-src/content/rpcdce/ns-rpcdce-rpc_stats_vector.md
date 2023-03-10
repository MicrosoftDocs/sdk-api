---
UID: NS:rpcdce.RPC_STATS_VECTOR
title: RPC_STATS_VECTOR (rpcdce.h)
description: The RPC_STATS_VECTOR structure contains statistics from the RPC run-time library on a per-server basis.
helpviewer_keywords: ["RPC_C_STATS_CALLS_IN","RPC_C_STATS_CALLS_OUT","RPC_C_STATS_PKTS_IN","RPC_C_STATS_PKTS_OUT","RPC_STATS_VECTOR","RPC_STATS_VECTOR structure [RPC]","_rpc_rpc_stats_vector","rpc.rpc_stats_vector","rpcdce/RPC_STATS_VECTOR"]
old-location: rpc\rpc_stats_vector.htm
tech.root: Rpc
ms.assetid: f2d959a5-530c-4534-9095-ec1a177ead99
ms.date: 12/05/2018
ms.keywords: RPC_C_STATS_CALLS_IN, RPC_C_STATS_CALLS_OUT, RPC_C_STATS_PKTS_IN, RPC_C_STATS_PKTS_OUT, RPC_STATS_VECTOR, RPC_STATS_VECTOR structure [RPC], _rpc_rpc_stats_vector, rpc.rpc_stats_vector, rpcdce/RPC_STATS_VECTOR
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_STATS_VECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RPC_STATS_VECTOR
 - rpcdce/RPC_STATS_VECTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_STATS_VECTOR
---

# RPC_STATS_VECTOR structure


## -description

The 
<b>RPC_STATS_VECTOR</b> structure contains statistics from the RPC run-time library on a per-server basis.

## -struct-fields

### -field Count

Number of statistics values present in the array <b>Stats</b>.

### -field Stats

Array of unsigned long integers representing server statistics that contains <b>Count</b> elements. Each array element contains an unsigned long value from the following list. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_STATS_CALLS_IN"></a><a id="rpc_c_stats_calls_in"></a><dl>
<dt><b>RPC_C_STATS_CALLS_IN</b></dt>
</dl>
</td>
<td width="60%">
The number of remote procedure calls received by the server.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_STATS_CALLS_OUT"></a><a id="rpc_c_stats_calls_out"></a><dl>
<dt><b>RPC_C_STATS_CALLS_OUT</b></dt>
</dl>
</td>
<td width="60%">
The number of remote procedure calls initiated by the server.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_STATS_PKTS_IN"></a><a id="rpc_c_stats_pkts_in"></a><dl>
<dt><b>RPC_C_STATS_PKTS_IN</b></dt>
</dl>
</td>
<td width="60%">
The number of network packets received by the server.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_STATS_PKTS_OUT"></a><a id="rpc_c_stats_pkts_out"></a><dl>
<dt><b>RPC_C_STATS_PKTS_OUT</b></dt>
</dl>
</td>
<td width="60%">
The number of network packets sent by the server.

</td>
</tr>
</table>

## -remarks

The statistics vector contains a count member (<b>Count</b>), followed by an array of statistics. To obtain run-time statistics, an application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqstats">RpcMgmtInqStats</a>. The RPC run-time library allocates memory for the statistics vector. The application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstatsvectorfree">RpcMgmtStatsVectorFree</a> to free the statistics vector.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqstats">RpcMgmtInqStats</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtstatsvectorfree">RpcMgmtStatsVectorFree</a>

