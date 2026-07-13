---
UID: NF:rpcnsi.RpcNsBindingLookupBeginW
title: RpcNsBindingLookupBeginW function (rpcnsi.h)
description: The RpcNsBindingLookupBegin function creates a lookup context for an interface and an object. (Unicode)
helpviewer_keywords: ["RpcNsBindingLookupBegin", "RpcNsBindingLookupBegin function [RPC]", "RpcNsBindingLookupBeginW", "_rpc_rpcnsbindinglookupbegin", "rpc.rpcnsbindinglookupbegin", "rpcnsi/RpcNsBindingLookupBegin", "rpcnsi/RpcNsBindingLookupBeginW"]
old-location: rpc\rpcnsbindinglookupbegin.htm
tech.root: Rpc
ms.assetid: 75b7e901-706a-4e3d-b958-d04a0709b993
ms.date: 12/05/2018
ms.keywords: RpcNsBindingLookupBegin, RpcNsBindingLookupBegin function [RPC], RpcNsBindingLookupBeginA, RpcNsBindingLookupBeginW, _rpc_rpcnsbindinglookupbegin, rpc.rpcnsbindinglookupbegin, rpcnsi/RpcNsBindingLookupBegin, rpcnsi/RpcNsBindingLookupBeginA, rpcnsi/RpcNsBindingLookupBeginW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsBindingLookupBeginW (Unicode) and RpcNsBindingLookupBeginA (ANSI)
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
 - RpcNsBindingLookupBeginW
 - rpcnsi/RpcNsBindingLookupBeginW
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
 - RpcNsBindingLookupBegin
 - RpcNsBindingLookupBeginA
 - RpcNsBindingLookupBeginW
---

# RpcNsBindingLookupBeginW function


## -description

The 
<b>RpcNsBindingLookupBegin</b> function creates a lookup context for an interface and an object.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param EntryNameSyntax

Syntax of the <i>EntryName</i> parameter. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param EntryName

Pointer to an entry name at which the search for compatible bindings begins. 




To use the entry name specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultEntry</b>, provide a null pointer or an empty string. In this case, the <i>EntryNameSyntax</i> parameter is ignored and the run-time library uses the default syntax.

### -param IfSpec

Stub-generated structure indicating the interface to look up. If the interface specification has not been exported or is of no concern to the caller, specify a null value for this parameter. In this case, the bindings returned are only guaranteed to be of a compatible and supported protocol sequence and to contain the specified object UUID. The desired interface might not be supported by the contacted server.

### -param ObjUuid

Pointer to an optional object UUID. 




For a nonzero UUID, compatible binding handles are returned from an entry only if the server has exported the specified object UUID.

For a null pointer value or a nil UUID for this parameter, the returned binding handles contain one of the object UUIDs exported by the compatible server. If the server did not export any object UUIDs, the returned compatible binding handles contain a nil object UUID.

### -param BindingMaxCount

Maximum number of bindings to return in the <i>BindingVec</i> parameter from the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a> function. 




Specify a value of zero to use the default count of RPC_C_BINDING_MAX_COUNT_DEFAULT.

### -param LookupContext

Returns a pointer to a name-service handle for use with the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a> and 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone">RpcNsBindingLookupDone</a> functions.

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
<dt><b>RPC_S_INVALID_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNSUPPORTED_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is unsupported.

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
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
Invalid object.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsBindingLookupBegin</b> function creates a lookup context for locating client-compatible binding handles to servers that offer the specified interface and object.

Before calling 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>, the client application must first call 
<b>RpcNsBindingLookupBegin</b> to create a lookup context. The parameters to this function control the operation of the 
<b>RpcNsBindingLookupNext</b> function.

Effective with Windows 2000, the RPC environment uses the Active Directory as its name-service database and the order in which the run-time environment performs the search is as follows:

<ul>
<li>Search in the local cache.</li>
<li>If entry not found in local cache, search that machine's Active Directory.</li>
<li>If entry not found on local machine, send broadcast requests to all other Active Directory services in the domain. 


Note that if the entry exists in the Active Directory, but there is no information associated with the entry, the run-time environment will not issue this broadcast request.

</li>
</ul>
When finished locating binding handles, the client application calls the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone">RpcNsBindingLookupDone</a> function to delete the lookup context.





> [!NOTE]
> The rpcnsi.h header defines RpcNsBindingLookupBegin as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone">RpcNsBindingLookupDone</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>
