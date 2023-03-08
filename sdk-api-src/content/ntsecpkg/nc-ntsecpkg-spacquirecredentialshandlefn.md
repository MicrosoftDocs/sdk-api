---
UID: NC:ntsecpkg.SpAcquireCredentialsHandleFn
title: SpAcquireCredentialsHandleFn (ntsecpkg.h)
description: Called to obtain a handle to a principal's credentials.
helpviewer_keywords: ["SECPKG_CRED_INBOUND","SECPKG_CRED_OUTBOUND","SpAcquireCredentialsHandle","SpAcquireCredentialsHandle callback function [Security]","SpAcquireCredentialsHandleFn","SpAcquireCredentialsHandleFn callback","_ssp_spacquirecredentialshandle","ntsecpkg/SpAcquireCredentialsHandle","security.spacquirecredentialshandle"]
old-location: security\spacquirecredentialshandle.htm
tech.root: security
ms.assetid: d01245d9-fbca-4346-acf5-86ae7f0eb01e
ms.date: 12/05/2018
ms.keywords: SECPKG_CRED_INBOUND, SECPKG_CRED_OUTBOUND, SpAcquireCredentialsHandle, SpAcquireCredentialsHandle callback function [Security], SpAcquireCredentialsHandleFn, SpAcquireCredentialsHandleFn callback, _ssp_spacquirecredentialshandle, ntsecpkg/SpAcquireCredentialsHandle, security.spacquirecredentialshandle
req.header: ntsecpkg.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpAcquireCredentialsHandleFn
 - ntsecpkg/SpAcquireCredentialsHandleFn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpAcquireCredentialsHandle
---

# SpAcquireCredentialsHandleFn callback function


## -description

Called to obtain a handle to a principal's <a href="/windows/desktop/SecGloss/c-gly">credentials</a>. The <a href="/windows/desktop/SecGloss/s-gly">security package</a> can deny access to the caller if the caller does not have permission to access the credentials.

If the credentials handle is returned to the caller, the package should also specify an expiration time for the handle.

## -parameters

### -param PrincipalName [in]

Optional. Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure containing the name of the <a href="/windows/desktop/SecGloss/s-gly">security principal</a> whose credentials are being requested. If this value is <b>NULL</b>, the caller requests a handle to the credentials of the user in whose <a href="/windows/desktop/SecGloss/s-gly">security context</a> the caller is executing.

### -param CredentialUseFlags [in]

Flags indicating how the credentials will be used. The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CRED_INBOUND"></a><a id="secpkg_cred_inbound"></a><dl>
<dt><b>SECPKG_CRED_INBOUND</b></dt>
</dl>
</td>
<td width="60%">
Credentials will be used with the 
<a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CRED_OUTBOUND"></a><a id="secpkg_cred_outbound"></a><dl>
<dt><b>SECPKG_CRED_OUTBOUND</b></dt>
</dl>
</td>
<td width="60%">
Credentials will be used with the 
<a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a> function.

</td>
</tr>
</table>

### -param LogonId [in]

Optional. Pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> containing the <a href="/windows/desktop/SecGloss/l-gly">logon identifier</a> of the security principal.

### -param AuthorizationData [in]

Optional. Pointer to supplemental authentication data.

### -param GetKeyFunction [in]

Pointer to a function in the caller's address space that generates <a href="/windows/desktop/SecGloss/s-gly">session keys</a>.


### -param GetKeyArgument [in]

Pointer to the argument used with the <i>GetKeyFunction</i> function.

### -param CredentialHandle [out]

Pointer to an <b>LSA_SEC_HANDLE</b> that receives the credentials. When you have finished using the credentials, free the handle by calling the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spfreecredentialshandlefn">SpFreeCredentialsHandle</a> function.

### -param ExpirationTime [out]

Pointer to a 
<a href="/windows/desktop/SecAuthN/timestamp">TimeStamp</a> that receives the time the credentials handle expires.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following table lists common reasons for failure and the error codes that should be returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NOT_OWNER</b></dt>
</dl>
</td>
<td width="60%">
The caller is denied access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NO_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
There are no credentials available for the specified principal.

</td>
</tr>
</table>

## -remarks

The package can use the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) support functions to determine whether the caller should be given access to the requested credentials.

Credentials obtained from <b>SpAcquireCredentialsHandle</b> are freed by calling the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spfreecredentialshandlefn">SpFreeCredentialsHandle</a> function.

SSP/APs must implement the <b>SpAcquireCredentialsHandle</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpAcquireCredentialsHandle</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spfreecredentialshandlefn">SpFreeCredentialsHandle</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>