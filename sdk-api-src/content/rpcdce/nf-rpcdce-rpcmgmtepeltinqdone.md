---
UID: NF:rpcdce.RpcMgmtEpEltInqDone
title: RpcMgmtEpEltInqDone function (rpcdce.h)
description: The RpcMgmtEpEltInqDone function deletes the inquiry context for viewing the elements in an endpoint map.
helpviewer_keywords: ["RpcMgmtEpEltInqDone","RpcMgmtEpEltInqDone function [RPC]","_rpc_rpcmgmtepeltinqdone","rpc.rpcmgmtepeltinqdone","rpcdce/RpcMgmtEpEltInqDone"]
old-location: rpc\rpcmgmtepeltinqdone.htm
tech.root: Rpc
ms.assetid: 7a0aac99-8829-4720-a388-da88d015d596
ms.date: 12/05/2018
ms.keywords: RpcMgmtEpEltInqDone, RpcMgmtEpEltInqDone function [RPC], _rpc_rpcmgmtepeltinqdone, rpc.rpcmgmtepeltinqdone, rpcdce/RpcMgmtEpEltInqDone
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
 - RpcMgmtEpEltInqDone
 - rpcdce/RpcMgmtEpEltInqDone
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
 - RpcMgmtEpEltInqDone
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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcMgmtEpEltInqDone</b> function deletes an inquiry context created by 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin">RpcMgmtEpEltInqBegin</a>. An application calls this function after viewing local endpoint-map elements using 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepeltinqnext">RpcMgmtEpEltInqNext</a>.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin">RpcMgmtEpEltInqBegin</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepeltinqnext">RpcMgmtEpEltInqNext</a>