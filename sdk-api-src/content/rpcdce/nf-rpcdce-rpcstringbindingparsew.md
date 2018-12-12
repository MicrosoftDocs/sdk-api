---
UID: NF:rpcdce.RpcStringBindingParseW
title: RpcStringBindingParseW function
author: windows-sdk-content
description: The RpcStringBindingParse function returns the object UUID part and the address parts of a string binding as separate strings.
old-location: rpc\rpcstringbindingparse.htm
tech.root: rpc
ms.assetid: c55d0259-e251-42d0-8565-ce71ab3bb59c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcStringBindingParse, RpcStringBindingParse function [RPC], RpcStringBindingParseA, RpcStringBindingParseW, _rpc_rpcstringbindingparse, rpc.rpcstringbindingparse, rpcdce/RpcStringBindingParse, rpcdce/RpcStringBindingParseA, rpcdce/RpcStringBindingParseW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcStringBindingParseW (Unicode) and RpcStringBindingParseA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcStringBindingParse
 - RpcStringBindingParseA
 - RpcStringBindingParseW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcStringBindingParseW function


## -description


The 
<b>RpcStringBindingParse</b> function returns the object UUID part and the address parts of a string binding as separate strings. An application calls 
<b>RpcStringBindingParse</b> to parse a string representation of a binding handle into its component fields. The 
<b>RpcStringBindingParse</b> function returns the object UUID part and the address parts of a string binding as separate strings.


## -parameters




### -param StringBinding

Pointer to a <b>null</b>-terminated string representation of a binding.


### -param ObjUuid

Returns a pointer to a pointer to a <b>null</b>-terminated string representation of an object 
<a href="https://msdn.microsoft.com/72cf12f5-49cd-440d-9665-73211509d050">UUID</a>. 




Specify a <b>NULL</b> value to prevent 
<b>RpcStringBindingParse</b> from returning the <i>ObjectUuid</i> parameter. In this case, the application does not call 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>.


### -param Protseq

Returns a pointer to a pointer to a <b>null</b>-terminated string representation of a protocol sequence. For a list of Microsoft RPC supported protocol sequences, see 
<a href="https://msdn.microsoft.com/5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305">String Binding</a>. 




Specify a <b>NULL</b> value to prevent 
<b>RpcStringBindingParse</b> from returning the <i>ProtSeq</i> parameter. In this case, the application does not call 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>.


### -param NetworkAddr

Returns a pointer to a pointer to a <b>null</b>-terminated string representation of a network address. Specify a <b>NULL</b> value to prevent 
<b>RpcStringBindingParse</b> from returning the <i>NetworkAddr</i> parameter. In this case, the application does not call 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>.


### -param Endpoint

Returns a pointer to a pointer to a <b>null</b>-terminated string representation of an endpoint. Specify a <b>NULL</b> value to prevent 
<b>RpcStringBindingParse</b> from returning the <i>EndPoint</i> parameter. In this case, the application does not call 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>.


### -param NetworkOptions

Returns a pointer to a pointer to a <b>null</b>-terminated string representation of network options. 




Specify a <b>NULL</b> value to prevent 
<b>RpcStringBindingParse</b> from returning the <i>NetworkOptions</i> parameter. In this case, the application does not call 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>.


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
The string binding is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls 
<b>RpcStringBindingParse</b> routine to parse a string representation of a binding handle into its component fields.

The RPC run-time library allocates memory for each component string returned. The application is responsible for calling 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> once for each returned string to deallocate the memory for that string.

If any field of the <i>StringBinding</i> parameter is empty, 
<b>RpcStringBindingParse</b> returns an empty string (\0) in the corresponding output parameter.

<div class="alert"><b>Note</b>  To query a client's address, an application starts by calling the RpcBindingServerFromClient function to obtain a partially bound server binding handle.  The server binding handle can be used to obtain a string binding by invoking RpcBindingToStringBinding.  The server can then call RpcStringBindingParse to extract the client's network address from the string binding.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>



<a href="https://msdn.microsoft.com/fd4fea9a-067e-4a1b-8be5-867bbe9663c5">RpcBindingToStringBinding</a>



<a href="https://msdn.microsoft.com/3f972fc9-67ca-4aa7-a0a0-204a8d90e928">RpcStringBindingCompose</a>



<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>
 

 

