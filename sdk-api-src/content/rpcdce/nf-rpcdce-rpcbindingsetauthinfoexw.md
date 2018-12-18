---
UID: NF:rpcdce.RpcBindingSetAuthInfoExW
title: RpcBindingSetAuthInfoExW function
author: windows-sdk-content
description: The RpcBindingSetAuthInfoEx function sets a binding handle's authentication, authorization, and security quality-of-service information.
old-location: rpc\rpcbindingsetauthinfoex.htm
tech.root: rpc
ms.assetid: 2438816c-995e-4398-999d-48a3538eec18
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcBindingSetAuthInfoEx, RpcBindingSetAuthInfoEx function [RPC], RpcBindingSetAuthInfoExA, RpcBindingSetAuthInfoExW, _rpc_rpcbindingsetauthinfoex, rpc.rpcbindingsetauthinfoex, rpcdce/RpcBindingSetAuthInfoEx, rpcdce/RpcBindingSetAuthInfoExA, rpcdce/RpcBindingSetAuthInfoExW
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcBindingSetAuthInfoExW (Unicode) and RpcBindingSetAuthInfoExA (ANSI)
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
 - RpcBindingSetAuthInfoEx
 - RpcBindingSetAuthInfoExA
 - RpcBindingSetAuthInfoExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcBindingSetAuthInfoExW function


## -description


The 
<b>RpcBindingSetAuthInfoEx</b> function sets a binding handle's authentication, authorization, and security quality-of-service information.


## -parameters




### -param Binding

Server binding handle into which authentication and authorization information is set.


### -param ServerPrincName

Pointer to the expected principal name of the server referenced by <i>Binding</i>. The content of the name and its syntax are defined by the authentication service in use.

<div class="alert"><b>Note</b>  For the set of allowable target names for SSPs, please refer to the comments in the <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext</a> documentation.</div>
<div> </div>

### -param AuthnLevel

Level of authentication to be performed on remote procedure calls made using <i>Binding</i>. For a list of the RPC-supported authentication levels, see 
<a href="https://msdn.microsoft.com/b8bb2517-e1a0-4607-a672-259f8686fc3e">Authentication-Level Constants</a>.


### -param AuthnSvc

Authentication service to use.

Specify RPC_C_AUTHN_NONE to turn off authentication for remote procedure calls made using <i>Binding</i>.

If RPC_C_AUTHN_DEFAULT is specified, the RPC run-time library uses the RPC_C_AUTHN_WINNT authentication service for remote procedure calls made using <i>Binding</i>.


### -param AuthIdentity

Handle for the structure that contains the client's authentication and authorization credentials appropriate for the selected authentication and authorization service. 




When using the <a href="https://msdn.microsoft.com/ac95276f-230d-4993-92fe-1739d022c8b3">RPC_C_AUTHN_WINNT</a>authentication service <i>AuthIdentity</i> should be a pointer to a 
<a href="https://msdn.microsoft.com/829dee24-aeeb-4191-b5fc-85970725f064">SEC_WINNT_AUTH_IDENTITY</a> structure (defined in Rpcdce.h). Kerberos and Negotiate authentication services also use the 
<b>SEC_WINNT_AUTH_IDENTITY</b> structure.

Specify a null value to use the security login context for the current address space. Pass the value RPC_C_NO_CREDENTIALS to use an anonymous log-in context. Note that RPC_C_NO_CREDENTIALS is only valid if RPC_C_AUTHN_GSS_SCHANNEL is selected as the authentication service.


### -param AuthzSvc

Authorization service implemented by the server for the interface of interest. The validity and trustworthiness of authorization data, like any application data, depends on the authentication service and authentication level selected. This parameter is ignored when using the RPC_C_AUTHN_WINNT authentication service. See Note.


#### - SecurityQOS

Pointer to the 
<a href="https://msdn.microsoft.com/f7733b9d-ae32-44ff-b1ca-dd0292dd0ff6">RPC_SECURITY_QOS</a> structure, which defines the security quality-of-service. 




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
<dt><b>RPC_S_UNKNOWN_AUTHN_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
Unknown authentication service.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A client application calls the 
<b>RpcBindingSetAuthInfoEx</b> function to set up a server binding handle for making authenticated remote procedure calls. This function provides the capability to set security quality-of-service information on the binding handle. It is otherwise identical to 
<a href="https://msdn.microsoft.com/2db946b6-6a0d-402c-89ef-68c7489aa7ee">RpcBindingSetAuthInfo</a>.

Unless a client calls 
<b>RpcBindingSetAuthInfoEx</b>, all remote procedure calls on <i>Binding</i> are unauthenticated. A client is not required to call this function.

The 
<b>RpcBindingSetAuthInfoEx</b> function takes a snapshot of the credentials. Therefore, the memory dedicated to the <i>AuthIdentity</i> parameter can be freed before the binding handle. The exception to this is when your application uses 
<b>RpcBindingSetAuthInfoEx</b> with RPC_C_QOS_IDENTITY_DYNAMIC and also specifies a non-<b>NULL</b> value for <i>AuthIdentity</i>.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/2db946b6-6a0d-402c-89ef-68c7489aa7ee">RpcBindingSetAuthInfo</a> function must not be called on a binding handle while an RPC call on the same handle is in progress. Doing so produces undefined results.</div>
<div> </div>
Due to the varying requirements of different versions of Microsoft RPC, Microsoft recommends that an application maintain a pointer to the <i>AuthIdentity</i> parameter for as long as the binding handle exists. Doing so increases the applications portability.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>For Windows XP SP2 and Windows Server 2003 SP1, the pointer to the <i>AuthIdentity</i> parameter need not be maintained for the life of the binding handle. This pointer must only be maintained if subsequent calls to <a href="https://msdn.microsoft.com/becb2c58-bfc7-47a7-ad2f-947ecf7bba2b">RpcBindingInqAuthInfo</a> or <a href="https://msdn.microsoft.com/e75f5ba6-7a1c-4069-8810-05aa38a47e9c">RpcBindingInqAuthInfoEx</a> are made.

<div class="alert"><b>Note</b>  The <b>ncalrpc</b> protocol sequence supports only RPC_C_AUTHN_WINNT, but does support mutual authentication; supply an SPN and request mutual authentication through the <i>SecurityQOS</i> parameter to achieve this.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f7733b9d-ae32-44ff-b1ca-dd0292dd0ff6">RPC_SECURITY_QOS</a>



<a href="https://msdn.microsoft.com/e75f5ba6-7a1c-4069-8810-05aa38a47e9c">RpcBindingInqAuthInfoEx</a>



<a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a>
 

 

