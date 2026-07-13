---
UID: NF:rpcdce.RpcEpRegisterW
title: RpcEpRegisterW function (rpcdce.h)
description: The RpcEpRegisterW (Unicode) function (rpcdce.h) adds to or replaces server address information in the local endpoint-map database.
helpviewer_keywords: ["RpcEpRegister", "RpcEpRegister function [RPC]", "RpcEpRegisterW", "_rpc_rpcepregister", "rpc.rpcepregister", "rpcdce/RpcEpRegister", "rpcdce/RpcEpRegisterW"]
old-location: rpc\rpcepregister.htm
tech.root: Rpc
ms.assetid: 35656cdd-b1ae-43d3-a5c7-92bdb7726d5b
ms.date: 08/16/2022
ms.keywords: RpcEpRegister, RpcEpRegister function [RPC], RpcEpRegisterA, RpcEpRegisterW, _rpc_rpcepregister, rpc.rpcepregister, rpcdce/RpcEpRegister, rpcdce/RpcEpRegisterA, rpcdce/RpcEpRegisterW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcEpRegisterW (Unicode) and RpcEpRegisterA (ANSI)
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
 - RpcEpRegisterW
 - rpcdce/RpcEpRegisterW
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
 - RpcEpRegister
 - RpcEpRegisterA
 - RpcEpRegisterW
---

# RpcEpRegisterW function


## -description

The 
<b>RpcEpRegister</b> function adds to or replaces server address information in the local endpoint-map database.

## -parameters

### -param IfSpec

Interface to register with the local endpoint-map database.

### -param BindingVector

Pointer to a vector of binding handles over which the server can receive remote procedure calls.

### -param UuidVector

Pointer to a vector of object UUIDs offered by the server. The server application constructs this vector.A null argument value indicates there are no object UUIDs to register.

### -param Annotation

Pointer to the character-string comment applied to each cross-product element added to the local endpoint-map database. The string can be up to 64 characters long, including the null terminating character. Specify a null value or a null-terminated string ("\0") if there is no annotation string. 




The annotation string is used by applications for information only. RPC does not use this string to determine which server instance a client communicates with or for enumerating elements in the endpoint-map database.

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
<dt><b>RPC_S_NO_BINDINGS</b></dt>
</dl>
</td>
<td width="60%">
No bindings.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcEpRegister</b> function adds or replaces entries in the local host's endpoint-map database. For an existing database entry that matches the provided interface specification, binding handle, and object UUID, this function replaces the entry's endpoint with the endpoint in the provided binding handle.

A server can use 
<b>RpcEpRegister</b> and 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a> to register entries in the endpoint mapper database. Previous to Windows 2000, two functions were available to enable a server to overwrite stale entries in the endpoint mapper database left from previous server instances that are no longer running. The endpoint mapper database automatically removes entries registered by a server instance as soon as the server stops functioning. However, servers are not allowed to replace the endpoint mapper entries of another server for security purposes. Therefore, <b>RpcEpRegister</b> and 
<b>RpcEpRegisterNoReplace</b> perform largely the same functionality.

A server application calls 
<b>RpcEpRegister</b> to register endpoints specified by calling any of the following functions:

<ul>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseq">RpcServerUseProtseq</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqep">RpcServerUseProtseqEp</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif">RpcServerUseAllProtseqsIf</a>
</li>
<li>
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif">RpcServerUseProtseqIf</a>
</li>
</ul>
If the server also exports to the name-service database, the server calls 
<b>RpcEpRegister</b> with the same <i>IfSpec</i>, <i>BindingVector</i>, and <i>UuidVector</i> values used when calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a> function.

If a protocol sequence is used without specifying an endpoint, the RPC run-time library automatically generates a dynamic endpoint.. In this case, the server can call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a> followed by 
<b>RpcEpRegister</b> to make itself available to multiple clients. Otherwise, the automatically started server is known only to the client for which the server was started.Each element added to the endpoint-map database logically contains the following:

<ul>
<li>Interface 
<a href="https://msdn.microsoft.com/">UUID</a>
</li>
<li>Interface version (major and minor)</li>
<li>Binding handle</li>
<li>Object UUID (optional)</li>
<li>Annotation (optional)</li>
</ul>
<b>RpcEpRegister</b> creates a cross-product from the <i>IfSpec</i>, <i>BindingVector</i>, and <i>UuidVector</i> parameters and adds each element in the cross-product as a separate registration in the endpoint-map database.





> [!NOTE]
> The rpcdce.h header defines RpcEpRegister as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepunregister">RpcEpUnregister</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif">RpcServerUseAllProtseqsIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseq">RpcServerUseProtseq</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqep">RpcServerUseProtseqEp</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif">RpcServerUseProtseqIf</a>
