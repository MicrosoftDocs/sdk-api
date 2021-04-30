---
UID: NC:ntsecpkg.CredReadDomainCredentialsFn
title: CredReadDomainCredentialsFn (ntsecpkg.h)
description: Reads a domain credential from the Credential Manager.
helpviewer_keywords: ["CREDP_FLAGS_CLEAR_PASSWORD","CREDP_FLAGS_DONT_CACHE_TI","CREDP_FLAGS_IN_PROCESS","CREDP_FLAGS_TRUSTED_CALLER","CREDP_FLAGS_USER_ENCRYPTED_PASSWORD","CREDP_FLAGS_USE_MIDL_HEAP","CredReadDomainCredentialsFn","CredReadDomainCredentialsFn callback","CrediReadDomainCredentials","CrediReadDomainCredentials callback function [Security]","ntsecpkg/CrediReadDomainCredentials","security.credireaddomaincredentials"]
old-location: security\credireaddomaincredentials.htm
tech.root: security
ms.assetid: fa5c92be-c74b-4143-8526-b60c25461b8c
ms.date: 12/05/2018
ms.keywords: CREDP_FLAGS_CLEAR_PASSWORD, CREDP_FLAGS_DONT_CACHE_TI, CREDP_FLAGS_IN_PROCESS, CREDP_FLAGS_TRUSTED_CALLER, CREDP_FLAGS_USER_ENCRYPTED_PASSWORD, CREDP_FLAGS_USE_MIDL_HEAP, CredReadDomainCredentialsFn, CredReadDomainCredentialsFn callback, CrediReadDomainCredentials, CrediReadDomainCredentials callback function [Security], ntsecpkg/CrediReadDomainCredentials, security.credireaddomaincredentials
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
 - CredReadDomainCredentialsFn
 - ntsecpkg/CredReadDomainCredentialsFn
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
 - CrediReadDomainCredentials
---

# CredReadDomainCredentialsFn callback function


## -description

Reads a domain credential from the <a href="/windows/desktop/SecAuthN/credential-manager">Credential Manager</a>.

## -parameters

### -param LogonId [in]

The logon ID for which to read credentials.

### -param CredFlags [in]

Flags that determine the behavior of this function. The following flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_IN_PROCESS"></a><a id="credp_flags_in_process"></a><dl>
<dt><b>CREDP_FLAGS_IN_PROCESS</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The caller is in-process.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_USE_MIDL_HEAP"></a><a id="credp_flags_use_midl_heap"></a><dl>
<dt><b>CREDP_FLAGS_USE_MIDL_HEAP</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The caller should use the <a href="/windows/desktop/Rpc/the-midl-user-allocate-function">midl_user_allocate</a> function to allocate the <i>Credential</i> buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_DONT_CACHE_TI"></a><a id="credp_flags_dont_cache_ti"></a><dl>
<dt><b>CREDP_FLAGS_DONT_CACHE_TI</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Do not cache target information.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_CLEAR_PASSWORD"></a><a id="credp_flags_clear_password"></a><dl>
<dt><b>CREDP_FLAGS_CLEAR_PASSWORD</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
The credential data is passed as clear text.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_USER_ENCRYPTED_PASSWORD"></a><a id="credp_flags_user_encrypted_password"></a><dl>
<dt><b>CREDP_FLAGS_USER_ENCRYPTED_PASSWORD</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
The credential data is encrypted by using the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-rtlencryptmemory">RtlEncryptMemory</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CREDP_FLAGS_TRUSTED_CALLER"></a><a id="credp_flags_trusted_caller"></a><dl>
<dt><b>CREDP_FLAGS_TRUSTED_CALLER</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
The caller is a trusted process.

</td>
</tr>
</table>

### -param TargetInfo [in]

A pointer to a <a href="/windows/desktop/api/wincred/ns-wincred-credential_target_informationa">CREDENTIAL_TARGET_INFORMATION</a> structure that contains information about the target computer.

### -param Flags

Reserved. This parameter must be set to zero.

### -param Count

The number of elements in the <i>Credential</i> array.

### -param Credential [out]

A pointer to a pointer to an array of <a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-encrypted_credentialw">ENCRYPTED_CREDENTIALW</a> structures that receive the credentials that this function reads.

## -returns

If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code that indicates the reason it failed.

## -remarks

A pointer to the <b>CrediReadDomainCredentials</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>