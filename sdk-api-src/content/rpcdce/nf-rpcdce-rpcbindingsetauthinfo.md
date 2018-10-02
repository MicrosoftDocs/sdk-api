---
UID: NF:rpcdce.RpcBindingSetAuthInfo
title: RpcBindingSetAuthInfo function
author: windows-sdk-content
description: The RpcBindingSetAuthInfo function sets a binding handle's authentication and authorization information.
old-location: rpc\rpcbindingsetauthinfo.htm
tech.root: Rpc
ms.assetid: 2db946b6-6a0d-402c-89ef-68c7489aa7ee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RpcBindingSetAuthInfo, RpcBindingSetAuthInfo function [RPC], RpcBindingSetAuthInfoA, RpcBindingSetAuthInfoW, _rpc_rpcbindingsetauthinfo, rpc.rpcbindingsetauthinfo, rpcdce/RpcBindingSetAuthInfo, rpcdce/RpcBindingSetAuthInfoA, rpcdce/RpcBindingSetAuthInfoW
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
req.unicode-ansi: RpcBindingSetAuthInfoW (Unicode) and RpcBindingSetAuthInfoA (ANSI)
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
 - RpcBindingSetAuthInfo
 - RpcBindingSetAuthInfoA
 - RpcBindingSetAuthInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcBindingSetAuthInfo function


## -description


The 
<b>RpcBindingSetAuthInfo</b> function sets a binding handle's authentication and authorization information.


## -parameters




### -param Binding

Server binding handle to which authentication and authorization information is to be applied.


### -param ServerPrincName

Pointer to the expected principal name of the server referenced by <i>Binding</i>. The content of the name and its syntax are defined by the authentication service in use. 

<div class="alert"><b>Note</b>  For the set of allowable target names for SSPs, please refer to the comments in the <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext</a> documentation.</div>
<div> </div>

### -param AuthnLevel

Level of authentication to be performed on remote procedure calls made using <i>Binding</i>. For a list of the RPC-supported authentication levels, see the list of 
<a href="https://msdn.microsoft.com/b8bb2517-e1a0-4607-a672-259f8686fc3e">Authentication-Level Constants</a>.


### -param AuthnSvc

Authentication service to use. See Note. 




Specify RPC_C_AUTHN_NONE to turn off authentication for remote procedure calls made using <i>Binding</i>.

If RPC_C_AUTHN_DEFAULT is specified, the RPC run-time library uses the RPC_C_AUTHN_WINNT authentication service for remote procedure calls made using <i>Binding</i>.


### -param AuthIdentity

Handle to the structure containing the client's authentication and authorization credentials appropriate for the selected authentication and authorization service.When using the RPC_C_AUTHN_WINNT authentication service <i>AuthIdentity</i> should be a pointer to a 
<a href="https://msdn.microsoft.com/829dee24-aeeb-4191-b5fc-85970725f064">SEC_WINNT_AUTH_IDENTITY</a> structure (defined in Rpcdce.h). Kerberos and Negotiate authentication services also use the 
<b>SEC_WINNT_AUTH_IDENTITY</b> structure. 




When you select the RPC_C_AUTHN_GSS_SCHANNEL authentication service, the <i>AuthIdentity</i> parameter should be a pointer to an <b>SCHANNEL_CRED</b> structure (defined in Schannel.h). Specify a null value to use the security login context for the current address space. Pass the value RPC_C_NO_CREDENTIALS to use an anonymous log-in context.

<div class="alert"><b>Note</b>  When selecting the RPC_C_AUTHN_GSS_SCHANNEL authentication service, the <i>AuthIdentity</i> parameter may also be a pointer to a <b>SCH_CRED</b> structure. However, in Windows XP and later releases of Windows, the only acceptable structure to be passed as the <i>AuthIdentity</i> parameter for the RPC_C_AUTHN_GSS_SCHANNEL authentication service is the <b>SCHANNEL_CRED</b> structure.</div>
<div> </div>

### -param AuthzSvc

Authorization service implemented by the server for the interface of interest. See Note. 




The validity and trustworthiness of authorization data, like any application data, depends on the authentication service and authentication level selected. This parameter is ignored when using the RPC_C_AUTHN_WINNT authentication service.

<div class="alert"><b>Note</b>  For more information, see 
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
<b>RpcBindingSetAuthInfo</b> function to set up a server binding handle for making authenticated remote procedure calls. A client is not required to call this function.

Unless a client calls 
<b>RpcBindingSetAuthInfo</b>, no remote procedure calls on the <i>Binding</i> binding handle are authenticated. A server can call 
<a href="https://msdn.microsoft.com/2834a6a8-8bd6-4829-84ea-e3f35c917ab7">RpcBindingInqAuthClient</a> from within a remote procedure call to determine whether that call has been authenticated.

The 
<b>RpcBindingSetAuthInfo</b> function takes a snapshot of the credentials. Therefore, the memory dedicated to the <i>AuthIdentity</i> parameter can be freed before the binding handle.

Due to varying requirements of different versions of Microsoft RPC, Microsoft recommends that your application maintain a pointer to the <i>AuthIdentity</i> parameter for as long as the binding handle exists. Doing so increases the application's portability.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>For Windows XP SP2 and Windows Server 2003 SP1, the pointer to the <i>AuthIdentity</i> parameter need not be maintained for the life of the binding handle. This pointer must only be maintained if subsequent calls to <a href="https://msdn.microsoft.com/becb2c58-bfc7-47a7-ad2f-947ecf7bba2b">RpcBindingInqAuthInfo</a> or <a href="https://msdn.microsoft.com/e75f5ba6-7a1c-4069-8810-05aa38a47e9c">RpcBindingInqAuthInfoEx</a> are made.

<div class="alert"><b>Note</b>  The <b>RpcBindingSetAuthInfo</b> function must not be called on a binding handle while an RPC call on the same handle is in progress. Doing so produces undefined results.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f4d45c4-7457-4449-8736-e141a95f6930">MSMQ Security
		  Services</a>



<a href="https://msdn.microsoft.com/becb2c58-bfc7-47a7-ad2f-947ecf7bba2b">RpcBindingInqAuthInfo</a>



<a href="https://msdn.microsoft.com/bc721fb0-2271-4658-995b-a41e8eefc5d5">RpcBindingSetOption</a>



<a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a>
 

 

