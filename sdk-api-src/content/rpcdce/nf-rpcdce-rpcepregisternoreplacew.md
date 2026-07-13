---
UID: NF:rpcdce.RpcEpRegisterNoReplaceW
title: RpcEpRegisterNoReplaceW function (rpcdce.h)
description: The RpcEpRegisterNoReplaceW (Unicode) function (rpcdce.h) adds server-address information to the local endpoint-map database.
helpviewer_keywords: ["RpcEpRegisterNoReplace", "RpcEpRegisterNoReplace function [RPC]", "RpcEpRegisterNoReplaceW", "_rpc_rpcepregisternoreplace", "rpc.rpcepregisternoreplace", "rpcdce/RpcEpRegisterNoReplace", "rpcdce/RpcEpRegisterNoReplaceW"]
old-location: rpc\rpcepregisternoreplace.htm
tech.root: Rpc
ms.assetid: eaf132a8-0bc2-4201-945a-76b6c2eab559
ms.date: 08/16/2022
ms.keywords: RpcEpRegisterNoReplace, RpcEpRegisterNoReplace function [RPC], RpcEpRegisterNoReplaceA, RpcEpRegisterNoReplaceW, _rpc_rpcepregisternoreplace, rpc.rpcepregisternoreplace, rpcdce/RpcEpRegisterNoReplace, rpcdce/RpcEpRegisterNoReplaceA, rpcdce/RpcEpRegisterNoReplaceW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcEpRegisterNoReplaceW (Unicode) and RpcEpRegisterNoReplaceA (ANSI)
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
 - RpcEpRegisterNoReplaceW
 - rpcdce/RpcEpRegisterNoReplaceW
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
 - RpcEpRegisterNoReplace
 - RpcEpRegisterNoReplaceA
 - RpcEpRegisterNoReplaceW
---

# RpcEpRegisterNoReplaceW function


## -description

The 
<b>RpcEpRegisterNoReplace</b> function adds server-address information to the local endpoint-map database.

## -parameters

### -param IfSpec

Interface to register with the local endpoint-map database.

### -param BindingVector

Pointer to a vector of binding handles over which the server can receive remote procedure calls.

### -param UuidVector

Pointer to a vector of object UUIDs offered by the server. The server application constructs this vector. 




A null parameter value indicates there are no object UUIDs to register.

### -param Annotation

Pointer to the character-string comment applied to each cross-product element added to the local endpoint-map database. The string can be up to 64 characters long, including the null-terminating character. Specify a null value or a null-terminated string ("\0") if there is no annotation string. 




The annotation string is used by applications for information only. RPC does not use this string to determine which server instance a client communicates with or to enumerate elements in the endpoint-map database.

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
<b>RpcEpRegisterNoReplace</b> function adds entries to the local host's endpoint-map database. This function does not replace existing database entries.

A server uses 
<b>RpcEpRegisterNoReplace</b> rather than 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a> when multiple instances of the server will run on the same host. In other words, use this function when more than one server instance will offer the same interface UUID, object UUID, and protocol sequence at any one time.

Because entries are not replaced when calling 
<b>RpcEpRegisterNoReplace</b>, servers must unregister themselves before they stop running. Otherwise, stale data accumulates each time a server instance stops running without calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepunregister">RpcEpUnregister</a>. Stale entries increase the likelihood that a client will receive endpoints to nonexistent servers. The client will spend time trying to communicate with a nonexistent server before obtaining another endpoint.

A server can use 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a> and 
<b>RpcEpRegisterNoReplace</b> to register entries in the endpoint mapper database. Previous to Windows 2000, two functions were available to enable a server to overwrite stale entries in the endpoint mapper database left from previous server instances that are no longer running. The endpoint mapper database automatically removes entries registered by a server instance as soon as the server stops functioning. However, servers are not allowed to replace the endpoint mapper entries of another server for security purposes. Therefore, <b>RpcEpRegister</b> and 
<b>RpcEpRegisterNoReplace</b> perform largely the same functionality.

A server application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a> to register endpoints specified by calling any of the following functions:

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
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a> with the same <i>IfSpec</i>, <i>BindingVector</i>, and <i>UuidVector</i> values used when calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a> function.

If a protocol sequence is used without specifying an endpoint, the RPC run-time library automatically generates a dynamic endpoint. In this case, the server can call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a> followed by 
<b>RpcEpRegisterNoReplace</b> to make itself available to multiple clients. Otherwise, the automatically started server is known only to the client for which the server was started.

Each element added to the endpoint-map database logically contains the following:

<ul>
<li>Interface UUID</li>
<li>Interface version (major and minor)</li>
<li>Binding handle</li>
<li>Object UUID (optional)</li>
<li>Annotation (optional)</li>
</ul>
<b>RpcEpRegisterNoReplace</b> creates a cross-product from the <i>IfSpec</i>, <i>BindingVector</i>, and <i>UuidVector</i> parameters and adds each element in the cross-product as a separate registration in the endpoint-map database.





> [!NOTE]
> The rpcdce.h header defines RpcEpRegisterNoReplace as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepunregister">RpcEpUnregister</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif">RpcServerUseAllProtseqsIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseq">RpcServerUseProtseq</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqep">RpcServerUseProtseqEp</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif">RpcServerUseProtseqIf</a>
