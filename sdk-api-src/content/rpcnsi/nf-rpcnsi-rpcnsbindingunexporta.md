---
UID: NF:rpcnsi.RpcNsBindingUnexportA
title: RpcNsBindingUnexportA function (rpcnsi.h)
description: The RpcNsBindingUnexport function removes the binding handles for an interface and objects from an entry in the name-service database. (ANSI)
helpviewer_keywords: ["RpcNsBindingUnexportA", "rpcnsi/RpcNsBindingUnexportA"]
old-location: rpc\rpcnsbindingunexport.htm
tech.root: Rpc
ms.assetid: 70662e7e-7a81-4953-9814-e29b46422c5b
ms.date: 12/05/2018
ms.keywords: RpcNsBindingUnexport, RpcNsBindingUnexport function [RPC], RpcNsBindingUnexportA, RpcNsBindingUnexportW, _rpc_rpcnsbindingunexport, rpc.rpcnsbindingunexport, rpcnsi/RpcNsBindingUnexport, rpcnsi/RpcNsBindingUnexportA, rpcnsi/RpcNsBindingUnexportW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsBindingUnexportW (Unicode) and RpcNsBindingUnexportA (ANSI)
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
 - RpcNsBindingUnexportA
 - rpcnsi/RpcNsBindingUnexportA
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
 - RpcNsBindingUnexport
 - RpcNsBindingUnexportA
 - RpcNsBindingUnexportW
---

# RpcNsBindingUnexportA function


## -description

The 
<b>RpcNsBindingUnexport</b> function removes the binding handles for an interface and objects from an entry in the name-service database.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param EntryName

Pointer to the entry name from which to remove binding handles and object UUIDs.

### -param IfSpec

Interface specification for the binding handles to be removed from the name service database. A null parameter value indicates not to unexport any binding handles (only object UUIDs are to be unexported).

### -param ObjectUuidVec

Pointer to a vector of object UUIDs that the server no longer wants to offer. The application constructs this vector. A null value indicates there are no object UUIDs to unexport (only binding handles are to be unexported).

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
<dt><b>RPC_S_INVALID_VERS_OPTION</b></dt>
</dl>
</td>
<td width="60%">
The version option is invalid.

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
<dt><b>RPC_S_INTERFACE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The interface was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NOT_ALL_OBJS_UNEXPORTED</b></dt>
</dl>
</td>
<td width="60%">
Not all objects unexported.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsBindingUnexport</b> function allows a server application to remove the binding handles and object UUIDs of resources from a name service database entry. A server application can unexport the specified interface and objects in a single call to 
<b>RpcNsBindingUnexport</b>, or it can unexport them separately. Only the binding handles that match the interface UUID and the major and minor interface version numbers found in the <i>IfSpec</i> parameter are unexported. Use the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtbindingunexporta">RpcNsMgmtBindingUnexport</a> function to remove multiple versions of an interface.

Effective with Windows 2000, the RPC run-time environment uses the Active Directory as its name-service database. This means that an authorized unexported entries will be removed both from the local cache and from the Active Directory. Unauthorized unexports will only be removed from the local cache. See 
<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> in the Security section of the Platform Software Development Kit (SDK) for more information on authorization and Access Control Lists.

If 
<b>RpcNsBindingUnexport</b> does not find any binding handles for the specified interface, the function returns an RPC_S_INTERFACE_NOT_FOUND status code and does not unexport the object UUIDs, if any were specified.

If one or more binding handles for the specified interface are found and unexported without error, 
<b>RpcNsBindingUnexport</b> unexports the specified object UUIDs, if any.

If any of the specified object UUIDs were not found, 
<b>RpcNsBindingUnexport</b> returns the RPC_S_NOT_ALL_OBJS_UNEXPORTED status code.

In addition to calling 
<b>RpcNsBindingUnexport</b>, a server should also call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepunregister">RpcEpUnregister</a> function to unregister the endpoints the server previously registered with the local endpoint-map database.

Once created, a server entry persists, even when all of the binding handles and UUIDs are removed. A server entry must have at least one binding handle to exist. As a result, exporting only UUIDs to a nonexisting entry has no effect, and unexporting all binding handles deletes the entry.

Use 
<b>RpcNsBindingUnexport</b> judiciously. To keep an automatically activated server available, you must leave its binding handles in the name-service database between the times when server processes are activated. However, with dynamic bindings, if you do not unexport binding handles, the Active Directory can become so large as to be unmanageable.

Therefore, before you call this function, keep in mind how long you expect the server to be unavailable, and the type of binding in use. If you are using static bindings, reserve this function for when you expect a server to be unavailable for an extended time—for example, when it is being permanently removed from service.

<div class="alert"><b>Note</b>  Name-service databases are designed to be relatively stable. In replicated name-service databases, frequent use of the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a> and 
<b>RpcNsBindingUnexport</b> functions causes the name-service database to repeatedly remove and replace the same entry and can cause performance problems.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsBindingUnexport as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepunregister">RpcEpUnregister</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>
