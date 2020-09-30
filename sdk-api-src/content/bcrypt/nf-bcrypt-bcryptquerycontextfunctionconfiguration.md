---
UID: NF:bcrypt.BCryptQueryContextFunctionConfiguration
title: BCryptQueryContextFunctionConfiguration function (bcrypt.h)
description: Obtains the cryptographic function configuration information for an existing CNG context.
helpviewer_keywords: ["BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","BCRYPT_CIPHER_INTERFACE","BCRYPT_HASH_INTERFACE","BCRYPT_RNG_INTERFACE","BCRYPT_SECRET_AGREEMENT_INTERFACE","BCRYPT_SIGNATURE_INTERFACE","BCryptQueryContextFunctionConfiguration","BCryptQueryContextFunctionConfiguration function [Security]","CRYPT_DOMAIN","CRYPT_LOCAL","NCRYPT_KEY_STORAGE_INTERFACE","NCRYPT_SCHANNEL_INTERFACE","bcrypt/BCryptQueryContextFunctionConfiguration","security.bcryptquerycontextfunctionconfiguration"]
old-location: security\bcryptquerycontextfunctionconfiguration.htm
tech.root: security
ms.assetid: 4eea9efe-bf45-4926-86fc-9b12b6d292cd
ms.date: 12/05/2018
ms.keywords: BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, BCRYPT_CIPHER_INTERFACE, BCRYPT_HASH_INTERFACE, BCRYPT_RNG_INTERFACE, BCRYPT_SECRET_AGREEMENT_INTERFACE, BCRYPT_SIGNATURE_INTERFACE, BCryptQueryContextFunctionConfiguration, BCryptQueryContextFunctionConfiguration function [Security], CRYPT_DOMAIN, CRYPT_LOCAL, NCRYPT_KEY_STORAGE_INTERFACE, NCRYPT_SCHANNEL_INTERFACE, bcrypt/BCryptQueryContextFunctionConfiguration, security.bcryptquerycontextfunctionconfiguration
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
 - BCryptQueryContextFunctionConfiguration
 - bcrypt/BCryptQueryContextFunctionConfiguration
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
 - BCryptQueryContextFunctionConfiguration
---

# BCryptQueryContextFunctionConfiguration function


## -description

<p class="CCE_Message">[<b>BCryptQueryContextFunctionConfiguration</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>BCryptQueryContextFunctionConfiguration</b> function obtains the cryptographic function configuration information for an existing CNG context.

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

A pointer to a null-terminated Unicode string that contains the identifier of the context to obtain the function configuration information for.

### -param dwInterface [in]

Identifies the cryptographic interface to obtain the function configuration information for. This can be one of the following values.

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
Obtain the function configuration information from the list of asymmetric encryption functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CIPHER_INTERFACE"></a><a id="bcrypt_cipher_interface"></a><dl>
<dt><b>BCRYPT_CIPHER_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Obtain the function configuration information from the list of cipher functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_INTERFACE"></a><a id="bcrypt_hash_interface"></a><dl>
<dt><b>BCRYPT_HASH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Obtain the function configuration information from the list of hash functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_INTERFACE"></a><a id="bcrypt_rng_interface"></a><dl>
<dt><b>BCRYPT_RNG_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Obtain the function configuration information from the list of random number generator functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></a><a id="bcrypt_secret_agreement_interface"></a><dl>
<dt><b>BCRYPT_SECRET_AGREEMENT_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Obtain the function configuration information from the list of secret agreement functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SIGNATURE_INTERFACE"></a><a id="bcrypt_signature_interface"></a><dl>
<dt><b>BCRYPT_SIGNATURE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Obtain the function configuration information from the list of signature functions.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_KEY_STORAGE_INTERFACE"></a><a id="ncrypt_key_storage_interface"></a><dl>
<dt><b>NCRYPT_KEY_STORAGE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Obtain the function configuration information from the list of key storage functions.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SCHANNEL_INTERFACE"></a><a id="ncrypt_schannel_interface"></a><dl>
<dt><b>NCRYPT_SCHANNEL_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Obtain the function configuration information from the list of Schannel functions.

</td>
</tr>
</table>

### -param pszFunction [in]

A pointer to a null-terminated Unicode string that contains the identifier of the cryptographic function to obtain the configuration information for.

### -param pcbBuffer [in, out]

The address of a <b>ULONG</b> variable that, on entry, contains the size, in bytes, of the buffer pointed to by <i>ppBuffer</i>. If this size is not large enough to hold the context information, this function will fail with <b>STATUS_BUFFER_TOO_SMALL</b>.

After this function returns, this variable contains the number of bytes that were copied to the <i>ppBuffer</i> buffer.

### -param ppBuffer [in, out]

The address of a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_context_function_config">CRYPT_CONTEXT_FUNCTION_CONFIG</a> structure that receives the function configuration information retrieved by this function. The value pointed to by the <i>pcbBuffer</i> parameter contains the size of this buffer.

If the value pointed to by this parameter is <b>NULL</b>, this function will allocate the required memory. This memory must be freed when it is no longer needed by passing this pointer to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a> function.

If this parameter is <b>NULL</b>, this function will place the required size, in bytes, in the variable pointed to by the <i>pcbBuffer</i> parameter and return <b>STATUS_BUFFER_TOO_SMALL</b>.

For more information about the usage of this parameter, see Remarks.

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
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppBuffer</i> parameter is not <b>NULL</b>, and the value pointed to by the <i>pcbBuffer</i> parameter is not large enough to hold the set of contexts.

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
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified context or function could not be found.

</td>
</tr>
</table>

## -remarks

Each cryptographic function has only one set of configuration information, so although the <i>ppBuffer</i> parameter appears to be a used as an array, this function treats this as an array with only one element. The following example helps clarify how this parameter is used.


```cpp
// Get the function configuration information.
CRYPT_CONTEXT_FUNCTION_CONFIG FuncConfig;
ULONG uSize = sizeof(FuncConfig);
PCRYPT_CONTEXT_FUNCTION_CONFIG pFuncConfig = &FuncConfig;
status = BCryptQueryContextFunctionConfiguration(
    CRYPT_LOCAL, 
    pszContext, 
    NCRYPT_SCHANNEL_INTERFACE,
    pszFunction,
    &uSize, 
    &pFuncConfig);

```


<b>BCryptQueryContextFunctionConfiguration</b> can be called only in user mode.

## -see-also

<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_context_function_config">CRYPT_CONTEXT_FUNCTION_CONFIG</a>