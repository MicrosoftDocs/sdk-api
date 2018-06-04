---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
<a href="https://msdn.microsoft.com/478b9f33-db01-4a1d-9b5b-dc2662ee8d7b">RpcMgmtInqStats</a>. The RPC run-time library allocates memory for the statistics vector. The application calls 
<a href="https://msdn.microsoft.com/0dc98053-8599-4884-a56a-5889a4480dcb">RpcMgmtStatsVectorFree</a> to free the statistics vector.




## -see-also




<a href="https://msdn.microsoft.com/478b9f33-db01-4a1d-9b5b-dc2662ee8d7b">RpcMgmtInqStats</a>



<a href="https://msdn.microsoft.com/0dc98053-8599-4884-a56a-5889a4480dcb">RpcMgmtStatsVectorFree</a>
 

 

