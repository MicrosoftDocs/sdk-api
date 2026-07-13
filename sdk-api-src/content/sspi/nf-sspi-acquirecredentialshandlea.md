---
UID: NF:sspi.AcquireCredentialsHandleA
title: AcquireCredentialsHandleA function (sspi.h)
description: The AcquireCredentialsHandle (CredSSP) function acquires a handle to preexisting credentials of a security principal. (ANSI)
helpviewer_keywords: ["AcquireCredentialsHandleA", "SECPKG_CRED_INBOUND", "SECPKG_CRED_OUTBOUND", "sspi/AcquireCredentialsHandleA"]
old-location: security\acquirecredentialshandle__credssp_.htm
tech.root: security
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
ms.date: 12/05/2018
ms.keywords: AcquireCredentialsHandle, AcquireCredentialsHandle (CredSSP), AcquireCredentialsHandle function [Security], AcquireCredentialsHandleA, AcquireCredentialsHandleW, SECPKG_CRED_INBOUND, SECPKG_CRED_OUTBOUND, security.acquirecredentialshandle__credssp_, sspi/AcquireCredentialsHandle, sspi/AcquireCredentialsHandleA, sspi/AcquireCredentialsHandleW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AcquireCredentialsHandleA
 - sspi/AcquireCredentialsHandleA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
 - schannel.dll
api_name:
 - AcquireCredentialsHandle
 - AcquireCredentialsHandleA
 - AcquireCredentialsHandleW
---

# AcquireCredentialsHandleA function


## -description

The <b>AcquireCredentialsHandle (CredSSP)</b> function acquires a handle to preexisting <a href="/windows/desktop/SecGloss/c-gly">credentials</a> of a <a href="/windows/desktop/SecGloss/s-gly">security principal</a>. This handle is required by the 
<a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (CredSSP)</a> and 
<a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (CredSSP)</a> functions. These can be either preexisting <i>credentials</i>, which are established through a system logon that is not described here, or the caller can provide alternative credentials.
			
<div class="alert"><b>Note</b>  This is not a "log on to the network" and does not imply gathering of credentials.</div><div> </div>

## -parameters

### -param pszPrincipal [in, optional]

A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.

<div class="alert"><b>Note</b>  If the process that requests the handle does not have access to the credentials, the function returns an error. A null string indicates that the process requires a handle to the credentials of the user under whose <a href="/windows/desktop/SecGloss/s-gly">security context</a> it is executing.</div>
<div> </div>

### -param pszPackage [in]

A pointer to a null-terminated string that specifies the name of the <a href="/windows/desktop/SecGloss/s-gly">security package</a> with which these credentials will be used. This is a security package name returned in the <b>Name</b> member of a 
<a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structure returned by the 
<a href="/windows/desktop/api/sspi/nf-sspi-enumeratesecuritypackagesa">EnumerateSecurityPackages</a> function. After a context is established, 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (CredSSP)</a> can be called with <i>ulAttribute</i> set to <b>SECPKG_ATTR_PACKAGE_INFO</b> to return information on the security package in use.

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
Validate an incoming server credential. Inbound credentials might be validated by using an authenticating authority when <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (CredSSP)</a> or <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (CredSSP)</a> is called. If such an authority is not available, the function will fail and return <b>SEC_E_NO_AUTHENTICATING_AUTHORITY</b>. Validation is package specific.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CRED_OUTBOUND"></a><a id="secpkg_cred_outbound"></a><dl>
<dt><b>SECPKG_CRED_OUTBOUND</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Allow a local client credential to prepare an outgoing token.

</td>
</tr>
</table>

### -param pvLogonId [in, optional]

A pointer to a  <a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a> (LUID) that identifies the user. This parameter is provided for file-system processes such as network redirectors. This parameter can be <b>NULL</b>.

### -param pAuthData [in, optional]

A pointer to a <a href="/windows/desktop/api/credssp/ns-credssp-credssp_cred">CREDSSP_CRED</a> structure that specifies authentication data for both Schannel and Negotiate packages.

### -param pGetKeyFn [in, optional]

Reserved. This parameter is not used and should be set to <b>NULL</b>.

### -param pvGetKeyArgument [in, optional]

Reserved. This parameter must be set to <b>NULL</b>.

### -param phCredential [out]

A pointer to the <a href="/windows/desktop/SecAuthN/sspi-handles">CredHandle</a> structure that will receive the credential handle.

### -param ptsExpiry [out, optional]

A pointer to a <a href="/windows/desktop/SecAuthN/timestamp">TimeStamp</a> structure that receives the time at which the returned credentials expire. The structure value received depends on the security package, which must specify the value in local time.

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
No credentials are available in the <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

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

The <b>AcquireCredentialsHandle (CredSSP)</b> function returns a handle to the credentials of a principal, such as a user or client, as used by a specific <a href="/windows/desktop/SecGloss/s-gly">security package</a>. The function can return the handle to either preexisting credentials or  newly created credentials and return it. This handle can be used in subsequent calls to the 
<a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (CredSSP)</a> and 
<a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (CredSSP)</a> functions.

In general, <b>AcquireCredentialsHandle (CredSSP)</b> does not provide  the credentials of other users logged on to the same computer. However, a caller with SE_TCB_NAME  <a href="/windows/desktop/SecGloss/p-gly">privilege</a> can obtain the <a href="/windows/desktop/SecGloss/c-gly">credentials</a> of an existing logon session by specifying the <a href="/windows/desktop/SecGloss/l-gly">logon identifier</a> (LUID) of that session. Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.

A package might call the function in <i>pGetKeyFn</i> provided by the RPC run-time transport. If the transport does not support the notion of callback to retrieve credentials, this parameter must be <b>NULL</b>.

For kernel mode callers, the following differences must be noted:

<ul>
<li>The two string parameters must be <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> strings.</li>
<li>The buffer values must be allocated in process virtual memory, not from the pool.</li>
</ul>
When you have finished using the returned credentials, free the memory used by the credentials by calling the 
<a href="/windows/desktop/api/sspi/nf-sspi-freecredentialshandle">FreeCredentialsHandle</a> function.





> [!NOTE]
> The sspi.h header defines AcquireCredentialsHandle as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (CredSSP)</a>



<a href="/windows/desktop/api/sspi/nf-sspi-freecredentialshandle">FreeCredentialsHandle</a>



<a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (CredSSP)</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>
