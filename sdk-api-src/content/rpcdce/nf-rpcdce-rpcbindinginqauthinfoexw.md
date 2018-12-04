---
UID: NF:rpcdce.RpcBindingInqAuthInfoExW
title: RpcBindingInqAuthInfoExW function
author: windows-sdk-content
description: The RpcBindingInqAuthInfoEx function returns authentication, authorization, and security quality-of-service information from a binding handle.
old-location: rpc\rpcbindinginqauthinfoex.htm
tech.root: rpc
ms.assetid: e75f5ba6-7a1c-4069-8810-05aa38a47e9c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RpcBindingInqAuthInfoEx, RpcBindingInqAuthInfoEx function [RPC], RpcBindingInqAuthInfoExA, RpcBindingInqAuthInfoExW, _rpc_rpcbindinginqauthinfoex, rpc.rpcbindinginqauthinfoex, rpcdce/RpcBindingInqAuthInfoEx, rpcdce/RpcBindingInqAuthInfoExA, rpcdce/RpcBindingInqAuthInfoExW
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
req.unicode-ansi: RpcBindingInqAuthInfoExW (Unicode) and RpcBindingInqAuthInfoExA (ANSI)
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
 - RpcBindingInqAuthInfoEx
 - RpcBindingInqAuthInfoExA
 - RpcBindingInqAuthInfoExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcBindingInqAuthInfoExW function


## -description


The 
<b>RpcBindingInqAuthInfoEx</b> function returns authentication, authorization, and security quality-of-service information from a binding handle.


## -parameters




### -param Binding

Server binding handle from which authentication and authorization information is returned.


### -param ServerPrincName

Returns a pointer to a pointer to the expected principal name of the server referenced in <i>Binding</i>. The content of the returned name and its syntax are defined by the authentication service in use.

Specify a null value to prevent 
<b>RpcBindingInqAuthInfoEx</b> from returning the <i>ServerPrincName</i> parameter. In this case, the application does not call the 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function.


### -param AuthnLevel

Returns a pointer set to the level of authentication used for remote procedure calls made using <i>Binding</i>. For a list of the RPC-supported authentication levels, see 
<a href="https://msdn.microsoft.com/b8bb2517-e1a0-4607-a672-259f8686fc3e">Authentication-Level Constants</a>. Specify a null value to prevent the function from returning the <i>AuthnLevel</i> parameter.

The level returned in the <i>AuthnLevel</i> parameter may be different from the level specified when the client called the 
<a href="https://msdn.microsoft.com/2438816c-995e-4398-999d-48a3538eec18">RpcBindingSetAuthInfoEx</a> function. This discrepancy happens when the RPC run-time library does not support the authentication level specified by the client and automatically upgrades to the next higher authentication level.


### -param AuthnSvc

Returns a pointer set to the authentication service specified for remote procedure calls made using <i>Binding</i>. For a list of the RPC-supported authentication services, see 
<a href="https://msdn.microsoft.com/ac95276f-230d-4993-92fe-1739d022c8b3">Authentication-Service Constants</a>.

Specify a null value to prevent 
<b>RpcBindingInqAuthInfoEx</b> from returning the <i>AuthnSvc</i> parameter.


### -param AuthIdentity

Returns a pointer to a handle to the data structure that contains the client's authentication and authorization credentials specified for remote procedure calls made using <i>Binding</i>.

Specify a null value to prevent 
<b>RpcBindingInqAuthInfoEx</b> from returning the <i>AuthIdentity</i> parameter.


### -param AuthzSvc

Returns a pointer set to the authorization service requested by the client application that made the remote procedure call on <i>Binding</i>. For a list of the RPC-supported authentication services, see 
<a href="https://msdn.microsoft.com/ac95276f-230d-4993-92fe-1739d022c8b3">Authentication-Service Constants</a>.

Specify a null value to prevent 
<b>RpcBindingInqAuthInfoEx</b> from returning the <i>AuthzSvc</i> parameter.


### -param RpcQosVersion

Passes value of current version (needed for forward compatibility if extensions are made to this function). Always set this parameter to RPC_C_SECURITY_QOS_VERSION.


### -param SecurityQOS

Returns pointer to the 
<a href="https://msdn.microsoft.com/f7733b9d-ae32-44ff-b1ca-dd0292dd0ff6">RPC_SECURITY_QOS</a> structure, which defines quality-of-service settings.


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
<dt><b>RPC_BINDING_HAS_NO_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Binding has no authentication information.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A client application calls the 
<b>RpcBindingInqAuthInfoEx</b> function to view the authentication and authorization information associated with a server binding handle. This function provides the ability to inquire about the security quality of service on the binding handle. It is otherwise identical to 
<a href="https://msdn.microsoft.com/becb2c58-bfc7-47a7-ad2f-947ecf7bba2b">RpcBindingInqAuthInfo</a>.

The RPC run-time library allocates memory for the returned <i>ServerPrincName</i> parameter. The application is responsible for calling the 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function for that returned argument string.




## -see-also




<a href="https://msdn.microsoft.com/f7733b9d-ae32-44ff-b1ca-dd0292dd0ff6">RPC_SECURITY_QOS</a>



<a href="https://msdn.microsoft.com/2438816c-995e-4398-999d-48a3538eec18">RpcBindingSetAuthInfoEx</a>



<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>
 

 

