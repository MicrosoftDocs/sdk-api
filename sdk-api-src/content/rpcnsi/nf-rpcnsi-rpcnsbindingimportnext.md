---
UID: NF:rpcnsi.RpcNsBindingImportNext
title: RpcNsBindingImportNext function (rpcnsi.h)
description: The RpcNsBindingImportNext function looks up an interface (and optionally an object from a name-service database) and returns a binding handle of a compatible server, if found.
helpviewer_keywords: ["RpcNsBindingImportNext","RpcNsBindingImportNext function [RPC]","_rpc_rpcnsbindingimportnext","rpc.rpcnsbindingimportnext","rpcnsi/RpcNsBindingImportNext"]
old-location: rpc\rpcnsbindingimportnext.htm
tech.root: Rpc
ms.assetid: c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e
ms.date: 12/05/2018
ms.keywords: RpcNsBindingImportNext, RpcNsBindingImportNext function [RPC], _rpc_rpcnsbindingimportnext, rpc.rpcnsbindingimportnext, rpcnsi/RpcNsBindingImportNext
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
 - RpcNsBindingImportNext
 - rpcnsi/RpcNsBindingImportNext
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
 - RpcNsBindingImportNext
---

# RpcNsBindingImportNext function


## -description

The 
<b>RpcNsBindingImportNext</b> function looks up an interface (and optionally an object from a name-service database) and returns a binding handle of a compatible server, if found.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param ImportContext

Name-service handle returned from the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a> function.

### -param Binding

Returns a pointer to a client-compatible server binding handle for a server.

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
<dt><b>RPC_S_NO_MORE_BINDINGS</b></dt>
</dl>
</td>
<td width="60%">
No more bindings.

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
<b>RpcNsBindingImportNext</b> function returns one client-compatible server binding handle for a server that offers the interface and object UUID specified by the <i>IfSpec</i> and <i>ObjUuid</i> parameters in the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a> function. The function communicates only with the name-service database, not directly with servers.

Effective with Windows 2000, the RPC environment uses the Active Directory as its name-service database and the order in which the run-time environment performs the search is as follows:

<ul>
<li>Search in the local cache. If there is no entry,</li>
<li>Search in the Active Directory. If there is no entry,</li>
<li>Send broadcast requests to all other directory services in the domain. 


Note that if the entry exists in the Active Directory, but there is no information associated with the entry, the run-time environment does not issue this broadcast request.

</li>
</ul>
The compatible binding handle that is returned always contains an object UUID, the value of which depends on the <i>ObjUuid</i> parameter in the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a> function. If a non-<b>null</b> object UUID was specified, the returned binding handle contains that object UUID. If, however, a <b>null</b> object UUID or <b>null</b> value was specified, the object UUID that is returned is a result of the following possibilities:

<ul>
<li>If the server did not export any object UUIDs, the returned binding handle contains a nil object UUID.</li>
<li>If the server exported one object UUID, the returned binding handle contains that object UUID.</li>
<li>If the server exported multiple object UUIDs, the returned binding handle contains one of the object UUIDs. The import-next operation selects the returned object UUID in a non-deterministic fashion. As a result, a different object UUID can be returned for each compatible binding handle from a single server entry.</li>
</ul>
The 
<b>RpcNsBindingImportNext</b> function selects and returns one server binding handle from the compatible binding handles found. The client application can use that binding handle to attempt a remote procedure call to the server. If the client fails to establish a relationship with the server, it can call 
<b>RpcNsBindingImportNext</b> again.

Each time the client calls 
<b>RpcNsBindingImportNext</b>, the function returns another server binding handle. The returned binding handles are unordered. A client application calls the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnsbindinginqentryname">RpcNsBindingInqEntryName</a> function to obtain the name-service database in the entry name from which the binding handle came.When the search reaches the end of the name-service database, 
<b>RpcNsBindingInqEntryName</b> returns a status of RPC_S_NO_MORE_BINDINGS and returns a binding parameter value of <b>NULL</b>.

The 
<b>RpcNsBindingImportNext</b> function allocates storage for the data referenced by the returned <i>Binding</i> parameter. When a client application finishes with the binding handle, it must call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a> to deallocate the storage. Each call to 
<b>RpcNsBindingImportNext</b> requires a corresponding call to 
<b>RpcBindingFree</b>.

The client is responsible for calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportdone">RpcNsBindingImportDone</a> function, which deletes the import context. The client also calls 
<b>RpcNsBindingImportDone</b> before calling 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a> to start a new search for compatible servers. Because the order of binding handles returned is different for each new search, the order in which binding handles are returned to an application can be different each time the application is run.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportdone">RpcNsBindingImportDone</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnsbindinginqentryname">RpcNsBindingInqEntryName</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone">RpcNsBindingLookupDone</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingselect">RpcNsBindingSelect</a>