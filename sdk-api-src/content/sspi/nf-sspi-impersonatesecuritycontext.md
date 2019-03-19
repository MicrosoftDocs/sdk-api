---
UID: NF:sspi.ImpersonateSecurityContext
title: ImpersonateSecurityContext function (sspi.h)
author: windows-sdk-content
description: Allows a server to impersonate a client by using a token previously obtained by a call to AcceptSecurityContext (General) or QuerySecurityContextToken.
old-location: security\impersonatesecuritycontext.htm
tech.root: SecAuthN
ms.assetid: 167eaf3b-b794-4587-946d-fa596f1f9411
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImpersonateSecurityContext, ImpersonateSecurityContext function [Security], _ssp_impersonatesecuritycontext, security.impersonatesecuritycontext, sspi/ImpersonateSecurityContext
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - ImpersonateSecurityContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImpersonateSecurityContext function


## -description


The <b>ImpersonateSecurityContext</b> function allows a server to impersonate a client by using a token previously obtained by a call to <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> or <a href="https://msdn.microsoft.com/5dc23608-9ce3-4fee-8161-2e409cef4063">QuerySecurityContextToken</a>. This function allows the application server to act as the client, and thus all necessary access controls are enforced.


## -parameters




### -param phContext [in]

The handle of the context to impersonate. This handle must have been obtained by a call to the 
<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> function.


## -returns



If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle passed to the function is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NO_IMPERSONATION</b></dt>
</dl>
</td>
<td width="60%">
The client could not be impersonated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_UNSUPPORTED_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
This value is returned by Schannel kernel mode to indicate that this function is not supported.

</td>
</tr>
</table>
 




## -remarks



The server application calls the <b>ImpersonateSecurityContext</b> function when it needs to impersonate the client. Before doing so, the server must have obtained a valid context handle. To obtain the context handle, the server must call 
<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> to submit the client's incoming security token to the security system. The server gets a context handle if the inbound context is validated. The function creates an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> and allows the thread or process to run with the impersonation context.

When using the Schannel <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP), the server application must pass the <b>ASC_REQ_MUTUAL_AUTH</b> flag when calling <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a>. This ensures that the client is asked for a client certificate during the SSL/TLS handshake. When a client certificate is received, the Schannel package verifies the client certificate and attempts to map it to a user account. When this mapping is successful, then a client user token is created and this function succeeds.

The application server must call the 
<a href="https://msdn.microsoft.com/d4ed1fe9-2e0a-4648-a010-1eae49ba03ee">RevertSecurityContext</a> function when it finishes or when it needs to restore its own <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.

<b>ImpersonateSecurityContext</b> is not available with all <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security packages</a> on all platforms. Typically, it is implemented only on platforms and with security packages that support impersonation. To learn whether a security package supports impersonation, call the 
<a href="https://msdn.microsoft.com/130ef0fe-bb13-4a65-b476-cd25ed234da1">QuerySecurityPackageInfo</a> function.

<div class="alert"><b>Note</b>  If the <b>ImpersonateSecurityContext</b> function fails, the client is not impersonated, and all subsequent client requests are made in the security context of the process that called the function. If the calling process is running as a privileged account, it can perform actions that the client would not be allowed to perform. To avoid security risks, the calling process should always check the return value. If the return value indicates that the function call failed, no client requests should be executed.</div>
<div> </div>
All impersonate functions, including <b>ImpersonateSecurityContext</b> allow the requested impersonation if one of the following is true: 



<ul>
<li>The requested impersonation level of the token is less than <b>SecurityImpersonation</b>, such as <b>SecurityIdentification</b> or <b>SecurityAnonymous</b>.</li>
<li>The caller has the <b>SeImpersonatePrivilege</b> privilege.</li>
<li>A process (or another process in the caller's logon session) created the token using explicit credentials through <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> or <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function.</li>
<li>The authenticated identity is same as the caller.</li>
</ul>
<b>Windows XP with SP1 and earlier:  </b>The <b>SeImpersonatePrivilege</b> privilege is not supported.

<b>Windows XP:  </b>The SeImpersonatePrivilege privilege is not supported until Windows XP with Service Pack 2 (SP2).




## -see-also




<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a>



<a href="https://msdn.microsoft.com/130ef0fe-bb13-4a65-b476-cd25ed234da1">QuerySecurityPackageInfo</a>



<a href="https://msdn.microsoft.com/d4ed1fe9-2e0a-4648-a010-1eae49ba03ee">RevertSecurityContext</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>
 

 

