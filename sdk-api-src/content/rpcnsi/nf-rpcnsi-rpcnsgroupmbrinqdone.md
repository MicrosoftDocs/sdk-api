---
UID: NF:rpcnsi.RpcNsGroupMbrInqDone
title: RpcNsGroupMbrInqDone function (rpcnsi.h)
description: The RpcNsGroupMbrInqDone function deletes the inquiry context for a group.
helpviewer_keywords: ["RpcNsGroupMbrInqDone","RpcNsGroupMbrInqDone function [RPC]","_rpc_rpcnsgroupmbrinqdone","rpc.rpcnsgroupmbrinqdone","rpcnsi/RpcNsGroupMbrInqDone"]
old-location: rpc\rpcnsgroupmbrinqdone.htm
tech.root: Rpc
ms.assetid: fe40be4d-1468-429a-aa20-694467076bde
ms.date: 12/05/2018
ms.keywords: RpcNsGroupMbrInqDone, RpcNsGroupMbrInqDone function [RPC], _rpc_rpcnsgroupmbrinqdone, rpc.rpcnsgroupmbrinqdone, rpcnsi/RpcNsGroupMbrInqDone
req.header: rpcnsi.h
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
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNsGroupMbrInqDone
 - rpcnsi/RpcNsGroupMbrInqDone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsGroupMbrInqDone
---

# RpcNsGroupMbrInqDone function


## -description

The 
<b>RpcNsGroupMbrInqDone</b> function deletes the inquiry context for a group.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param InquiryContext

Pointer to a name-service handle to free. A value of NULL is returned.

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
<dt><b>RPC_S_INVALID_NS_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The name-service handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsGroupMbrInqDone</b> function frees an inquiry context created by calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqbegina">RpcNsGroupMbrInqBegin</a> function. An application calls 
<b>RpcNsGroupMbrInqDone</b> after viewing RPC group members using the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqnexta">RpcNsGroupMbrInqNext</a> function.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqbegina">RpcNsGroupMbrInqBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqnexta">RpcNsGroupMbrInqNext</a>