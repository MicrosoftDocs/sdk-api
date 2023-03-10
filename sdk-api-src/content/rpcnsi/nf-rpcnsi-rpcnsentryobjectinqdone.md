---
UID: NF:rpcnsi.RpcNsEntryObjectInqDone
title: RpcNsEntryObjectInqDone function (rpcnsi.h)
description: The RpcNsEntryObjectInqDone function deletes the inquiry context for a name-service database entry's objects.
helpviewer_keywords: ["RpcNsEntryObjectInqDone","RpcNsEntryObjectInqDone function [RPC]","_rpc_rpcnsentryobjectinqdone","rpc.rpcnsentryobjectinqdone","rpcnsi/RpcNsEntryObjectInqDone"]
old-location: rpc\rpcnsentryobjectinqdone.htm
tech.root: Rpc
ms.assetid: de1ed214-1018-498a-81a9-7932d4eead0b
ms.date: 12/05/2018
ms.keywords: RpcNsEntryObjectInqDone, RpcNsEntryObjectInqDone function [RPC], _rpc_rpcnsentryobjectinqdone, rpc.rpcnsentryobjectinqdone, rpcnsi/RpcNsEntryObjectInqDone
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
 - RpcNsEntryObjectInqDone
 - rpcnsi/RpcNsEntryObjectInqDone
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
 - RpcNsEntryObjectInqDone
---

# RpcNsEntryObjectInqDone function


## -description

The 
<b>RpcNsEntryObjectInqDone</b> function deletes the inquiry context for a name-service database entry's objects.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param InquiryContext

Pointer to a name-service handle specifying the object UUIDs exported to the <i>EntryName</i> parameter specified in the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsentryobjectinqbegina">RpcNsEntryObjectInqBegin</a> function. 




An argument value of <b>NULL</b> is returned.

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
<b>RpcNsEntryObjectInqDone</b> function frees an inquiry context created by calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsentryobjectinqbegina">RpcNsEntryObjectInqBegin</a> function.

An application calls 
<b>RpcNsEntryObjectInqDone</b> after viewing exported object UUIDs using the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsentryobjectinqnext">RpcNsEntryObjectInqNext</a> function.

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsentryobjectinqbegina">RpcNsEntryObjectInqBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsentryobjectinqnext">RpcNsEntryObjectInqNext</a>