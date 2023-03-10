---
UID: NF:rpcdce.RpcMgmtStatsVectorFree
title: RpcMgmtStatsVectorFree function (rpcdce.h)
description: The RpcMgmtStatsVectorFree function frees a statistics vector.
helpviewer_keywords: ["RpcMgmtStatsVectorFree","RpcMgmtStatsVectorFree function [RPC]","_rpc_rpcmgmtstatsvectorfree","rpc.rpcmgmtstatsvectorfree","rpcdce/RpcMgmtStatsVectorFree"]
old-location: rpc\rpcmgmtstatsvectorfree.htm
tech.root: Rpc
ms.assetid: 0dc98053-8599-4884-a56a-5889a4480dcb
ms.date: 12/05/2018
ms.keywords: RpcMgmtStatsVectorFree, RpcMgmtStatsVectorFree function [RPC], _rpc_rpcmgmtstatsvectorfree, rpc.rpcmgmtstatsvectorfree, rpcdce/RpcMgmtStatsVectorFree
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
 - RpcMgmtStatsVectorFree
 - rpcdce/RpcMgmtStatsVectorFree
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
 - RpcMgmtStatsVectorFree
---

# RpcMgmtStatsVectorFree function


## -description

The 
<b>RpcMgmtStatsVectorFree</b> function frees a statistics vector.

## -parameters

### -param StatsVector

Pointer to a pointer to a statistics vector. On return, the pointer is set to <b>NULL</b>.

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

An application calls the 
<b>RpcMgmtStatsVectorFree</b> function to release the memory used to store statistics.

An application obtains a vector of statistics by calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqstats">RpcMgmtInqStats</a> function.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqstats">RpcMgmtInqStats</a>