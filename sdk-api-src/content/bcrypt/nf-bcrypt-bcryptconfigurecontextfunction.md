---
UID: NF:bcrypt.BCryptConfigureContextFunction
title: BCryptConfigureContextFunction function (bcrypt.h)
description: Sets the configuration information for the cryptographic function of an existing CNG context.
helpviewer_keywords: ["BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","BCRYPT_CIPHER_INTERFACE","BCRYPT_HASH_INTERFACE","BCRYPT_RNG_INTERFACE","BCRYPT_SECRET_AGREEMENT_INTERFACE","BCRYPT_SIGNATURE_INTERFACE","BCryptConfigureContextFunction","BCryptConfigureContextFunction function [Security]","CRYPT_DOMAIN","CRYPT_LOCAL","NCRYPT_KEY_STORAGE_INTERFACE","NCRYPT_SCHANNEL_INTERFACE","NCRYPT_SCHANNEL_SIGNATURE_INTERFACE","bcrypt/BCryptConfigureContextFunction","security.bcryptconfigurecontextfunction"]
old-location: security\bcryptconfigurecontextfunction.htm
tech.root: security
ms.assetid: e93c5e3e-3c63-49a3-8c8c-6510e10611ea
ms.date: 12/05/2018
ms.keywords: BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, BCRYPT_CIPHER_INTERFACE, BCRYPT_HASH_INTERFACE, BCRYPT_RNG_INTERFACE, BCRYPT_SECRET_AGREEMENT_INTERFACE, BCRYPT_SIGNATURE_INTERFACE, BCryptConfigureContextFunction, BCryptConfigureContextFunction function [Security], CRYPT_DOMAIN, CRYPT_LOCAL, NCRYPT_KEY_STORAGE_INTERFACE, NCRYPT_SCHANNEL_INTERFACE, NCRYPT_SCHANNEL_SIGNATURE_INTERFACE, bcrypt/BCryptConfigureContextFunction, security.bcryptconfigurecontextfunction
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptConfigureContextFunction
 - bcrypt/BCryptConfigureContextFunction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptConfigureContextFunction
---

# BCryptConfigureContextFunction function


## -description

<p class="CCE_Message">[<b>BCryptConfigureContextFunction</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>BCryptConfigureContextFunction</b> function sets the configuration information for the cryptographic function of an existing CNG context.

## -parameters

### -param dwTable [in]

Identifies the configuration table that the context exists in. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LOCAL"></a><a id="crypt_local"></a><dl>
<dt><b>CRYPT_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The context exists in the local-machine configuration table.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DOMAIN"></a><a id="crypt_domain"></a><dl>
<dt><b>CRYPT_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
This value is not available for use.

</td>
</tr>
</table>

### -param pszContext [in]

A pointer to a null-terminated Unicode string that contains the identifier of the context to set the cryptographic function configuration information for.

### -param dwInterface [in]

Identifies the cryptographic interface to set the function configuration information for. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></a><a id="bcrypt_asymmetric_encryption_interface"></a><dl>
<dt><b>BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Set the function configuration information in the list of asymmetric encryption functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CIPHER_INTERFACE"></a><a id="bcrypt_cipher_interface"></a><dl>
<dt><b>BCRYPT_CIPHER_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Set the function configuration information in the list of cipher functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_INTERFACE"></a><a id="bcrypt_hash_interface"></a><dl>
<dt><b>BCRYPT_HASH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Set the function configuration information in the list of hash functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_INTERFACE"></a><a id="bcrypt_rng_interface"></a><dl>
<dt><b>BCRYPT_RNG_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Set the function configuration information in the list of random number generator functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></a><a id="bcrypt_secret_agreement_interface"></a><dl>
<dt><b>BCRYPT_SECRET_AGREEMENT_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Set the function configuration information in the list of secret agreement functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SIGNATURE_INTERFACE"></a><a id="bcrypt_signature_interface"></a><dl>
<dt><b>BCRYPT_SIGNATURE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Set the function configuration information in the list of signature functions.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_KEY_STORAGE_INTERFACE"></a><a id="ncrypt_key_storage_interface"></a><dl>
<dt><b>NCRYPT_KEY_STORAGE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Set the function configuration information in the list of key storage functions.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SCHANNEL_INTERFACE"></a><a id="ncrypt_schannel_interface"></a><dl>
<dt><b>NCRYPT_SCHANNEL_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Set the function configuration information in the list of Schannel functions.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></a><a id="ncrypt_schannel_signature_interface"></a><dl>
<dt><b>NCRYPT_SCHANNEL_SIGNATURE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Set the function configuration information in the  list of signature suites that Schannel accepts for TLS 1.2.

<b>Windows Vista and Windows Server 2008:  </b>This value is not supported.

</td>
</tr>
</table>

### -param pszFunction [in]

A pointer to a null-terminated Unicode string that contains the identifier of the cryptographic function to set the configuration information for.

### -param pConfig [in]

The address of a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_context_function_config">CRYPT_CONTEXT_FUNCTION_CONFIG</a> structure that contains the new function configuration information.

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

<b>BCryptConfigureContextFunction</b> can be called only in user mode.

## -see-also

<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_context_function_config">CRYPT_CONTEXT_FUNCTION_CONFIG</a>