---
UID: NC:ntsecpkg.SpAddCredentialsFn
title: SpAddCredentialsFn (ntsecpkg.h)
description: Used to add credentials for a security principal.
helpviewer_keywords: ["SECPKG_CRED_INBOUND","SECPKG_CRED_OUTBOUND","SpAddCredentials","SpAddCredentials callback function [Security]","SpAddCredentialsFn","SpAddCredentialsFn callback","_ssp_spaddcredentials","ntsecpkg/SpAddCredentials","security.spaddcredentials"]
old-location: security\spaddcredentials.htm
tech.root: security
ms.assetid: 27377afa-4e54-4c6b-8e84-a8810bc01139
ms.date: 12/05/2018
ms.keywords: SECPKG_CRED_INBOUND, SECPKG_CRED_OUTBOUND, SpAddCredentials, SpAddCredentials callback function [Security], SpAddCredentialsFn, SpAddCredentialsFn callback, _ssp_spaddcredentials, ntsecpkg/SpAddCredentials, security.spaddcredentials
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
 - SpAddCredentialsFn
 - ntsecpkg/SpAddCredentialsFn
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
 - SpAddCredentials
---

# SpAddCredentialsFn callback function


## -description

Used to add <a href="/windows/desktop/SecGloss/c-gly">credentials</a> for a <a href="/windows/desktop/SecGloss/s-gly">security principal</a>.

## -parameters

### -param CredentialHandle [in]

A handle to the credential to add.

### -param PrincipalName [in]

Optional. Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure containing the name of the <a href="/windows/desktop/SecGloss/s-gly">security principal</a> whose credentials are being added.

### -param Package [in]

Pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure containing the name of the authenticating package.

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

### -param AuthorizationData [in]

Optional. Pointer to supplemental authentication data.

### -param GetKeyFunction [in]

Pointer to a function in the caller's address space that generates <a href="/windows/desktop/SecGloss/s-gly">session keys</a>.


### -param GetKeyArgument [in]

Pointer to the argument used with the <i>GetKeyFunction</i> function.

### -param ExpirationTime [out]

Pointer to a 
<a href="/windows/desktop/SecAuthN/timestamp">TimeStamp</a> that receives the time the credentials handle expires.


## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.

## -remarks

SSP/APs must implement the <b>SpAddCredentials</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpAddCredentials</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>