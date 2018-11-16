---
UID: NF:sspi.AcquireCredentialsHandleW
title: AcquireCredentialsHandleW function
author: windows-sdk-content
description: The AcquireCredentialsHandle (CredSSP) function acquires a handle to preexisting credentials of a security principal.
old-location: security\acquirecredentialshandle__credssp_.htm
tech.root: SecAuthN
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AcquireCredentialsHandle, AcquireCredentialsHandle (CredSSP), AcquireCredentialsHandle function [Security], AcquireCredentialsHandleA, AcquireCredentialsHandleW, SECPKG_CRED_INBOUND, SECPKG_CRED_OUTBOUND, security.acquirecredentialshandle__credssp_, sspi/AcquireCredentialsHandle, sspi/AcquireCredentialsHandleA, sspi/AcquireCredentialsHandleW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AcquireCredentialsHandleW (Unicode) and AcquireCredentialsHandleA (ANSI)
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
 - AcquireCredentialsHandle
 - AcquireCredentialsHandleA
 - AcquireCredentialsHandleW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- AcquireCredentialsHandleW
: 
---

# AcquireCredentialsHandleW function


## -description


The <b>AcquireCredentialsHandle (CredSSP)</b> function acquires a handle to preexisting <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a>. This handle is required by the 
<a href="https://msdn.microsoft.com/f3d8c07b-db28-4f26-ba29-8733fc95bdb5">InitializeSecurityContext (CredSSP)</a> and 
<a href="https://msdn.microsoft.com/a53f733e-b646-4431-b021-a2c446308849">AcceptSecurityContext (CredSSP)</a> functions. These can be either preexisting <i>credentials</i>, which are established through a system logon that is not described here, or the caller can provide alternative credentials.
			
<div class="alert"><b>Note</b>  This is not a "log on to the network" and does not imply gathering of credentials.</div><div> </div>

## -parameters




### -param pPrincipal

TBD


### -param pPackage

TBD


### -param fCredentialUse [in]

A flag that indicates how these credentials will be used. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CRED_INBOUND"></a><a id="secpkg_cred_inbound"></a><dl>
<dt><b>SECPKG_CRED_INBOUND</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Validate an incoming server credential. Inbound credentials might be validated by using an authenticating authority when <a href="https://msdn.microsoft.com/f3d8c07b-db28-4f26-ba29-8733fc95bdb5">InitializeSecurityContext (CredSSP)</a> or <a href="https://msdn.microsoft.com/a53f733e-b646-4431-b021-a2c446308849">AcceptSecurityContext (CredSSP)</a> is called. If such an authority is not available, the function will fail and return <b>SEC_E_NO_AUTHENTICATING_AUTHORITY</b>. Validation is package specific.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CRED_OUTBOUND"></a><a id="secpkg_cred_outbound"></a><dl>
<dt><b>SECPKG_CRED_OUTBOUND</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Allow a local client credential to prepare an outgoing token.

</td>
</tr>
</table>
 


### -param pvLogonId [in, optional]

A pointer to a  <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a> (LUID) that identifies the user. This parameter is provided for file-system processes such as network redirectors. This parameter can be <b>NULL</b>.


### -param pAuthData [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/b22bd22c-e6e1-4817-b5cf-ab49f574e75f">CREDSSP_CRED</a> structure that specifies authentication data for both Schannel and Negotiate packages.


### -param pGetKeyFn [in, optional]

Reserved. This parameter is not used and should be set to <b>NULL</b>.


### -param pvGetKeyArgument [in, optional]

Reserved. This parameter must be set to <b>NULL</b>.


### -param phCredential [out]

A pointer to the <a href="https://msdn.microsoft.com/94b622d0-7c04-4513-841f-0df9b5d49136">CredHandle</a> structure that will receive the credential handle.


### -param ptsExpiry [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/0a609b32-dbd7-4905-8990-65ebabcd0668">TimeStamp</a> structure that receives the time at which the returned credentials expire. The structure value received depends on the security package, which must specify the value in local time.


#### - pszPackage [in]

A pointer to a null-terminated string that specifies the name of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> with which these credentials will be used. This is a security package name returned in the <b>Name</b> member of a 
<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structure returned by the 
<a href="https://msdn.microsoft.com/900790a6-111d-43f5-9316-e85aab03a3bc">EnumerateSecurityPackages</a> function. After a context is established, 
<a href="https://msdn.microsoft.com/4956c4ab-b71e-4960-b750-f3a79b87baac">QueryContextAttributes (CredSSP)</a> can be called with <i>ulAttribute</i> set to <b>SECPKG_ATTR_PACKAGE_INFO</b> to return information on the security package in use.


#### - pszPrincipal [in, optional]

A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.

<div class="alert"><b>Note</b>  If the process that requests the handle does not have access to the credentials, the function returns an error. A null string indicates that the process requires a handle to the credentials of the user under whose <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> it is executing.</div>
<div> </div>

## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available to complete the requested action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred that did not map to an SSPI error code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NO_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
No credentials are available in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NOT_OWNER</b></dt>
</dl>
</td>
<td width="60%">
The caller of the function does not have the necessary credentials.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_SECPKG_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested security package does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_UNKNOWN_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
The credentials supplied to the package were not recognized.

</td>
</tr>
</table>
 




## -remarks



The <b>AcquireCredentialsHandle (CredSSP)</b> function returns a handle to the credentials of a principal, such as a user or client, as used by a specific <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>. The function can return the handle to either preexisting credentials or  newly created credentials and return it. This handle can be used in subsequent calls to the 
<a href="https://msdn.microsoft.com/a53f733e-b646-4431-b021-a2c446308849">AcceptSecurityContext (CredSSP)</a> and 
<a href="https://msdn.microsoft.com/f3d8c07b-db28-4f26-ba29-8733fc95bdb5">InitializeSecurityContext (CredSSP)</a> functions.

In general, <b>AcquireCredentialsHandle (CredSSP)</b> does not provide  the credentials of other users logged on to the same computer. However, a caller with SE_TCB_NAME  <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privilege</a> can obtain the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> of an existing logon session by specifying the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon identifier</a> (LUID) of that session. Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.

A package might call the function in <i>pGetKeyFn</i> provided by the RPC run-time transport. If the transport does not support the notion of callback to retrieve credentials, this parameter must be <b>NULL</b>.

For kernel mode callers, the following differences must be noted:

<ul>
<li>The two string parameters must be <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> strings.</li>
<li>The buffer values must be allocated in process virtual memory, not from the pool.</li>
</ul>
When you have finished using the returned credentials, free the memory used by the credentials by calling the 
<a href="https://msdn.microsoft.com/e089618c-8233-475a-9725-39265c6427ab">FreeCredentialsHandle</a> function.




## -see-also




<a href="https://msdn.microsoft.com/a53f733e-b646-4431-b021-a2c446308849">AcceptSecurityContext (CredSSP)</a>



<a href="https://msdn.microsoft.com/e089618c-8233-475a-9725-39265c6427ab">FreeCredentialsHandle</a>



<a href="https://msdn.microsoft.com/f3d8c07b-db28-4f26-ba29-8733fc95bdb5">InitializeSecurityContext (CredSSP)</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>
 

 

