---
UID: NC:ntsecpkg.CredWriteFn
title: CredWriteFn (ntsecpkg.h)
description: Writes the specified credential to the Credential Manager.
helpviewer_keywords: ["CREDP_FLAGS_CLEAR_PASSWORD","CREDP_FLAGS_DONT_CACHE_TI","CREDP_FLAGS_IN_PROCESS","CREDP_FLAGS_TRUSTED_CALLER","CREDP_FLAGS_USER_ENCRYPTED_PASSWORD","CREDP_FLAGS_USE_MIDL_HEAP","CredWriteFn","CredWriteFn callback","CrediWrite","CrediWrite callback function [Security]","ntsecpkg/CrediWrite","security.crediwrite"]
old-location: security\crediwrite.htm
tech.root: security
ms.assetid: 19c7fe4d-9c7b-4547-baab-443483deb013
ms.date: 12/05/2018
ms.keywords: CREDP_FLAGS_CLEAR_PASSWORD, CREDP_FLAGS_DONT_CACHE_TI, CREDP_FLAGS_IN_PROCESS, CREDP_FLAGS_TRUSTED_CALLER, CREDP_FLAGS_USER_ENCRYPTED_PASSWORD, CREDP_FLAGS_USE_MIDL_HEAP, CredWriteFn, CredWriteFn callback, CrediWrite, CrediWrite callback function [Security], ntsecpkg/CrediWrite, security.crediwrite
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - CredWriteFn
 - ntsecpkg/CredWriteFn
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
 - CrediWrite
---

# CredWriteFn callback function


## -description

Writes the specified credential to the <a href="/windows/desktop/SecAuthN/credential-manager">Credential Manager</a>.

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

### -param Credential [in]

A pointer to an <a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-encrypted_credentialw">ENCRYPTED_CREDENTIALW</a> structure that represents the credentials to write.

### -param Flags [in]

Reserved. This parameter must be set to zero.

## -returns

If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code that indicates the reason it failed.

## -remarks

A pointer to the <b>CrediWrite</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>