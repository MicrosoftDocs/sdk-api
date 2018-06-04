---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RpcGetAuthorizationContextForClient function


## -description


The 
<b>RpcGetAuthorizationContextForClient</b> function returns the Authz context for an RPC client that can be used with Authz functions for high-performance authentication. Supported for <b>ncalrpc</b> and <b>ncacn_*</b> protocol sequences only.


## -parameters




### -param ClientBinding [in, optional]

Binding handle on the server that represents a binding to a client. The server impersonates the client indicated by this handle. If a value of zero is specified, the server impersonates the client that is being served by this server thread.


### -param ImpersonateOnReturn [in]

Directs the function to impersonate the client on return, and then return an <b>AUTHZ_CLIENT_CONTEXT_HANDLE</b> structure. Set this parameter to nonzero to impersonate the client. See Remarks.


### -param Reserved1 [in]

Reserved. Must be null.


### -param pExpirationTime [in, optional]

Pointer to the expiration date and time of the token. If no value is passed, the token never expires. Expiration time is not currently enforced.


### -param Reserved2 [in]

Reserved. Must be a <b>LUID</b> structure with each member set to zero.


### -param Reserved3 [in]

Reserved. Must be zero.


### -param Reserved4 [in]

Reserved. Must be null.


### -param pAuthzClientContext [out]

Pointer to an <b>AUTHZ_CLIENT_CONTEXT_HANDLE</b> structure that can be passed directly to Authz functions. If the function fails, the content of this parameter is undefined.


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
<dt><b>RERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A reserved parameter is different than its prescribed value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_CONTEXT_AVAILABLE </b></dt>
</dl>
</td>
<td width="60%">
The RPC client has not been authenticated successfully.

</td>
</tr>
</table>
 

Failure returns an RPC_S_* error code, or a Windows error code. Extended error information is available through standard RPC or Windows error code retrieval mechanisms. For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.




## -remarks



The 
<b>RpcGetAuthorizationContextForClient</b> function can be called in the same context as the 
<b>RpcImpersonateClient</b> function. All functions that impersonate check to determine whether the caller has the SeImpersonatePrivilege privilege. If the caller has the SeImpersonatePrivilege, or if the authenticated identity is the same as the caller, the requested impersonation is allowed. Otherwise, the impersonation succeeds at Identify level only.

<b>Note</b>  The SeImpersonatePrivilege privilege is not supported until Windows XP with Service Pack 2 (SP2).

The 
<b>RpcGetAuthorizationContextForClient</b> function is supported for ncalrpc and ncacn_* protocol sequences only, and is not supported on named pipes that only implement transport security.

The 
<b>RpcGetAuthorizationContextForClient</b> function is thread-safe, and can be called from multiple threads. The context returned in <i>pAuthzClientContext</i> is independent of the function call, and can be used subsequent to its completion. The caller is responsible for freeing the context with a call to the 
<a href="https://msdn.microsoft.com/ad6117e1-3244-42dd-b513-d5b2c28e8e10">RpcFreeAuthorizationContext</a> function.

Performance improvement observed by using the 
<b>RpcGetAuthorizationContextForClient</b> function, when compared to previous methods of impersonation or access check or revert to self, depend on the following factors:

<ul>
<li>How many times the function is called for a given client identity.</li>
<li>Protocol sequence and identity tracking in effect for the function call.</li>
</ul>
Subsequent calls to the 
<b>RpcGetAuthorizationContextForClient</b> function for the same client identity have an extremely low cost. This efficiency is achieved by results from previous inquiries being cached, and responses being returned from the cache whenever possible.

Calls over ncalrpc with static identity tracking execute the 
<b>RpcGetAuthorizationContextForClient</b> function faster than calls over ncalrpc with dynamic identity tracking. Calls over ncacn_* execute with approximately the same speed for a given protocol sequence, regardless of whether identity tracking is static or dynamic.




## -see-also




<a href="https://msdn.microsoft.com/c236f335-b5de-4e8b-851d-45e008791271">Client/Server Access
		  Control Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>



<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return
		  Values</a>



<a href="https://msdn.microsoft.com/ad6117e1-3244-42dd-b513-d5b2c28e8e10">RpcFreeAuthorizationContext</a>



<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a>
 

 

