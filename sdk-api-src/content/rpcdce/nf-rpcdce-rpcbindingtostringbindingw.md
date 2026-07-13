---
UID: NF:rpcdce.RpcBindingToStringBindingW
title: RpcBindingToStringBindingW function (rpcdce.h)
description: The RpcBindingToStringBindingW (Unicode) function (rpcdce.h) returns a string representation of a binding handle.
helpviewer_keywords: ["RpcBindingToStringBinding", "RpcBindingToStringBinding function [RPC]", "RpcBindingToStringBindingW", "_rpc_rpcbindingtostringbinding", "rpc.rpcbindingtostringbinding", "rpcdce/RpcBindingToStringBinding", "rpcdce/RpcBindingToStringBindingW"]
old-location: rpc\rpcbindingtostringbinding.htm
tech.root: Rpc
ms.assetid: fd4fea9a-067e-4a1b-8be5-867bbe9663c5
ms.date: 08/16/2022
ms.keywords: RpcBindingToStringBinding, RpcBindingToStringBinding function [RPC], RpcBindingToStringBindingA, RpcBindingToStringBindingW, _rpc_rpcbindingtostringbinding, rpc.rpcbindingtostringbinding, rpcdce/RpcBindingToStringBinding, rpcdce/RpcBindingToStringBindingA, rpcdce/RpcBindingToStringBindingW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcBindingToStringBindingW (Unicode) and RpcBindingToStringBindingA (ANSI)
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
 - RpcBindingToStringBindingW
 - rpcdce/RpcBindingToStringBindingW
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
 - RpcBindingToStringBinding
 - RpcBindingToStringBindingA
 - RpcBindingToStringBindingW
---

# RpcBindingToStringBindingW function


## -description

The 
<b>RpcBindingToStringBinding</b> function returns a string representation of a binding handle.

## -parameters

### -param Binding

Client or server binding handle to convert to a string representation of a binding handle.

### -param StringBinding

Returns a pointer to a pointer to the string representation of the binding handle specified in the <i>Binding</i> parameter. 




Specify a null value to prevent 
<b>RpcBindingToStringBinding</b> from returning the <i>StringBinding</i> parameter. In this case, the application does not call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function.

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
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcBindingToStringBinding</b> function converts a client or server binding handle to its string representation.

The RPC run-time library allocates memory for the string returned in the <i>StringBinding</i> parameter. The application is responsible for calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function to deallocate that memory.

If the binding handle in the <i>Binding</i> parameter contained a nil object 
<a href="https://msdn.microsoft.com/">UUID</a>, the object UUID field is not included in the returned string.

To parse the returned <i>StringBinding</i> parameter, call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingparse">RpcStringBindingParse</a> function.

<div class="alert"><b>Note</b>  To query a client's address, an application starts by calling the RpcBindingServerFromClient function to obtain a partially bound server binding handle.  The server binding handle can be used to obtain a string binding by invoking RpcBindingToStringBinding.  The server can then call RpcStringBindingParse to extract the client's network address from the string binding.</div>
<div> </div>




> [!NOTE]
> The rpcdce.h header defines RpcBindingToStringBinding as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingparse">RpcStringBindingParse</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
