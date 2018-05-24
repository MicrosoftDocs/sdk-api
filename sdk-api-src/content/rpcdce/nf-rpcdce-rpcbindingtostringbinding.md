---
UID: NF:rpcdce.RpcBindingToStringBinding
title: RpcBindingToStringBinding function
author: windows-driver-content
description: The RpcBindingToStringBinding function returns a string representation of a binding handle.
old-location: rpc\rpcbindingtostringbinding.htm
old-project: Rpc
ms.assetid: fd4fea9a-067e-4a1b-8be5-867bbe9663c5
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: RpcBindingToStringBinding, RpcBindingToStringBinding function [RPC], RpcBindingToStringBindingA, RpcBindingToStringBindingW, _rpc_rpcbindingtostringbinding, rpc.rpcbindingtostringbinding, rpcdce/RpcBindingToStringBinding, rpcdce/RpcBindingToStringBindingA, rpcdce/RpcBindingToStringBindingW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcBindingToStringBindingW (Unicode) and RpcBindingToStringBindingA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcBindingToStringBinding
-	RpcBindingToStringBindingA
-	RpcBindingToStringBindingW
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcBindingToStringBinding function


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
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function.


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcBindingToStringBinding</b> function converts a client or server binding handle to its string representation.

The RPC run-time library allocates memory for the string returned in the <i>StringBinding</i> parameter. The application is responsible for calling the 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function to deallocate that memory.

If the binding handle in the <i>Binding</i> parameter contained a nil object 
<a href="midl.uuid">UUID</a>, the object UUID field is not included in the returned string.

To parse the returned <i>StringBinding</i> parameter, call the 
<a href="https://msdn.microsoft.com/c55d0259-e251-42d0-8565-ce71ab3bb59c">RpcStringBindingParse</a> function.

<div class="alert"><b>Note</b>  To query a client's address, an application starts by calling the RpcBindingServerFromClient function to obtain a partially bound server binding handle.  The server binding handle can be used to obtain a string binding by invoking RpcBindingToStringBinding.  The server can then call RpcStringBindingParse to extract the client's network address from the string binding.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>



<a href="https://msdn.microsoft.com/c55d0259-e251-42d0-8565-ce71ab3bb59c">RpcStringBindingParse</a>



<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>
 

 

