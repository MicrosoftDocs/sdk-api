---
UID: NF:rpcnsi.RpcNsEntryObjectInqNext
title: RpcNsEntryObjectInqNext function (rpcnsi.h)
description: The RpcNsEntryObjectInqNext function returns one object at a time from a name-service database entry.
helpviewer_keywords: ["RpcNsEntryObjectInqNext","RpcNsEntryObjectInqNext function [RPC]","_rpc_rpcnsentryobjectinqnext","rpc.rpcnsentryobjectinqnext","rpcnsi/RpcNsEntryObjectInqNext"]
old-location: rpc\rpcnsentryobjectinqnext.htm
tech.root: Rpc
ms.assetid: 95648480-5b53-4a8c-ba82-6c7f204520d2
ms.date: 12/05/2018
ms.keywords: RpcNsEntryObjectInqNext, RpcNsEntryObjectInqNext function [RPC], _rpc_rpcnsentryobjectinqnext, rpc.rpcnsentryobjectinqnext, rpcnsi/RpcNsEntryObjectInqNext
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
 - RpcNsEntryObjectInqNext
 - rpcnsi/RpcNsEntryObjectInqNext
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
 - RpcNsEntryObjectInqNext
---

# RpcNsEntryObjectInqNext function


## -description

The 
<b>RpcNsEntryObjectInqNext</b> function returns one object at a time from a name-service database entry.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param InquiryContext

Name-service handle that indicates the object UUIDs for a name-service database entry.

### -param ObjUuid

Returns a pointer to an exported object UUID.

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
<dt><b>RPC_S_NO_MORE_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
No more members.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INCOMPLETE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is incomplete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_ENTRY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The name-service entry was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NAME_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The name service is unavailable.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsEntryObjectInqNext</b> function returns one of the object UUIDs exported to the name-service database entry specified by the <i>EntryName</i> parameter in the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsentryobjectinqbegina">RpcNsEntryObjectInqBegin</a> function.

An application can view all of the exported object UUIDs by repeatedly calling 
<b>RpcNsEntryObjectInqNext</b>. When all the object UUIDs have been viewed, this function returns an RPC_S_NO_MORE_MEMBERS status code. The returned object UUIDs are unordered.

The application supplies the memory for the object UUID returned in the <i>ObjUuid</i> parameter.

After viewing the object UUIDs, the application must call the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsentryobjectinqdone">RpcNsEntryObjectInqDone</a> function to release the inquiry context.

The order in which object UUIDs are returned can be different for each viewing of an entry. This means that the order in which object UUIDs are returned to an application can be different each time the application is run.

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsentryobjectinqbegina">RpcNsEntryObjectInqBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsentryobjectinqdone">RpcNsEntryObjectInqDone</a>