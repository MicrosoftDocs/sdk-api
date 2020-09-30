---
UID: NF:rpcnsi.RpcNsBindingLookupNext
title: RpcNsBindingLookupNext function (rpcnsi.h)
description: The RpcNsBindingLookupNext function returns a list of compatible binding handles for a specified interface and optionally an object.
helpviewer_keywords: ["RpcNsBindingLookupNext","RpcNsBindingLookupNext function [RPC]","_rpc_rpcnsbindinglookupnext","rpc.rpcnsbindinglookupnext","rpcnsi/RpcNsBindingLookupNext"]
old-location: rpc\rpcnsbindinglookupnext.htm
tech.root: Rpc
ms.assetid: 068913fb-f9ca-4e03-93d7-3484ba43472e
ms.date: 12/05/2018
ms.keywords: RpcNsBindingLookupNext, RpcNsBindingLookupNext function [RPC], _rpc_rpcnsbindinglookupnext, rpc.rpcnsbindinglookupnext, rpcnsi/RpcNsBindingLookupNext
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
 - RpcNsBindingLookupNext
 - rpcnsi/RpcNsBindingLookupNext
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
 - RpcNsBindingLookupNext
---

# RpcNsBindingLookupNext function


## -description

The 
<b>RpcNsBindingLookupNext</b> function returns a list of compatible binding handles for a specified interface and optionally an object.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param LookupContext

Name-service handle returned from the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a> function.

### -param BindingVec

Returns the address of a pointer to a vector of client-compatible server binding handles.

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
<b>RpcNsBindingLookupNext</b> function returns a vector of client-compatible server binding handles for a server offering the interface and object UUID specified by the <i>IfSpec</i> and <i>ObjUuid</i> parameters in the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a> function. (Compare this to 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportnext">RpcNsBindingImportNext</a>, which returns a single compatible server binding handle.)

The 
<b>RpcNsBindingLookupNext</b> function communicates only with the name-service database, not directly with servers.

Effective with Windows 2000, the RPC environment uses Active Directory as its name-service database and the order in which the run-time environment performs the search is as follows:

<ul>
<li>Search the local cache.</li>
<li>If entry not found in local cache, search that machine's Active Directory.</li>
<li>If entry not found on local machine, send broadcast requests to all other Active Directory services in the domain. 


Note that if the entry exists in the Active Directory, but there is no information associated with the entry, the run-time environment will not issue this broadcast request.

</li>
</ul>
On successive calls, the 
<b>RpcNsBindingLookupNext</b> function traverses name-service database entries, collecting client-compatible server binding handles from each entry.

When  Microsoft Active Directory is the name-service database, 
<b>RpcNsBindingLookupNext</b> traverses the database only if the given entry name is <b>null</b> and the default entry (in the registry) is undefined or empty. Also, since mixed entries are not permitted in the Active Directory, the function searches for server entry names only, not group or profile names.

When the DCE Cell Directory Service (CDS) is the name-service database, and the entry at which the search begins contains binding handles in addition to group or profile names, 
<b>RpcNsBindingLookupNext</b> returns the binding handles from <i>EntryName</i> before searching the group or profile. This means that the function can return a partially full vector before processing the members of the group or profile.

The compatible binding handle that is returned always contains an object UUID, the value of which depends on the <i>ObjUuid</i> parameter in the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a> function. If a non-<b>null</b> object UUID was specified, the returned binding handle contains that object UUID. If, however, a <b>null</b> object UUID or <b>null</b> value was specified, the object UUID that is returned is a result of the following possibilities:

<ul>
<li>If the server did not export any object UUIDs, the returned binding handle contains a nil object UUID.</li>
<li>If the server exported one object UUID, the returned binding handle contains that object UUID.</li>
<li>If the server exported multiple object UUIDs, the returned binding handle contains one of the object UUIDs. The import-next operation selects the returned object UUID in a non-deterministic fashion. As a result, a different object UUID can be returned for each compatible binding handle from a single server entry.</li>
</ul>
From the returned vector of server binding handles, the client application can employ its own criteria for selecting individual binding handles, or the application can call the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingselect">RpcNsBindingSelect</a> function to select a binding handle. The 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingtostringbinding">RpcBindingToStringBinding</a> and 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingparse">RpcStringBindingParse</a> functions will be helpful to a client creating its own selection criteria.

The client application can use the selected binding handle to attempt to make a remote procedure call to the server. If the client fails to establish a relationship with the server, it can select another binding handle from the vector. When all of the binding handles in the vector have been used, the client application calls 
<b>RpcNsBindingLookupNext</b> again.

Each time the client calls 
<b>RpcNsBindingLookupNext</b>, the function returns another vector of binding handles. The binding handles returned in each vector are unordered. The vectors returned from multiple calls to this function are also unordered.

A client calls the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnsbindinginqentryname">RpcNsBindingInqEntryName</a> function to obtain the name-service database server entry name that the binding came from.

When the search reaches the end of the name-service database, 
<b>RpcNsBindingLookupNext</b> returns a status of RPC_S_NO_MORE_BINDINGS and returns a <i>BindingVec</i> value of <b>NULL</b>.

The 
<b>RpcNsBindingLookupNext</b> function allocates storage for the data referenced by the returned <i>BindingVec</i> parameter. When a client application finishes with the vector, it must call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingvectorfree">RpcBindingVectorFree</a> function to deallocate the storage. Each call to 
<b>RpcNsBindingLookupNext</b> requires a corresponding call to 
<b>RpcBindingVectorFree</b>.

The client is responsible for calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone">RpcNsBindingLookupDone</a> function to delete the lookup context, or if you want the application to start a new search for compatible servers.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingtostringbinding">RpcBindingToStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingvectorfree">RpcBindingVectorFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnsbindinginqentryname">RpcNsBindingInqEntryName</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone">RpcNsBindingLookupDone</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingparse">RpcStringBindingParse</a>