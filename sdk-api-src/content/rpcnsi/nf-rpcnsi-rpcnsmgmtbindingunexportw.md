---
UID: NF:rpcnsi.RpcNsMgmtBindingUnexportW
title: RpcNsMgmtBindingUnexportW function (rpcnsi.h)
description: The RpcNsMgmtBindingUnexport function removes multiple binding handles and objects from an entry in the name-service database. (Unicode)
helpviewer_keywords: ["RPC_C_VERS_ALL", "RPC_C_VERS_EXACT", "RPC_C_VERS_IF_ID", "RPC_C_VERS_MAJOR_ONLY", "RPC_C_VERS_UPTO", "RpcNsMgmtBindingUnexport", "RpcNsMgmtBindingUnexport function [RPC]", "RpcNsMgmtBindingUnexportW", "_rpc_rpcnsmgmtbindingunexport", "rpc.rpcnsmgmtbindingunexport", "rpcnsi/RpcNsMgmtBindingUnexport", "rpcnsi/RpcNsMgmtBindingUnexportW"]
old-location: rpc\rpcnsmgmtbindingunexport.htm
tech.root: Rpc
ms.assetid: e15b9e45-ac9f-4f90-9323-8b16066290d2
ms.date: 12/05/2018
ms.keywords: RPC_C_VERS_ALL, RPC_C_VERS_EXACT, RPC_C_VERS_IF_ID, RPC_C_VERS_MAJOR_ONLY, RPC_C_VERS_UPTO, RpcNsMgmtBindingUnexport, RpcNsMgmtBindingUnexport function [RPC], RpcNsMgmtBindingUnexportA, RpcNsMgmtBindingUnexportW, _rpc_rpcnsmgmtbindingunexport, rpc.rpcnsmgmtbindingunexport, rpcnsi/RpcNsMgmtBindingUnexport, rpcnsi/RpcNsMgmtBindingUnexportA, rpcnsi/RpcNsMgmtBindingUnexportW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsMgmtBindingUnexportW (Unicode) and RpcNsMgmtBindingUnexportA (ANSI)
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
 - RpcNsMgmtBindingUnexportW
 - rpcnsi/RpcNsMgmtBindingUnexportW
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
 - RpcNsMgmtBindingUnexport
 - RpcNsMgmtBindingUnexportA
 - RpcNsMgmtBindingUnexportW
---

# RpcNsMgmtBindingUnexportW function


## -description

The 
<b>RpcNsMgmtBindingUnexport</b> function removes multiple binding handles and objects from an entry in the name-service database.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param EntryName

Pointer to the name of the entry from which to remove binding handles and object UUIDs.

### -param IfId

Pointer to an interface identification. A null parameter value indicates that binding handles are not to be unexported—only object UUIDs are to be unexported.

### -param VersOption

Specifies how the 
<b>RpcNsMgmtBindingUnexport</b> function uses the <b>VersMajor</b> and <b>VersMinor</b> members of the structure pointed to by the <i>IfId</i> parameter. 




The following table describes valid values for the <i>VersOption</i> parameter.

<table>
<tr>
<th>VersOption values</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_ALL"></a><a id="rpc_c_vers_all"></a><dl>
<dt><b>RPC_C_VERS_ALL</b></dt>
</dl>
</td>
<td width="60%">
Unexports all bindings for the interface UUID in <i>IfId</i>, regardless of the version numbers. For this value, specify 0 for both the major and minor versions in <i>IfId</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_IF_ID"></a><a id="rpc_c_vers_if_id"></a><dl>
<dt><b>RPC_C_VERS_IF_ID</b></dt>
</dl>
</td>
<td width="60%">
Unexports the bindings for the compatible interface UUID in <i>IfId</i> with the same major version and with a minor version greater than or equal to the minor version in <i>IfId</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_EXACT"></a><a id="rpc_c_vers_exact"></a><dl>
<dt><b>RPC_C_VERS_EXACT</b></dt>
</dl>
</td>
<td width="60%">
Unexports the bindings for the interface UUID in <i>IfId</i> with the same major and minor versions as in <i>IfId</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_MAJOR_ONLY"></a><a id="rpc_c_vers_major_only"></a><dl>
<dt><b>RPC_C_VERS_MAJOR_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Unexports the bindings for the interface UUID in <i>IfId</i> with the same major version as in <i>IfId</i> (ignores the minor version). For this value, specify 0 for the minor version in <i>IfId</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_UPTO"></a><a id="rpc_c_vers_upto"></a><dl>
<dt><b>RPC_C_VERS_UPTO</b></dt>
</dl>
</td>
<td width="60%">
Unexports the bindings that offer a version of the specified interface UUID less than or equal to the specified major and minor version. (For example, if the <i>IfId</i> contained V2.0 and the name service–database entry contained binding handles with the versions 1.3, 2.0, and 2.1, the 
<b>RpcNsMgmtBindingUnexport</b> function would unexport the binding handles with versions 1.3 and 2.0.)

</td>
</tr>
</table>

### -param ObjectUuidVec

Pointer to a vector of object UUIDs that the server no longer wants to offer. The application constructs this vector. A null value indicates there are no object UUIDs to unexport—only binding handles are to be unexported.

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
The name syntax is not supported.

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
<b>RpcNsMgmtBindingUnexport</b> function allows a management application to remove one of the following from a name service–database entry:

<ul>
<li>All the binding handles for a specified interface UUID, qualified by the interface version numbers (major and minor)</li>
<li>One or more object UUIDs of resources</li>
<li>Both binding handles and object UUIDs of resources</li>
</ul>
A management application can unexport interfaces and objects in a single call to 
<b>RpcNsMgmtBindingUnexport</b>, or it can unexport them separately. If 
<b>RpcNsMgmtBindingUnexport</b> does not find any binding handles for the specified interface, the function returns an RPC_S_INTERFACE_NOT_FOUND status code and does not unexport the object UUIDs, if any were specified.

If one or more binding handles for the specified interface are found and unexported without error, 
<b>RpcNsMgmtBindingUnexport</b> unexports any specified object UUIDs. If any of the specified object UUIDs were not found, 
<b>RpcNsMgmtBindingUnexport</b> returns RPC_S_NOT_ALL_OBJS_UNEXPORTED.

In addition to calling 
<b>RpcNsMgmtBindingUnexport</b>, a management application should also call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepunregister">RpcMgmtEpUnregister</a> function to unregister the servers that have registered with the endpoint-map database.

<div class="alert"><b>Note</b>  Name-service databases are designed to be relatively stable. In replicated name services, frequent use of the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a> and 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingunexporta">RpcNsBindingUnexport</a> functions causes the name service to repeatedly remove and replace the same entry, which can cause performance problems.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsMgmtBindingUnexport as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepunregister">RpcMgmtEpUnregister</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingunexporta">RpcNsBindingUnexport</a>
