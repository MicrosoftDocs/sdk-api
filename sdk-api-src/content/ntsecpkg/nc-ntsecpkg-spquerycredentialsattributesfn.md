---
UID: NC:ntsecpkg.SpQueryCredentialsAttributesFn
title: SpQueryCredentialsAttributesFn (ntsecpkg.h)
description: Retrieves the attributes for a credential.
helpviewer_keywords: ["SECPKG_ATTR_CIPHER_STRENGTHS","SECPKG_ATTR_SUPPORTED_ALGS","SECPKG_ATTR_SUPPORTED_PROTOCOLS","SECPKG_CRED_ATTR_NAMES","SpQueryCredentialsAttributes","SpQueryCredentialsAttributes callback function [Security]","SpQueryCredentialsAttributesFn","SpQueryCredentialsAttributesFn callback","_ssp_spquerycredentialsattributes","ntsecpkg/SpQueryCredentialsAttributes","security.spquerycredentialsattributes"]
old-location: security\spquerycredentialsattributes.htm
tech.root: security
ms.assetid: e9174a42-3ccd-4c9a-bf80-fba062df4459
ms.date: 12/05/2018
ms.keywords: SECPKG_ATTR_CIPHER_STRENGTHS, SECPKG_ATTR_SUPPORTED_ALGS, SECPKG_ATTR_SUPPORTED_PROTOCOLS, SECPKG_CRED_ATTR_NAMES, SpQueryCredentialsAttributes, SpQueryCredentialsAttributes callback function [Security], SpQueryCredentialsAttributesFn, SpQueryCredentialsAttributesFn callback, _ssp_spquerycredentialsattributes, ntsecpkg/SpQueryCredentialsAttributes, security.spquerycredentialsattributes
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
 - SpQueryCredentialsAttributesFn
 - ntsecpkg/SpQueryCredentialsAttributesFn
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
 - SpQueryCredentialsAttributes
---

# SpQueryCredentialsAttributesFn callback function


## -description

The <b>SpQueryCredentialsAttributes</b> function retrieves the attributes for a <a href="/windows/desktop/SecGloss/c-gly">credential</a>.

The <b>SpQueryCredentialsAttributes</b> function is the dispatch function for the 
<a href="/windows/desktop/api/sspi/nf-sspi-querycredentialsattributesa">QueryCredentialsAttributes</a> function of the 
<a href="/windows/desktop/SecAuthN/sspi">Security Support Provider Interface</a>.

## -parameters

### -param CredentialHandle [in]

A handle to the credential to query.

### -param CredentialAttribute [in]

<a href="/windows/desktop/SecGloss/a-gly">Attribute</a> to query. The following table lists the valid values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CRED_ATTR_NAMES"></a><a id="secpkg_cred_attr_names"></a><dl>
<dt><b>SECPKG_CRED_ATTR_NAMES</b></dt>
</dl>
</td>
<td width="60%">
The name of the principal associated with the <a href="/windows/desktop/SecGloss/c-gly">credentials</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SUPPORTED_ALGS"></a><a id="secpkg_attr_supported_algs"></a><dl>
<dt><b>SECPKG_ATTR_SUPPORTED_ALGS</b></dt>
</dl>
</td>
<td width="60%">
The algorithms supported with a particular credential.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_CIPHER_STRENGTHS"></a><a id="secpkg_attr_cipher_strengths"></a><dl>
<dt><b>SECPKG_ATTR_CIPHER_STRENGTHS</b></dt>
</dl>
</td>
<td width="60%">
The minimum and maximum cipher strength used with a credential.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_SUPPORTED_PROTOCOLS"></a><a id="secpkg_attr_supported_protocols"></a><dl>
<dt><b>SECPKG_ATTR_SUPPORTED_PROTOCOLS</b></dt>
</dl>
</td>
<td width="60%">
The protocols supported with a particular credential.

</td>
</tr>
</table>

### -param Buffer [out]

Pointer to a buffer that receives the requested attributes. Allocate memory for this buffer using the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer">AllocateClientBuffer</a> function, so that caller can free it by calling the 
<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function.

## -returns

If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists common reasons for failure and the error codes that the function should return.

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
Memory allocation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The credential handle is not valid.

</td>
</tr>
</table>

## -remarks

SSP/APs must implement the <b>SpQueryCredentialsAttributes</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpQueryCredentialsAttributes</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>