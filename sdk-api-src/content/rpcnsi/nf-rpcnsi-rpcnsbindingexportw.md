---
UID: NF:rpcnsi.RpcNsBindingExportW
title: RpcNsBindingExportW function (rpcnsi.h)
description: The RpcNsBindingExport function establishes a name service database entry with multiple binding handles and multiple objects for a server. (Unicode)
helpviewer_keywords: ["RpcNsBindingExport", "RpcNsBindingExport function [RPC]", "RpcNsBindingExportW", "_rpc_rpcnsbindingexport", "rpc.rpcnsbindingexport", "rpcnsi/RpcNsBindingExport", "rpcnsi/RpcNsBindingExportW"]
old-location: rpc\rpcnsbindingexport.htm
tech.root: Rpc
ms.assetid: c89d04d7-f607-48cc-8cb6-b6aebab41671
ms.date: 12/05/2018
ms.keywords: RpcNsBindingExport, RpcNsBindingExport function [RPC], RpcNsBindingExportA, RpcNsBindingExportW, _rpc_rpcnsbindingexport, rpc.rpcnsbindingexport, rpcnsi/RpcNsBindingExport, rpcnsi/RpcNsBindingExportA, rpcnsi/RpcNsBindingExportW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsBindingExportW (Unicode) and RpcNsBindingExportA (ANSI)
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
 - RpcNsBindingExportW
 - rpcnsi/RpcNsBindingExportW
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
 - RpcNsBindingExport
 - RpcNsBindingExportA
 - RpcNsBindingExportW
---

# RpcNsBindingExportW function


## -description

The 
<b>RpcNsBindingExport</b> function establishes a name service–database entry with multiple binding handles and multiple objects for a server.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param EntryName

Pointer to the entry name to which binding handles and object UUIDs are exported. You cannot provide a null or empty string. The client and the server must both use the same entry name.

### -param IfSpec

Stub-generated data structure specifying the interface to export. A null value indicates there are no binding handles to export (only object UUIDs are to be exported) and <i>BindingVec</i> is ignored.

### -param BindingVec

Pointer to server bindings to export. A null value indicates there are no binding handles to export (only object UUIDs are to be exported).

### -param ObjectUuidVec

Pointer to a vector of object UUIDs offered by the server. The server application constructs this vector. A null value indicates there are no object UUIDs to export (only binding handles are to be exported).

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
<dt><b>RPC_S_NOTHING_TO_EXPORT</b></dt>
</dl>
</td>
<td width="60%">
There was nothing to export.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

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
<dt><b>RPC_S_NO_NS_PRIVILEGE</b></dt>
</dl>
</td>
<td width="60%">
No privilege for name-service operation.

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
<b>RpcNsBindingExport</b> function allows a server application to publicly offer an interface in the name-service database for use by any client application.

Effective with Windows 2000, the RPC run-time environment uses the Active Directory as its name-service database. This means that authorized exported entries persist in the name service, and are visible even after rebooting. Unauthorized exports do not persist. See 
<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> in the Security section of the Platform Software Development Kit (SDK) for more information on authorization and Access Control Lists.

To export an interface, the server application calls the 
<b>RpcNsBindingExport</b> routine with an interface and the server binding handles a client can use to access the server. A server application also calls the 
<b>RpcNsBindingExport</b> function to publicly offer the object UUID(s) of resource(s) it offers, if any, in the name-service database.

A server can export interfaces and objects in a single call to 
<b>RpcNsBindingExport</b>, or it can export them separately.If the name-service database entry specified by <i>EntryName</i> does not exist, 
<b>RpcNsBindingExport</b> tries to create it. In this case, the server application must have the privilege to create the entry.In addition to calling 
<b>RpcNsBindingExport</b>, a server that called the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a> or 
<b>RpcServerUseProtseq</b> function must also register with the local endpoint-map database by calling either 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a> or 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>.

A server is not required to export any of its interfaces to the name-service database. When a server does not export, only clients that privately know that server's binding information can access its interfaces. For example, a client that has the information needed to construct a string binding can call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a> to create a binding handle for making remote procedure calls to a server.

Before calling 
<b>RpcNsBindingExport</b>, a server must do the following:

<ul>
<li>Register one or more protocol sequences with the local RPC run-time library by calling one of the following functions: 


<ul>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>, 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsex">RpcServerUseAllProtseqsEx</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseq">RpcServerUseProtseq</a>, 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqex">RpcServerUseProtseqEx</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif">RpcServerUseAllProtseqsIf</a>, 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex">RpcServerUseAllProtseqsIfEx</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif">RpcServerUseProtseqIf</a>, 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif">RpcServerUseProtseqIf</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqep">RpcServerUseProtseqEp</a>, 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqep">RpcServerUseProtseqEp</a>
</li>
</ul>
</li>
<li>Obtain a list of server bindings by calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a> function.</li>
</ul>
The vector returned from the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a> function becomes the <i>Binding</i> parameter for 
<b>RpcNsBindingExport</b>. To prevent a binding from being exported, set the selected vector element to a null value.

If a server exports to the same name-service database entry multiple times, the second and subsequent calls to 
<b>RpcNsBindingExport</b> add the binding information and object UUIDs when that data is different from the binding information already in the server entry. Existing data is not removed from the entry.

To remove binding handles and object UUIDs from the name-service database, a server application calls the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingunexporta">RpcNsBindingUnexport</a> function.

A server entry must have at least one binding handle to exist. As a result, exporting only UUIDs to a non-existing entry has no effect, and unexporting all binding handles deletes the entry.





> [!NOTE]
> The rpcnsi.h header defines RpcNsBindingExport as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingunexporta">RpcNsBindingUnexport</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif">RpcServerUseAllProtseqsIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseq">RpcServerUseProtseq</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqep">RpcServerUseProtseqEp</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif">RpcServerUseProtseqIf</a>
