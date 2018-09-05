---
UID: NF:rpcdce.RpcBindingInqAuthInfoW
title: RpcBindingInqAuthInfoW function
author: windows-sdk-content
description: The RpcBindingInqAuthInfo function returns authentication and authorization information from a binding handle.
old-location: rpc\rpcbindinginqauthinfo.htm
old-project: Rpc
ms.assetid: becb2c58-bfc7-47a7-ad2f-947ecf7bba2b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcBindingInqAuthInfo, RpcBindingInqAuthInfo function [RPC], RpcBindingInqAuthInfoA, RpcBindingInqAuthInfoW, _rpc_rpcbindinginqauthinfo, rpc.rpcbindinginqauthinfo, rpcdce/RpcBindingInqAuthInfo, rpcdce/RpcBindingInqAuthInfoA, rpcdce/RpcBindingInqAuthInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcBindingInqAuthInfoW (Unicode) and RpcBindingInqAuthInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcBindingInqAuthInfo
 - RpcBindingInqAuthInfoA
 - RpcBindingInqAuthInfoW
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcBindingInqAuthInfoW function


## -description


The 
<b>RpcBindingInqAuthInfo</b> function returns authentication and authorization information from a binding handle.


## -parameters




### -param Binding

Server binding handle from which authentication and authorization information is returned.


### -param ServerPrincName

Returns a pointer to a pointer to the expected principal name of the server referenced in <i>Binding</i>. The content of the returned name and its syntax are defined by the authentication service in use.

Specify a null value to prevent 
<b>RpcBindingInqAuthInfo</b> from returning the <i>ServerPrincName</i> parameter. In this case, the application does not call the 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function.


### -param AuthnLevel

Returns a pointer set to the level of authentication used for remote procedure calls made using <i>Binding</i>. See Note.

Specify a null value to prevent the function from returning the <i>AuthnLevel</i> parameter.

The level returned in the <i>AuthnLevel</i> parameter may be different from the level specified when the client called the 
<a href="https://msdn.microsoft.com/2db946b6-6a0d-402c-89ef-68c7489aa7ee">RpcBindingSetAuthInfo</a> function. This discrepancy occurs when the RPC run-time library does not support the authentication level specified by the client and automatically upgrades to the next higher authentication level.


### -param AuthnSvc

Returns a pointer set to the authentication service specified for remote procedure calls made using <i>Binding</i>. See Note.

Specify a null value to prevent 
<b>RpcBindingInqAuthInfo</b> from returning the <i>AuthnSvc</i> parameter.


### -param AuthIdentity

Returns a pointer to a handle to the data structure that contains the client's authentication and authorization credentials specified for remote procedure calls made using <i>Binding</i>.

Specify a null value to prevent 
<b>RpcBindingInqAuthInfo</b> from returning the <i>AuthIdentity</i> parameter.


### -param AuthzSvc

Returns a pointer set to the authorization service requested by the client application that made the remote procedure call on <i>Binding</i> See Note.

Specify a null value to prevent 
<b>RpcBindingInqAuthInfo</b> from returning the <i>AuthzSvc</i> parameter.

<div class="alert"><b>Note</b>  For a list of the RPC-supported authentication services, see 
<a href="https://msdn.microsoft.com/ac95276f-230d-4993-92fe-1739d022c8b3">Authentication-Service Constants</a>.</div>
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
<b>RpcBindingInqAuthInfo</b> function to view the authentication and authorization information associated with a server binding handle. A similar function, 
<a href="https://msdn.microsoft.com/e75f5ba6-7a1c-4069-8810-05aa38a47e9c">RpcBindingInqAuthInfoEx</a> additionally provides security quality-of-service information on the binding handle.

The RPC run-time library allocates memory for the returned <i>ServerPrincName</i> parameter. The application is responsible for calling the 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function for that returned argument string.




## -see-also




<a href="https://msdn.microsoft.com/2834a6a8-8bd6-4829-84ea-e3f35c917ab7">RpcBindingInqAuthClient</a>



<a href="https://msdn.microsoft.com/e75f5ba6-7a1c-4069-8810-05aa38a47e9c">RpcBindingInqAuthInfoEx</a>



<a href="https://msdn.microsoft.com/f148c827-d18a-41f2-834a-f6b77b331bcc">RpcBindingInqOption</a>



<a href="https://msdn.microsoft.com/2db946b6-6a0d-402c-89ef-68c7489aa7ee">RpcBindingSetAuthInfo</a>



<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>
 

 

