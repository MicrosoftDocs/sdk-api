---
UID: NF:rpcdce.RpcStringBindingComposeA
title: RpcStringBindingComposeA function (rpcdce.h)
description: The RpcStringBindingCompose function creates a string binding handle. (RpcStringBindingComposeA)
helpviewer_keywords: ["RpcStringBindingComposeA", "rpcdce/RpcStringBindingComposeA"]
old-location: rpc\rpcstringbindingcompose.htm
tech.root: Rpc
ms.assetid: 3f972fc9-67ca-4aa7-a0a0-204a8d90e928
ms.date: 12/05/2018
ms.keywords: RpcStringBindingCompose, RpcStringBindingCompose function [RPC], RpcStringBindingComposeA, RpcStringBindingComposeW, _rpc_rpcstringbindingcompose, rpc.rpcstringbindingcompose, rpcdce/RpcStringBindingCompose, rpcdce/RpcStringBindingComposeA, rpcdce/RpcStringBindingComposeW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcStringBindingComposeW (Unicode) and RpcStringBindingComposeA (ANSI)
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
 - RpcStringBindingComposeA
 - rpcdce/RpcStringBindingComposeA
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
 - RpcStringBindingCompose
 - RpcStringBindingComposeA
 - RpcStringBindingComposeW
---

# RpcStringBindingComposeA function


## -description

The 
<b>RpcStringBindingCompose</b> function creates a string binding handle.

## -parameters

### -param ObjUuid

Pointer to a <b>null</b>-terminated string representation of an object 
<a href="https://msdn.microsoft.com/">UUID</a>. For example, the string 6B29FC40-CA47-1067-B31D-00DD010662DA represents a valid UUID.

### -param ProtSeq

Pointer to a <b>null</b>-terminated string representation of a protocol sequence. See Note.

### -param NetworkAddr

Pointer to a <b>null</b>-terminated string representation of a network address. The network-address format is associated with the protocol sequence. See Note.

### -param Endpoint

Pointer to a <b>null</b>-terminated string representation of an endpoint. The endpoint format and content are associated with the protocol sequence. For example, the endpoint associated with the protocol sequence <b>ncacn_np</b> is a pipe name in the format \pipe\pipename. See Note.

### -param Options

Pointer to a <b>null</b>-terminated string representation of network options. The option string is associated with the protocol sequence. See Note.

### -param StringBinding

Returns a pointer to a pointer to a <b>null</b>-terminated string representation of a binding handle. 




Specify a <b>NULL</b> value to prevent 
<b>RpcStringBindingCompose</b> from returning the <i>StringBinding</i> parameter. In this case, the application does not call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>. See Note.

<div class="alert"><b>Note</b>  For more information, see 
<a href="/windows/desktop/Rpc/string-binding">String Binding</a>.</div>
<div> </div>

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
<dt><b>RPC_S_INVALID_STRING_UUID</b></dt>
</dl>
</td>
<td width="60%">
The string representation of the UUID is not valid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls 
<b>RpcStringBindingCompose</b> routine to combine an object UUID, a protocol sequence, a network address, an endpoint and other network options into a string representation of a binding handle.

The RPC run-time library allocates memory for the string returned in the <i>StringBinding</i> parameter. The application is responsible for calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> to deallocate that memory.

Specify a <b>null</b> parameter value or provide an empty string (\0) for each input string that has no data.

Literal backslash characters within C-language strings must be quoted. The actual C string for the server name for the <b>ncacn_np</b> protocol sequence appears as \\\\servername, and the actual C string for a pipe name appears as \\pipe\\pipename.





> [!NOTE]
> The rpcdce.h header defines RpcStringBindingCompose as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingtostringbinding">RpcBindingToStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingparse">RpcStringBindingParse</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
