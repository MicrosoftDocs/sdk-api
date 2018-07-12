---
UID: NF:rpcdce.RpcMgmtEpEltInqDone
title: RpcMgmtEpEltInqDone function
author: windows-sdk-content
description: The RpcMgmtEpEltInqDone function deletes the inquiry context for viewing the elements in an endpoint map.
old-location: rpc\rpcmgmtepeltinqdone.htm
old-project: rpc
ms.assetid: 7a0aac99-8829-4720-a388-da88d015d596
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: RpcMgmtEpEltInqDone, RpcMgmtEpEltInqDone function [RPC], _rpc_rpcmgmtepeltinqdone, rpc.rpcmgmtepeltinqdone, rpcdce/RpcMgmtEpEltInqDone
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcMgmtEpEltInqDone
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcMgmtEpEltInqDone function


## -description


The 
<b>RpcMgmtEpEltInqDone</b> function deletes the inquiry context for viewing the elements in an endpoint map.


## -parameters




### -param InquiryContext

Inquiry context to delete and returns the value <b>NULL</b>.


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



The 
<b>RpcMgmtEpEltInqDone</b> function deletes an inquiry context created by 
<a href="https://msdn.microsoft.com/659ab657-e17f-46a9-942e-aa2631c1716d">RpcMgmtEpEltInqBegin</a>. An application calls this function after viewing local endpoint-map elements using 
<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a>.




## -see-also




<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/659ab657-e17f-46a9-942e-aa2631c1716d">RpcMgmtEpEltInqBegin</a>



<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a>
 

 

