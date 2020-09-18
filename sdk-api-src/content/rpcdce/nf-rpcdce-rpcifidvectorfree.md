---
UID: NF:rpcdce.RpcIfIdVectorFree
title: RpcIfIdVectorFree function (rpcdce.h)
description: The RpcIfIdVectorFree function frees the vector and the interface-identification structures contained in the vector.
helpviewer_keywords: ["RpcIfIdVectorFree","RpcIfIdVectorFree function [RPC]","_rpc_rpcifidvectorfree","rpc.rpcifidvectorfree","rpcdce/RpcIfIdVectorFree"]
old-location: rpc\rpcifidvectorfree.htm
tech.root: Rpc
ms.assetid: 1af518a7-02db-438a-ba3f-723bd8422188
ms.date: 12/05/2018
ms.keywords: RpcIfIdVectorFree, RpcIfIdVectorFree function [RPC], _rpc_rpcifidvectorfree, rpc.rpcifidvectorfree, rpcdce/RpcIfIdVectorFree
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
 - RpcIfIdVectorFree
 - rpcdce/RpcIfIdVectorFree
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
 - RpcIfIdVectorFree
---

# RpcIfIdVectorFree function


## -description

The 
<b>RpcIfIdVectorFree</b> function frees the vector and the interface-identification structures contained in the vector.

## -parameters

### -param IfIdVector

Address of a pointer to a vector of interface information. On return, the pointer is set to <b>NULL</b>.

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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls the 
<b>RpcIfIdVectorFree</b> function to release the memory used to store a vector of interface identifications. 
<b>RpcIfIdVectorFree</b> frees memory containing the interface identifications and the vector itself. On return, this function sets the <i>IfIdVec</i> parameter to <b>NULL</b>.

An application obtains a vector of interface identifications by calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtentryinqifidsa">RpcNsMgmtEntryInqIfIds</a> and 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqifids">RpcMgmtInqIfIds</a> functions.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifinqid">RpcIfInqId</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqifids">RpcMgmtInqIfIds</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtentryinqifidsa">RpcNsMgmtEntryInqIfIds</a>