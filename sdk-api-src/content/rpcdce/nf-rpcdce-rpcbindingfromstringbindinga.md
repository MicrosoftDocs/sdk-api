---
UID: NF:rpcdce.RpcBindingFromStringBindingA
title: RpcBindingFromStringBindingA function (rpcdce.h)
description: Returns a binding handle from a string representation of a binding handle. (RpcBindingFromStringBindingA)
helpviewer_keywords: ["RpcBindingFromStringBindingA", "rpcdce/RpcBindingFromStringBindingA"]
old-location: rpc\rpcbindingfromstringbinding.htm
tech.root: Rpc
ms.assetid: fd82fb9f-da0e-46fb-9c11-a75a9b6ee858
ms.date: 12/05/2018
ms.keywords: RpcBindingFromStringBinding, RpcBindingFromStringBinding function [RPC], RpcBindingFromStringBindingA, RpcBindingFromStringBindingW, _rpc_rpcbindingfromstringbinding, rpc.rpcbindingfromstringbinding, rpcdce/RpcBindingFromStringBinding, rpcdce/RpcBindingFromStringBindingA, rpcdce/RpcBindingFromStringBindingW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcBindingFromStringBindingW (Unicode) and RpcBindingFromStringBindingA (ANSI)
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
 - RpcBindingFromStringBindingA
 - rpcdce/RpcBindingFromStringBindingA
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
 - RpcBindingFromStringBinding
 - RpcBindingFromStringBindingA
 - RpcBindingFromStringBindingW
---

# RpcBindingFromStringBindingA function


## -description

The 
<b>RpcBindingFromStringBinding</b> function returns a binding handle from a string representation of a binding handle.

## -parameters

### -param StringBinding

Pointer to a string representation of a binding handle.

### -param Binding

Returns a pointer to the server binding handle.

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
<dt><b>RPC_S_INVALID_STRING_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The string binding is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_PROTSEQ_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Protocol sequence not supported on this host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_RPC_PROTSEQ</b></dt>
</dl>
</td>
<td width="60%">
The protocol sequence is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ENDPOINT_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The endpoint format is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_STRING_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
String too long.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_NET_ADDR</b></dt>
</dl>
</td>
<td width="60%">
The network address is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_NAF_ID</b></dt>
</dl>
</td>
<td width="60%">
The network address family identifier is not valid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcBindingFromStringBinding</b> function creates a server binding handle from a string representation of a binding handle. The <i>StringBinding</i> parameter does not have to contain an object 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>. In this case, the returned binding contains a nil UUID. If the provided <i>StringBinding</i> parameter does not contain an endpoint field, the returned <i>Binding</i> parameter is a partially-bound binding handle. If the provided <i>StringBinding</i> parameter contains an endpoint field, the endpoint is considered to be a well-known endpoint. If the provided <i>StringBinding</i> parameter does not contain a host address field, the returned <i>Binding</i> parameter references the local host.

An application creates a string binding by calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingcompose">RpcStringBindingCompose</a> function or by providing a character-string constant. The creation of a string binding by this method does not involve contact with the server. Success or failure of the API will not indicate server availability.

When an application is finished using the <i>Binding</i> parameter, the application should call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a> function to release the memory used by the binding handle.





> [!NOTE]
> The rpcdce.h header defines RpcBindingFromStringBinding as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingcopy">RpcBindingCopy</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingtostringbinding">RpcBindingToStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingcompose">RpcStringBindingCompose</a>
