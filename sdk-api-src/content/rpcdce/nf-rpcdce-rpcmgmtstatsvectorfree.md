---
UID: NF:rpcdce.RpcMgmtStatsVectorFree
title: RpcMgmtStatsVectorFree function
author: windows-sdk-content
description: The RpcMgmtStatsVectorFree function frees a statistics vector.
old-location: rpc\rpcmgmtstatsvectorfree.htm
tech.root: rpc
ms.assetid: 0dc98053-8599-4884-a56a-5889a4480dcb
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: RpcMgmtStatsVectorFree, RpcMgmtStatsVectorFree function [RPC], _rpc_rpcmgmtstatsvectorfree, rpc.rpcmgmtstatsvectorfree, rpcdce/RpcMgmtStatsVectorFree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcMgmtStatsVectorFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls the 
<b>RpcMgmtStatsVectorFree</b> function to release the memory used to store statistics.

An application obtains a vector of statistics by calling the 
<a href="https://msdn.microsoft.com/478b9f33-db01-4a1d-9b5b-dc2662ee8d7b">RpcMgmtInqStats</a> function.




## -see-also




<a href="https://msdn.microsoft.com/478b9f33-db01-4a1d-9b5b-dc2662ee8d7b">RpcMgmtInqStats</a>
 

 

